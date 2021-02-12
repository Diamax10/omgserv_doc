---
description: >-
  Dans ce tutoriel nous allons voir comment utiliser l’openmod pour installer
  une version de forge non disponible sur le panel OMGSERV.
---

# Installation de Forge via Openmod

### Installation

* Téléchargez sur [le site de Forge](http://files.minecraftforge.net) la version de Forge voulue \(exemple: 1.12.2-14.23.5.2838\).
* Installez Forge en version serveur, en prenant soin de saisir un dossier d'installation vide \(voir la capture ci-dessous\).
* Effectuez une réinstallation du serveur dans l'onglet "Réinstallation" puis en sélectionnant Openmod.
* Glisser **les deux `.jar` \(server et client\), le dossier `librairies` et le fichier `.json`** qui auront été extrait précédemment.
* Définir le **.jar client** en **.jar de démarrage** \(OMGSERV le demande\).

### Configuration

* Démarrez le serveur. Si celui ne démarre pas, vérifiez que Java 8 est activé dans les **propriétés** du panel.
* Attendre que le serveur s'allume complètement \(voir la console si besoin\) puis éteindre le serveur.
* Se connecter en FTP sur le serveur avec un client FTP comme [FileZilla](https://filezilla-project.org/download.php?type=client) \([tutoriel](https://www.omgserv.com/fr/faq-minecraft/comment_cr_er_et_utiliser_mon_acc_s_ftp-66/)\) \(ou avec le WebFTP mais ceci est déconseillé car beaucoup de bugs\).
* Glisser les mods dans le dossier `mods`, ainsi que la configuration s’il y en a une. 
* Supprimez le dossier `world` pour réinitialiser la map \(:warning: ceci aura pour conséquence de supprimer tout ce qui est présent sur la map, plus d'information avec [ce tutoriel](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)\).
* Enfin, vous pouvez démarrer votre serveur et si tout à bien été fait \(mods compatible entre eux, tous les fichiers présents et bonne version de Forge\) normalement vous devriez avoir votre serveur Minecraft avec vos mods.

## English version

> In this tutorial we will see how to use openmod to install a forge version not available on the OMGSERV panel.

### Installation

* Download on [Forge's website](http://files.minecraftforge.net) the desired version of Forge \(example: 1.12.2-14.23.5.2838\).
* Install Forge in server version, take care to enter an empty installation folder \(see the capture below\).
* Perform a server reinstallation in the "Reinstall" tab and select Openmod.
* Drag **both `.jar` \(server and client\), the `libraries` folder and the `.json` file** that will have been extracted previously.
* Set the **.jar client** as **.jar startup** \(OMGSERV requires it\).

### Configuration

* Start the server. If it does not start, make sure that Java 8 is enabled in the panel **properties**.
* Wait for the server to turn on completely \(see the console if necessary\) then turn off the server.
* Connect in FTP on the server with an FTP client like [FileZilla](https://filezilla-project.org/download.php?type=client) \([tutorial](https://www.omgserv.com/en/faq-minecraft/how_to_create_and_use_ftp_acces-86/)\) \(or with WebFTP from the OMGSERV panel but this is not recommended because many bugs\). 
* Drag the mods into the `mods` folder, as well as the configuration if there is one.
* Delete the `world` folder to reset the map \(:warning: this will delete everything on the map, more information with [this tutorial](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)\).
* Finally, you can start your server and if everything has been well done \(mods compatible with each other, all files present and good version of Forge\) normally you should have your Minecraft server with your mods.

