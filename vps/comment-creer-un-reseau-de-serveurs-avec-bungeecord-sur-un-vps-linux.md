---
description: >-
  Dans ce tutoriel apprenez à créer un réseau de serveurs Minecraft reliés entre
  eux grâce à Bungeecord sur votre VPS !
---

# Créer un réseau de serveurs avec Bungeecord sur un VPS Linux

## Définition

Un réseau de serveurs est un ensemble de serveurs Minecraft indépendants \(ex: Spigot\) reliés par un serveur coordinateur \(ex: BungeeCord\). Ce dernier est un proxy qui "simule" un serveur Minecraft mais qui en réalité route le flux vers le bon serveur.

Par exemple, vous avez 2 serveurs Minecraft, imaginons un serveur survie et un serveur mini-jeux. Afin de pouvoir se téléporter entre ces deux serveurs sans se déconnecter, il faut que votre Minecraft croit que vous soyez sur un même serveur, c'est le rôle du proxy. Le joueur se connecte donc sur le proxy, puis ce dernier se chargera d'envoyer les informations du bon serveur au joueur.

## Installation

Dans ce tutoriel je pars du principe que vous avez un VPS, configuré, sécurisé et avec Java d'installé. Ce tutoriel a été rédigé avec une distribution comme Debian ou Ubuntu.

Commençons par créer un dossier qui contiendra les fichiers de notre proxy:

```text
mkdir proxy
cd proxy
```

Ensuite, nous téléchargeons la dernière version de Bungeecord sur le site officiel. Généralement il faut directement aller chercher le fichier .jar sur la CI du projet qui se trouve ici : [https://ci.md-5.net/job/BungeeCord/](https://ci.md-5.net/job/BungeeCord/) Il faut prendre le _"Derniers artefacts construits avec succès"_ nommé `BungeeCord.jar`.

```text
wget https://ci.md-5.net/job/BungeeCord/lastSuccessfulBuild/artifact/bootstrap/target/BungeeCord.jar
```

Afin d'avoir les fichiers de configuration par défaut, il faut allumer au moins une fois le proxy.

```text
java -Xms128M -Xmx512M -jar BungeeCord.jar
```

> Pour information, un proxy Bungeecord ne consomme pas énormément de RAM, c'est plus le CPU et la bande passante qui seront sollicités. Il faut donc mieux avoir un très bon CPU et peu de RAM. La consommation de RAM va dépendre du nombre de plugin installés sur le proxy, plus il y aura de plugin, plus cela consommera de la RAM et naturellement du CPU. On estime qu'avec un proxy sans aucun plugin un consommation de 1Mo de RAM par joueur, donc si vous souhaitez avoir 500 joueurs, un peu plus de 500Mo de RAM sera nécessaire \(bien sûr ces données sont purement indicatives et dépendent de pleins de critères\).

## Configuration

_Rédaction en cours ..._

