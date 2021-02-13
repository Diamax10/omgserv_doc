---
description: >-
  Parce que tout le monde n'a pas les compétences de créer un serveur Minecraft
  en ligne de commande, ce script vous permettra de le faire facilement !
---

# Script automatique de création d'un serveur Minecraft

### Pré-requis:

* Debian 10 \(Buster\)
* Un accès SSH au serveur \([tutoriel](https://www.omgserv.com/fr/faq-vps/comment_me_connecter_en_ssh__mon_vps-104/)\)

Si vous n'avez pas les pré-requis cité ci-dessus le script ne pourra fonctionner. Pour installer Debian 10 sur votre VPS, dirigez vous sur l'onglet "Réinstallation" sur votre panel. Les identifiants de connexion SSH vous seront envoyer par mail à la suite de l'installation \(vérifier vos spams\).

### Utilisation du script

Une fois connecté en SSH sur le serveur, collez la ligne de commande ci-dessous et appuyez sur entrée pour l'exécuter.

```bash
sudo wget -P /opt https://github.com/zendrique/mc-script/releases/download/1.4/boot.sh && sudo bash /opt/boot.sh
```

{% hint style="info" %}
**Sur Windows avec Putty**, faites clique droit avec votre souris pour coller la commande dans le terminal.

**Sur MacOS**, faites `Command`⌘`+ C` pour coller la commande.

**Sur Linux**, faites clique droit puis "Coller" **ou** `CTRL + SHIFT + C` pour coller la commande.
{% endhint %}

Une fois la commande exécuter, suivez tout simplement les instructions affichées dans le terminal. Lisez tout, c'est important.

### Accéder aux fichiers

Pour accéder aux fichiers de votre nouveau serveur afin de par exemple ajouter un plugin ou un mod, il faut vous connecter en SFTP.

Pour cela utilisez un client comme [FileZilla](https://filezilla-project.org/download.php?show_all=1) ou [WinSCP](https://winscp.net/eng/download.php). Saisissez vous informations de connexions :

* Dans le champ "Hôte", mettez l'adresse IP de votre serveur.
* Dans le champ "Port", mettez 22.
* Dans le champ "Utilisateur", mettez votre nom d'utilisateur avec lequel vous vous êtes connecté en SSH.
* Dans le champ "Mot de passe", mettez votre mot de passe avec lequel vous vous êtes connecté en SSH.
* Si vous avez la possibilité de choisir le type de protocol utilisé, choisissez "SFTP", sinon, ajoutez `sftp://` devant l'adresse IP dans le champ "Hôte".

Une fois tout cela rempli, vous pouvez votre connecter et ainsi avoir accès à tous les fichiers de votre serveur Minecraft.

