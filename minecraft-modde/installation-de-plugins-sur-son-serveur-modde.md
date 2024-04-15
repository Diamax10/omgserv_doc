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

Dans notre cas, cela permet aux développeurs de plugins ou de mods de développer de nouvelles fonctionnalités plus rapidement et facilement sur les différentes versions de Minecraft.
{% endhint %}

### API existant:

* **API Bukkit-Spigot:** Les plugins téléchargés sur les sites officiels de Bukkit et de Spigot seront compatibles.&#x20;
* **API SpongeForge:** Les plugins téléchargés sur le site officiel de SpongeForge seront compatible.

### Les différents types de serveur:

{% tabs %}
{% tab title="1.6" %}
{% hint style="danger" %}
Cette version de Minecraft est très ancienne et n'est plus maintenue par les développeurs. Plus simplement s'il y a des bugs, c'est votre problème.
{% endhint %}

Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**KCauldron**](https://sourceforge.net/projects/kcauldron/)
* [**Thermos**](https://github.com/CyberdyneCC/Thermos/releases)
{% endtab %}

{% tab title="1.7" %}
{% hint style="danger" %}
Cette version de Minecraft est très ancienne et n'est plus maintenue par les développeurs. Plus simplement s'il y a des bugs, c'est votre problème.
{% endhint %}

Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/)
* [**KCauldron**](https://sourceforge.net/projects/kcauldron/)
* [**Thermos**](https://github.com/CyberdyneCC/Thermos/releases)
{% endtab %}

{% tab title="1.8 - 1.11" %}
Pour supporter les plugins compatibles Sponge:

* [**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)
{% endtab %}

{% tab title="1.12" %}
Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/)
* [**Magma**](https://magmafoundation.org/)
* [**Catserver**](https://catserver.moe/)

Pour supporter les plugins compatibles Sponge:

* [**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)
{% endtab %}

{% tab title="1.16" %}
Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/)
* [**Magma**](https://magmafoundation.org/)

Pour supporter les plugins compatibles Sponge:

* [**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)
{% endtab %}

{% tab title="1.18" %}
Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/) (n'est plus supporté par les développeurs)
* [**Magma**](https://magmafoundation.org/)
{% endtab %}

{% tab title="1.19" %}
Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/)

Pour supporter les plugins compatibles Bukkit et Spigot

* [**Arclight Horn**](https://github.com/IzzelAliz/Arclight/releases)
{% endtab %}

{% tab title="1.20" %}
Pour supporter les plugins compatibles Bukkit, Spigot et Paper:

* [**Mohist**](https://mohistmc.com/)

Pour supporter les plugins compatibles Bukkit et Spigot

* (1.20 - 1.20.1) [**Arclight Trials**](https://github.com/IzzelAliz/Arclight/releases)
* (1.20.4) [**Arclight Whisper**](https://github.com/IzzelAliz/Arclight/releases)
{% endtab %}
{% endtabs %}

## Quel type de serveur choisir ?

* Il faut commencer par regarder votre version de jeu. Par exemple, je suis en 1.12.2; je pourrai installer Mohist, Catserver ou bien SpongeForge.
* Ensuite, je regarde mes besoins en plugins. Mes plugins viennent du site de Spigot donc je me dirige vers un type de serveur comme Mohist ou bien Catserver.&#x20;
* Pour terminer, je vais prendre Mohist car celui-ci me convient le mieux (choix personnel).&#x20;

Et voilà, plus qu'à suivre le tutoriel d'installation adapté disponible ci-dessous !

## Installer Mohist, Catserver, KCauldron ou Thermos

* Suivre en premier lieu ce [tutoriel](https://docs.idelya-network.fr/minecraft/utiliser-openmod-chez-omgserv)
* (Pour **KCauldron et Thermos:** laisser Java 7 dans l'onglet **Propriétés,** passer en Java 11 pour **Mohist** 1.16 et Java 17 pour Mohist 1.18+)&#x20;
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
