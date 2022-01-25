---
description: >-
  OpenMod permet de pouvoir ajouter et executer le .jar de votre choix sur votre
  serveur Minecraft.
---

# Utiliser Openmod

{% hint style="danger" %}
Forge 1.17+ et Mohist 1.18 ne peuvent pas être installé avec Openmod.
{% endhint %}

{% hint style="danger" %}
**Pensez à faire une sauvegarde** de votre serveur avant de suivre le tutoriel si vous souhaitez conserver des fichiers de votre serveur actuel. Pour cela nous avons fait [un tutoriel](sauvegarde-et-restauration.md).
{% endhint %}

### Utilisation

* Téléchargez le .jar souhaité sur son **site officiel**.
* Faites une réinstallation serveur avec l'Openmod et y glisser le **.jar** voulu.
* Définir le **.jar** en démarrage si cela est demandé.
* Si vous avez un serveur moddé, via le FTP ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp)), n'oubliez pas de mettre les dossiers `librairies` et `config` s'ils existent, ils sont important pour le démarrage du serveur.
* Démarrez le serveur. Si celui ne démarre pas, vérifiez la version de Java dans les **propriétés** du serveur sur le panel
  * Pour les versions en dessous de 1.16 sélectionner **Java 8**,
  * Pour la 1.16 sélectionner **Java 11**,
  * Pour la 1.17 sélectionner **Java 16**,
  * Pour la 1.18 sélectionner **Java 17**.

### Ajouter des mods pour les serveurs sous Forge, Mohist ou Fabric

* Se connecter en FTP sur le serveur avec un client FTP comme FileZilla ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp)) et glissez les mods dans le dossier `mods` puis les dossiers `librairies` et `config` s’ils existent.&#x20;
* Enfin, supprimez aussi le dossier `world` pour réinitialiser la map (plus d'informations avec [ce tutoriel](https://docs.idelya-network.fr/minecraft/dois-je-supprimer-mon-monde)).
