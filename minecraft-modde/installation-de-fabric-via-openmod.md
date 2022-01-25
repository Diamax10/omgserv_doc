---
description: >-
  Dans ce tutoriel nous allons voir comment utiliser Openmod pour installer une
  version de Fabric non disponible sur le panel OMGSERV.
---

# Installation de Fabric via Openmod

{% hint style="danger" %}
**Pensez à faire une sauvegarde** de votre serveur avant de suivre le tutoriel si vous souhaitez conserver des fichiers de votre serveur actuel. Pour cela nous avons fait [un tutoriel](../omgserv/sauvegarde-et-restauration.md).
{% endhint %}

### Installation

* Téléchargez sur le site de Fabric l'installateur universel.
* Sur votre ordinateur, ouvrez le `.jar` téléchargé avec Java puis installez Fabric en version serveur, en prenant soin de saisir un dossier d'installation vide (voir la capture ci-dessous).

![Installateur Fabric, en mode serveur](<../.gitbook/assets/image (4).png>)

* Sur le panel OMGSERV, effectuez une réinstallation du serveur dans l'onglet "Réinstallation" puis en sélectionnant Openmod.
* Glissez le fichier `fabric-server-launch.jar` puis continuez.
* Sélectionner le fichier précédemment transféré en tant que "JAR de démarrage" et continuez.
* Connectez-vous sur le FTP de votre serveur (nous avons fait un [super tutoriel](../omgserv/acceder-au-ftp.md)).
* Transférez le dossier `libraries` et le fichier `server.jar`&#x20;
* Sur le panel OMGSERV dans l'onglet "Propriétés", changez la version de Java utilisée:
  * Pour les versions en dessous de 1.16 sélectionner **Java 8**,
  * Pour la 1.16 sélectionner **Java 11**,
  * Pour la 1.17 sélectionner **Java 16**,
  * Pour la 1.18 sélectionner **Java 17**.
* Vous pouvez maintenant démarrer votre serveur sous Fabric.&#x20;

### Configuration

{% hint style="info" %}
**Pour plus stabilité et fiabilité**, utilisez un [client FTP](../omgserv/acceder-au-ftp.md) au lieu du WebFTP d'OMGSERV.
{% endhint %}

Pour ajouter des mods sur votre serveur rien de plus simple ! Il suffit de mettre les **mods compatibles Fabric** dans le dossier `mods` se trouvant à la racine du serveur. Si ce dossier n'existe pas, il suffit juste de le créer.

Certains mods ont besoin de librairies pour fonctionner, si un dossier `libraries` est fourni avec le mod, il faut mettre son contenu dans le dossier `libraries` du serveur.
