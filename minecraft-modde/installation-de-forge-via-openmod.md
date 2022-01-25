---
description: >-
  Dans ce tutoriel nous allons voir comment utiliser Openmod pour installer une
  version de Forge non disponible sur le panel OMGSERV.
---

# Installation de Forge via Openmod

{% hint style="danger" %}
Il est impossible d'installer avec Openmod les versions de **Forge supérieur à la 1.17**, dû à un changement dans les arguments de démarrage de Forge.&#x20;
{% endhint %}

### Installation

* Téléchargez sur [le site de Forge](http://files.minecraftforge.net) la version de Forge voulue (exemple: 1.12.2-14.23.5.2838).
* **Sur votre ordinateur**, ouvrez le `.jar` téléchargé avec Java puis installez Forge en version serveur, en prenant soin de saisir un dossier d'installation vide (voir la capture ci-dessous).
* Effectuez une réinstallation du serveur dans l'onglet "Réinstallation" puis en sélectionnant Openmod.
* Glisser **les deux `.jar` (server et client), le dossier `librairies` et le fichier `.json`** qui auront été extrait précédemment.
* Définir le **.jar client** en **.jar de démarrage** (OMGSERV le demande).

![](../.gitbook/assets/small\_capture\_d\_ecran\_2021\_01\_13\_a\_14\_26\_55\_49c6053892.png)

### Configuration

* Démarrez le serveur. Si celui ne démarre pas, vérifiez la version de Java dans les **propriétés** du serveur sur le panel&#x20;
  * Pour les versions en dessous de 1.16 sélectionner **Java 8**,
  * Pour la 1.16 sélectionner **Java 11**,
  * Pour la 1.17 sélectionner **Java 16**,
  * Pour la 1.18 sélectionner **Java 17**.
* Attendre que le serveur s'allume complètement (voir la console si besoin) puis éteindre le serveur.
* Se connecter en FTP sur le serveur avec un client FTP comme [FileZilla](https://filezilla-project.org/download.php?type=client) ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp)) (ou avec le WebFTP mais ceci est déconseillé car beaucoup de bugs).
* Glisser les mods dans le dossier `mods`, ainsi que la configuration s’il y en a une.&#x20;
* Supprimez le dossier `world` pour réinitialiser la map (⚠️ ceci aura pour conséquence de supprimer tout ce qui est présent sur la map, plus d'information avec [ce tutoriel](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)).
* Enfin, vous pouvez démarrer votre serveur et si tout à bien été fait (mods compatible entre eux, tous les fichiers présents et bonne version de Forge) normalement vous devriez avoir votre serveur Minecraft avec vos mods.