---
description: >-
  Entre Bukkit, Spigot ou Paper il y a de quoi être perdu ! Cette page va vous
  permettre d'y voir plus clair et de prendre la meilleure API 😎
---

# Quelle API Minecraft choisir ?

## Qu'est-ce qu'une API ?

**Une API ?** Qu'est ce que c'est ? Une API ou **A**pplication **P**rogramming **I**nterface c'est un logiciel intermédiaire permettant à deux applications de se parler. Chaque fois que vous utilisez une application comme Facebook, que vous envoyez un message instantané ou que vous vérifiez la météo sur votre téléphone, vous utilisez une API.

Pour Minecraft, une API permet aux plugins (EssentialsX, WorldEdit ...) de communiquer facilement avec le serveur. Certaines API apportent des modifications aux mécaniques de Minecraft par défaut afin d'optimiser les performances du serveur.

## Les API

### [Bukkit](https://dev.bukkit.org)

Bukkit est l'API historique de Minecraft, elle ne modifie pas les mécaniques de Minecraft, elle permet juste aux serveurs Minecraft d'avoir des plugins.

### [Spigot](https://www.spigotmc.org)

Spigot est basée sur Bukkit et modifie quelques mécaniques de Minecraft mais rien de très méchant, elle limite surtout le nombre d'entités sur le serveur.

### [Paper](https://papermc.io) (à partir de Minecraft 1.8)

Paper est basée sur Spigot et modifie elle aussi des mécaniques de Minecraft, elle permet de pousser l'optimisation de Spigot plus loin. De plus, elle délègue la génération du monde sur d'autres coeurs du processeur, ce qui soulage beaucoup le serveur et lui permet de traiter plus efficacement les mécaniques de Minecraft basiques.

Pour la version 1.18 cela en fait la meilleure API intégrant les optimisations de Tuinity depuis la 1.17.

### [Tuinity](https://github.com/Tuinity/Tuinity) (à partir de Minecraft 1.15 jusqu'à 1.17)

Tuinity est basée sur Paper et optimise encore plus les mécaniques de Minecraft. Tuinity est intégré dans Paper depuis la 1.17, donc pour profiter des optimisations de Tuinity, il suffit de télécharger une version de Paper supérieur à la 1.17.

### [Airplane](https://airplane.gg) (à partir de Minecraft 1.16 jusqu'à 1.17)

Airplane est basée sur Tuinity et optimise de façon intelligente les mécaniques de Minecraft pour gagner énormément en performance sans toucher à l'expérience de jeu du joueur.

Très clairement Airplane est aujourd'hui la meilleure API 1.16-1.17 mais le projet a été abandonné par son développeur pour manque de temps, c'est pour cela qu'il n'y a plus de mises à jour.

### [Purpur](https://purpurmc.org/downloads) (à partir de Minecraft 1.14)

Purpur est basée sur Paper et permet de modifier un très grand nombre de mécanique Minecraft via sa configuration. Purpur est destiné aux utilisateurs avancés. De base sans aucun paramétrage il n'optimise pas le serveur.

## Les plugins

Majoritairement tous les plugins compatibles Bukkit ou Spigot sont compatibles avec Paper, Tuinity et Airplane.

