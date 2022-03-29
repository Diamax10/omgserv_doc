---
description: >-
  Beaucoup d'utilisateurs de VPS Linux débutent dans l'univers UNIX et ne savent
  pas sécuriser leur VPS contre des menaces basiques d'Internet.
---

# Sécuriser son VPS Linux

## Introduction

Protéger son VPS est essentiel, c'est la première chose à faire lorsqu'on vient juste de l'installer. Si celui-ci n'est pas protégé, il peut se faire pirater en quelques jours voire même quelques heures ! Ce tutoriel est là pour vous montrer quelques bases dans la sécurisation de votre VPS. Ceci empêchera les attaques les plus courantes.

## Installation & configurations&#x20;

### Fail2Ban (le plus simple mais moins efficace)

{% hint style="warning" %}
Attention, ce service fonctionne toujours mais nous vous recommandons la méthode suivante étant beaucoup plus efficace, couvrant plus de services et plus simple à la configuration sur le long terme.
{% endhint %}

Fail2Ban est une application permettant de bannir les adresses IP qui essayent de se connecter plusieurs fois (en échouant) à un service (par exemple en SSH). Ainsi les utilisateurs malveillants (souvent des robots) qui tente pleins de combinaisons de mot de passe et nom d'utilisateur ne pourront pas vous [brute force](https://fr.wikipedia.org/wiki/Attaque\_par\_force\_brute). Pour l'installer rien de plus simple, saisissez la commande suivante :

```bash
sudo apt update && sudo apt install rsyslog fail2ban
```

Une fois cela fait, votre VPS est déjà sécurisé. Toutefois, vous pouvez éditer sa configuration qui se trouve dans le fichier `/etc/fail2ban/jail.conf`. Dans ce fichier trois lignes sont importantes :

* `bantime`: représentant le temps que l'adresse IP sera bannis (par exemple: `120m` pour 2 heures).
* `findtime`: lapse de temps durant lequel Fail2Ban comptera le nombre d'échec d'une adresse IP (par exemple: `60m` afin de remonter les logs jusqu'à 1 heure).
* `maxretry`: nombre d'échecs d'authentification autorisés (par exemple: 5) mais attention à ne pas mettre une valeur trop faible au risque de vous bannir vous-même si vous faites une erreur.

{% hint style="warning" %}
Dans la configuration par défaut, ces lignes sont commentées par un `#` donc pour qu'elles soient effectives, il faut enlever le `#`.
{% endhint %}

Si vous le souhaitez vous pouvez regarder les autres paramètres, ainsi que la documentation de l'application pour avoir une configuration plus avancée.

À chaque fois que vous modifiez la configuration, il faut redémarrer l'application avec la commande :

```bash
sudo service fail2ban restart
```

### Crowdsec (plus complexe mais plus puissant)

Crowdsec est une application communautaire que protège activement votre serveur. Comme Fail2ban il est capable de bloquer les attaques brute-force sur votre serveur mais s'étend nativement au delà de l'accès SSH. Plusieurs "parsers" sont disponible pour détecter vos différents services (nginx, apache, mysql ...). Crowdsec communique en permanence avec les autres instances Crowdsec et partage des listes de blocage pour prévenir de certaines attaques.

Pour l'installer rien de plus simple tout est expliqué sur [leur documentation](https://doc.crowdsec.net/docs/getting\_started/install\_crowdsec) mais voici les commandes principales à exécuter :

```bash
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.deb.sh | sudo bash
```

{% hint style="warning" %}
Avant de continuer, il faut vérifier que le port TCP 8080 de votre serveur n'est pas utilisé, car Crowdsec en a besoin pour fonctionner. Pour cela la commande `netstat -lnpt` vous permet de vérifier ça.

Si vous utilisez Pterodactyl, le port de communication par défaut utilisé par Wings est le TCP 8080, il faut donc [changer cela dans la configuration de Wings](https://pterodactyl.io/wings/1.0/configuration.html#enabling-cloudflare-proxy).
{% endhint %}

```bash
sudo apt install crowdsec
```

```bash
sudo apt install crowdsec-firewall-bouncer-iptables && sudo systemctl enable crowdsec-firewall-bouncer
```

Pour ajouter de nouveaux "parsers" à votre Crowdsec et ainsi sécuriser vos applications, regardez directement sur le [hub Crowdsec](https://hub.crowdsec.net/browse/#collections) en cherchant le nom de l'application.

### SSH

Protéger son VPS avec des logiciels qui détectent les attaques c'est bien mais ces logiciels ne sont pas infaillibles. C'est pour cela qu'il est important de réduire sa surface d'exposition.

Pour cela il est important de ne pas autoriser les connexions SSH sur l'utilisateur `root` car de nombreux robots essayent de se connecter avec cet utilisateur.

Cependant, si vous faites cela, vous non plus vous ne serez plus autoriser à vous connecter avec l'utilisateur `root`, il faut donc créer un nouvel utilisateur appartenant au groupe `sudo` pour vous connecter en tant qu'administrateur sur votre VPS.

Pour ce faire, éditez et exécutez les commandes suivantes:

```shell
# Installation de sudo pour autoriser l'élévation de privilège
apt install sudo

# Création d'un utilisateur
adduser <votre user>
# Saisissez un mot de passe fort et répétez le.
# Puis appuyez sur entrée pour laissez les autres valeurs par défaut

# Ajout de l'utilisateur dans le groupe sudo
usermod -aG sudo <votre user>
```

Une fois cela fait, connectez-vous en SSH avec votre nouvel utilisateur pour valider sa création et valider l'appartenance au groupe `sudo` en passant à l'utilisateur `root` avec la commande:

```shell
sudo -s
```

Maintenant que vous vous êtes bien reconnecté en root, vous allez pouvoir désactiver la connexion via l'utilisateur root depuis SSH. Pour cela, il est nécessaire de modifier le fichier `/etc/ssh/sshd_config` et de modifier la valeur de `PermitRootLogin`

```shell
nano /etc/ssh/sshd_config

    # Editez PermitRootLogin à No
    PermitRootLogin No
```

Et maintenant, une fois le fichier de configuration sauvegardé, il suffit de redémarrer le service SSH. Pour cela exécutez la commande:

```shell
service sshd restart
```
