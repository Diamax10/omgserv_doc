---
description: >-
  Dans ce tutoriel apprenez à installer des plugins facilement sur un serveur
  Minecraft moddé.
---

# Installation de plugins sur son serveur moddé

**Installation de plugins sur son serveur moddé**

Pour installer des plugins sur un serveur moddé, il faudra veiller à **deux** critères:

* Avoir la même version de jeu.
* Utiliser des plugins fonctionnats avec le type de serveur choisi selon l'**API** avec lequel il fonctionne.

**Une API ?** Qu'est ce que c'est ? Une API ou **A**pplication **P**rogramming **I**nterface c'est un logiciel intermédiaire permettant à deux applications de se parler. Chaque fois que vous utilisez une application comme Facebook, que vous envoyez un message instantané ou que vous vérifiez la météo sur votre téléphone, vous utilisez une API.

**API existant:**

* **API Bukkit-Spigot:** Les plugins téléchargés sur les sites officiels de Bukkit et de Spigot seront compatible. 
* **API SpongeForge:** Les plugins télécgargés sur le site officiel de SpongeForge seront compatible.

**Les différents types de serveur:**

* [**Mohist**](https://mohistmc.com/)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.7.10, 1.12.2 et 1.16.5**.
* \*\*\*\*[**Catserver**](https://catserver.moe/)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.12.2**. 
* **KCauldron:** adpaté à l'API Bukkit-Spigot, disponible en **1.6.X et 1.7.10**. 
* **Thermos:** adpaté à l'API Bukkit-Spigot, disponible en **1.6.X et 1.7.10**.
* \*\*\*\*[**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)**:** adapté à l'API SpongeForge, disponible en **1.10.2, 1.11, 1.11.2, 1.12, 1.12.1 et 1.12.2**.

_Les projets KCauldron, Thermos et SpongeForge sont à l'abandon, il n'y aura plus de nouvelles versions pour ces types de serveurs._

**Quel type de serveur choisir ?**

* Il faut commencer par regarder votre version de jeu. Par exemple, je suis en 1.12.2; je pourrai installer Mohist, Catserver ou bien SpongeForge.
* Ensuite, je regarde mes besoins en plugins. Mes plugins viennent du site de Spigot donc je me dirige vers un type de serveur comme Mohist ou bien Catserver. 
* Pour terminer, je vais prendre Mohist car celui-ci me convient le mieux \(choix personnel\). 

Et voilà, plus qu'à suivre le tutoriel d'installation adapté disponible ci-dessous !

**Installation de Mohist, Catserver, KCauldron et Thermos:**

* Suivre en premier lieu ce [tutoriel](https://docs.idelya-network.fr/minecraft/utiliser-openmod-chez-omgserv)
* \( Pour **KCauldron et Thermos:** laisser Java 7 dans l'onglet **Propriétés**\) 
* Ajouter les [plugins ](https://www.omgserv.com/fr/faq-minecraft/comment_installer_un_plugin_sur_mon_serveur-65/)voulus dans le dossier plugins via le WebFTP ou à l'aide d'un client FTP
* Redémarrer le serveur afin que les plugins prennent effets.

:warning: Seul les plugins stipulants qu'ils sont compatible avec l'**API Bukkit-Spigot** fonctionneront.  
Il faut savoir aussi que les plugins influants sur les blocs comme WorldEdit peuvent ne pas être à 100% fonctionnels vis à vis des blocs moddés.

 **Installer SpongeForge:**

* Utiliser l'outil de réinstallation de OMGSERV
* Ajouter les **mods** dans le dossier Mods via le WebFTP ou à l'aide d'un client FTP
* Ajouter les **plugins dans le dossier mods** via le WebFTP ou à l'aide d'un client FTP
* Redémarrer le serveur

 :warning: Seul des plugins sous l'**API SpongeForge** peuvent être installés.

