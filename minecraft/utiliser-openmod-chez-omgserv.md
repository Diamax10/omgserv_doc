---
description: >-
  OpenMod permet de pouvoir ajouter et executer le .jar de votre choix sur votre
  serveur Minecraft.
---

# Utiliser Openmod chez OMGSERV

### Utilisation

* Téléchargez le .jar souhaité sur son **site officiel**.
* Faites une réinstallation serveur avec l'Openmod et y glisser le **.jar** voulu.
* Définir le **.jar** en démarrage si cela est demandé.
* Démarrez le serveur. Si celui ne démarre pas, vérifiez la version de Java dans les **propriétés** du serveur sur le panel
  * Pour les versions en dessous de 1.16 sélectionner **Java 8**,
  * Pour la 1.16 sélectionner **Java 11**,
  * Pour la 1.17 sélectionner **Java 16**,
  * Pour la 1.18 sélectionner **Java 17**.
* Se connecter en FTP sur le serveur avec un client FTP comme FileZilla ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp)) et glissez les mods dans le dossier `mods`, ainsi que la configuration s’il y en a une.&#x20;
* Enfin, supprimez aussi le dossier `world` pour réinitialiser la map (plus d'informations avec [ce tutoriel](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)).
