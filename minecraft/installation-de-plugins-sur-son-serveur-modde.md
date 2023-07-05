---
description: >-
  In this tutorial learn how to install plugins easily on a modded Minecraft
  server.
---

# Installation of plugins on your modded server

To install plugins on a modded server, you have to take care of **two** criteria:

* Have the same version of the game.
* Use plugins that work with the type of server chosen according to the **API** it works with.

## Introduction

{% hint style="info" %}
**An API?** What is an API? An API or Application Programming Interface is a middleware that allows two applications to talk to each other. Every time you use an application like Facebook, send an instant message or check the weather on your phone, you are using an API.
{% endhint %}

### Existing API

* **API Bukkit-Spigot:** Plugins downloaded from the official Bukkit and Spigot websites will be compatible.
* **API SpongeForge:** Plugins downloaded from the official SpongeForge website will be compatible.

### The different types of server

* [**Mohist**](https://mohistmc.com/)**:** adapted to the Bukkit-Spigot API, available in **1.7.10, 1.12.2 and 1.16.5**.
* [**Catserver**](https://catserver.moe/)**:** adapted to the Bukkit-Spigot API, available in **1.12.2**.
* [**KCauldron**](https://sourceforge.net/projects/kcauldron/)**:** adapted to the Bukkit-Spigot API, available in **1.6.X and 1.7.10**.
* [**Thermos**](https://github.com/CyberdyneCC/Thermos/releases)**:** adapted to the Bukkit-Spigot API, available in **1.6.X and 1.7.10**.
* [**SpongeForge**](https://www.spongepowered.org/downloads/spongeforge/stable/1.12.2)**:** adapted to the SpongeForge API, available in **1.10.2, 1.11, 1.11.2, 1.12, 1.12.1 and 1.12.2**.

{% hint style="warning" %}
The KCauldron and Thermos projects are abandoned, there will be no more new versions for these types of servers.
{% endhint %}

### What type of server should I choose?

* You should start by looking at your game version. For example, I am in 1.12.2; I could install Mohist, Catserver or SpongeForge.
* Then I look at my plugin needs. My plugins come from the Spigot site so I'm going for a server type like Mohist or Catserver.&#x20;
* Finally, I will take Mohist because it suits me best (personal choice).

And there you go, just follow the adapted installation tutorial available below!

## Install Mohist, Catserver, KCauldron or Thermos

* Follow [this tutorial](https://docs.idelya-network.fr/minecraft/utiliser-openmod-chez-omgserv) first.
* For **KCauldron** and **Thermos**: keep **Java 7** in the Properties tab.&#x20;
* Add the desired [plugins](https://www.omgserv.com/en/faq-minecraft/how\_to\_install\_plugins\_on\_my\_minecraft\_server-82/) to the plugins folder via WebFTP or using a FTP client.
* Restart the server so that the plugins take effect.

{% hint style="warning" %}
Only plugins that state that they are compatible with the **Bukkit-Spigot AP**I will work. You should also know that plugins that influence blocks like **WorldEdit** may not be 100% functional with respect to modded blocks.
{% endhint %}

## &#x20;**Install SpongeForge**

* Use the OMGSERV reinstallation tool.
* Add mods to the `mods` folder via WebFTP or using an FTP client.
* Add plugins to the `mods` folder via WebFTP or using an FTP client.
* Restart the server.

{% hint style="warning" %}
Only plugins under the **SpongeForge API** can be installed.
{% endhint %}
