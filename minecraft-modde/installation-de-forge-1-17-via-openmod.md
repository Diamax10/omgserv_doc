---
description: >-
  Dans ce tutoriel nous allons voir comment utiliser Openmod pour installer une
  version de Forge supérieure à la 1.16 non disponible sur le panel OMGSERV.
---

# Installation de Forge 1.17+ via Openmod

{% hint style="info" %}
Pour installer une version de Forge inférieure à la 1.17 veuillez suivre [ce tutoriel](installation-de-forge-via-openmod.md).
{% endhint %}

{% hint style="danger" %}
**Pensez à faire une sauvegarde** de votre serveur avant de suivre le tutoriel si vous souhaitez conserver des fichiers de votre serveur actuel. Pour cela nous avons fait [un tutoriel](../omgserv/sauvegarde-et-restauration.md).
{% endhint %}

### Installation (à partir de la 1.17)

* Téléchargez sur [le site de Forge](http://files.minecraftforge.net) la version de Forge voulue (exemple: 1.18.2-40.1.60).
* Effectuez une réinstallation du serveur dans l'onglet "Réinstallation" puis en sélectionnant "Openmod Forge 1.17+".
* Glissez le `.jar` précédemment téléchargé.
* Cliquez ensuite sur le bouton "Installer en OpenMod".
* Sélectionnez le `.jar` précédemment téléchargé et cliquez sur "Continuer".
* Après une courte installation, votre serveur est installé.

### Configuration

* Vérifiez la version de Java dans les **propriétés** du serveur sur le panel&#x20;
  * Pour la 1.17 sélectionner **Java 16**,
  * Pour la 1.18, 1.19 et 1.20 sélectionner **Java 17,**
  * Pour la 1.21+ sélectionner **Java 21.**
* Attendre que le serveur s'allume complètement (voir la console si besoin) puis éteindre le serveur.
* Se connecter en FTP sur le serveur avec un client FTP comme [FileZilla](https://filezilla-project.org/download.php?type=client) ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp)) (ou avec le WebFTP mais ceci est déconseillé car beaucoup de bugs).
* Glisser les mods dans le dossier `mods`, ainsi que la configuration s’il y en a une.&#x20;
* Supprimez le dossier `world` pour réinitialiser la map (⚠️ ceci aura pour conséquence de supprimer tout ce qui est présent sur la map, plus d'information avec [ce tutoriel](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)).
* Enfin, vous pouvez démarrer votre serveur et si tout à bien été fait (mods compatible entre eux, tous les fichiers présents et bonne version de Forge) normalement vous devriez avoir votre serveur Minecraft avec vos mods.
