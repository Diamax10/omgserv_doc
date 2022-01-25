---
description: >-
  Le modpack All The Mods 6 de base tourne sur une version basique de Forge, ne
  prenant pas en charge les plugins et offrant peu de fonctionnalités
  d'optimisation.
---

# ATM6 - Migrer vers Mohist - All The Mods 6

{% hint style="danger" %}
**Pensez à faire une sauvegarde** de votre serveur avant de suivre le tutoriel si vous souhaitez conserver des fichiers de votre serveur actuel. Pour cela nous avons fait [un tutoriel](../omgserv/sauvegarde-et-restauration.md).
{% endhint %}

### Migration

Faire une sauvegarde du serveur actuel (surtout la map si vous souhaitez la conserver).

Télécharger les fichiers serveurs de ATM6 sur le lien [https://www.curseforge.com/minecraft/modpacks/all-the-mods-6/files](https://www.curseforge.com/minecraft/modpacks/all-the-mods-6/files). Les fichiers serveurs se trouve dans la section additionnel et l'archive se nomme de cette manière `SIMPLE-SERVER-FILES-x.x.x.zip`.

Executer le fichier `startserver.bat` (sous Windows), ce qui téléchargera tous les fichiers nécessaire au serveur.

Attendre le message demandant de confirmer les EULA (au bout de 2 à 15 minutes), à ce moment il faudra faire `CTRL + C` pour stopper l'installation.

Télécharger Mohist 1.16 : [https://mohistmc.com/download/](https://mohistmc.com/download/)

Réinstaller son serveur Minecraft en OpenMod et en mettant comme jar de démarrage le fichier Mohist télécharger juste avant.

Cocher Java 11 dans les propriétés de son serveur.

Démarrer son serveur, attendre 1 minute et regarder dans la console s'il est bien démarré, sinon attendre qu'il finisse de démarrer.

Arrêter son serveur.

Se connecter au FTP avec Filezilla (et pas avec le Webftp), voici un tuto [https://docs.idelya-network.fr/minecraft/acceder-au-ftp](https://docs.idelya-network.fr/minecraft/acceder-au-ftp).

Glisser les dossiers (précédemment créés avec l'installateur `startserver.bat`) `mods`, `config`, `defaultconfigs` et `kubejs` sur le serveur avec le FTP.

Si vous aviez un ancien monde, supprimer le dossier `world` existant sur le serveur puis glisser votre dossier `world` sur le serveur.

Démarrer le serveur et attendre 5 à 10 minutes qu'il s'allume.

