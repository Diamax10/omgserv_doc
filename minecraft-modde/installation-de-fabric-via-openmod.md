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
