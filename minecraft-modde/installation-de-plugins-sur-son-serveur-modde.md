---
description: >-
  Dans ce tutoriel apprenez à installer des plugins facilement sur un serveur
  Minecraft moddé.
---

# Installation de plugins sur son serveur moddé

Pour installer des plugins sur un serveur moddé, il faudra veiller à **deux** critères:

* Avoir la même version de jeu.
* Utiliser des plugins fonctionnants avec le type de serveur choisi selon l'**API** avec lequel il fonctionne.

## Introduction

{% hint style="info" %}
**Une API ?** Qu'est ce que c'est ? Une API ou **A**pplication **P**rogramming **I**nterface c'est un logiciel intermédiaire permettant à deux applications de se parler. Chaque fois que vous utilisez une application comme Facebook, que vous envoyez un message instantané ou que vous vérifiez la météo sur votre téléphone, vous utilisez une API.
{% endhint %}

### API existant:

* **API Bukkit-Spigot:** Les plugins téléchargés sur les sites officiels de Bukkit et de Spigot seront compatibles.&#x20;
* **API SpongeForge:** Les plugins télécgargés sur le site officiel de SpongeForge seront compatible.

### Les différents types de serveur:

* [**Mohist**](https://mohistmc.com)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.7.10, 1.12.2, 1.16.5 **~~**et 1.18.1**~~.
* [**Catserver**](https://catserver.moe)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.12.2**.&#x20;
* [**KCauldron**](https://sourceforge.net/projects/kcauldron/)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.6.X et 1.7.10**.&#x20;
* [**Thermos**](https://github.com/CyberdyneCC/Thermos/releases)**:** adpaté à l'API Bukkit-Spigot, disponible en **1.6.X et 1.7.10**.
* [**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)**:** adapté à l'API SpongeForge, disponible en **1.10.2, 1.11, 1.11.2, 1.12, 1.12.1 et 1.12.2**.

{% hint style="warning" %}
Les projets KCauldron et Thermos sont à l'abandon, il n'y aura plus de nouvelles versions pour ces types de serveurs.
{% endhint %}

## Quel type de serveur choisir ?

* Il faut commencer par regarder votre version de jeu. Par exemple, je suis en 1.12.2; je pourrai installer Mohist, Catserver ou bien SpongeForge.
* Ensuite, je regarde mes besoins en plugins. Mes plugins viennent du site de Spigot donc je me dirige vers un type de serveur comme Mohist ou bien Catserver.&#x20;
* Pour terminer, je vais prendre Mohist car celui-ci me convient le mieux (choix personnel).&#x20;

Et voilà, plus qu'à suivre le tutoriel d'installation adapté disponible ci-dessous !

## Installer Mohist, Catserver, KCauldron ou Thermos

* Suivre en premier lieu ce [tutoriel](https://docs.idelya-network.fr/minecraft/utiliser-openmod-chez-omgserv)
* (Pour **KCauldron et Thermos:** laisser Java 7 dans l'onglet **Propriétés** et passer en Java 11 pour **Mohist** 1.16)&#x20;
* Ajouter les [plugins ](https://www.omgserv.com/fr/faq-minecraft/comment\_installer\_un\_plugin\_sur\_mon\_serveur-65/)voulus dans le dossier plugins à l'aide d'un client FTP ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp))
* Redémarrer le serveur afin que les plugins prennent effets.

{% hint style="warning" %}
Seul les plugins stipulants qu'ils sont compatible avec l'**API Bukkit**, **Spigot** ou **Paper** fonctionneront.\
Il faut savoir aussi que les plugins influants sur les blocs comme **WorldEdit** peuvent ne pas être à 100% fonctionnels vis à vis des blocs moddés.
{% endhint %}

## **Installer SpongeForge**

* Utiliser l'outil de réinstallation de OMGSERV
* Ajouter les **mods** dans le dossier Mods à l'aide d'un client FTP ([tutoriel](https://docs.idelya-network.fr/minecraft/acceder-au-ftp))
* Ajouter les **plugins dans le dossier mods** à l'aide d'un client FTP
* Redémarrer le serveur

{% hint style="warning" %}
Seul des plugins sous l'**API SpongeForge** peuvent être installés.
{% endhint %}
