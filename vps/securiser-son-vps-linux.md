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

Rédaction en cours
