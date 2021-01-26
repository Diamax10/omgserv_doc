# Installation de Forge via Openmod

> Dans ce tutoriel nous allons voir comment utiliser l’openmods pour installer une version de forge non disponible sur le panel OMGSERV.

### Installation

* Téléchargez sur [le site de Forge](http://files.minecraftforge.net/) la version de Forge voulue \(exemple: 1.12.2-14.23.5.2838\).
* Installez Forge en version serveur, en prenant soin de saisir un dossier d'installation vide \(voir la capture ci-dessous\).
* Effectuez une réinstallation serveur avec l'openmod et glisser **les deux `.jar` \(server et client\), le dossier `librairies` et le fichier `.json`** qui auront été extrait précédemment.
* Définir le **.jar client** en **.jar de démarrage** \(OMGSERV le demande\).

![](../.gitbook/assets/small_capture_d_ecran_2021_01_13_a_14_26_55_49c6053892.png)

### Configuration

* Démarrez le serveur. Si celui ne démarre pas, vérifiez que Java 8 est activé dans les **propriétés** du panel.
* Attendre que le serveur s'allume complètement \(voir la console si besoin\) puis éteindre le serveur.
* Se connecter en FTP sur le serveur avec un client FTP comme FileZilla \(ou avec le WebFTP\) et glisser les mods dans le dossier `mods`, ainsi que la configuration s’il y en a une.
* Supprimez le dossier `world` pour réinitialiser la map \(⚠️ ceci aura pour conséquence de supprimer tout ce qui est présent sur la map, plus d'information avec [ce tutoriel](https://wiki.idelya-network.fr/tutorials/dois-je-supprimer-mon-monde)\).
* Enfin, vous pouvez démarrer votre serveur et si tout à bien été fait \(mods compatible entre eux, tous les fichiers présents et bonne version de Forge\) normalement vous devriez avoir votre serveur Minecraft avec vos mods.



