---
description: >-
  Vous avez des lags sur votre serveur Minecraft ? Dans ce tutoriel nous allons
  voir comment essayer de résoudre ces problèmes.
---

# Optimiser son serveur Minecraft

### Introduction

La communauté de Spigot propose [un guide](https://www.spigotmc.org/threads/guide-server-optimization%E2%9A%A1.283181/) pour optimiser efficacement son serveur Minecraft. Ce guide comprend une multitude d'options à modifier dans les différentes configuration disponible d'un serveur Minecraft. Ici nous allons vous donner nos modifications efficaces en se basant sur ce guide.

Tout d'abord, **choisissez une bonne API de serveur Minecraft**. Il en existe beaucoup sur Internet, les 4 grandes sont [Bukkit](https://dev.bukkit.org/), [Spigot](https://www.spigotmc.org/), [Paper](https://papermc.io/) et [Tuinity](https://github.com/Spottedleaf/Tuinity). Nous vous conseillons de prendre soit Paper soit Tuinity pour avoir de bonnes performances même sans changer la configuration. Tuinity est tout simplement une version améliorée de Paper, il se base dessus mais depuis la 1.17 il est fusionné dans Paper, rendant Paper encore plus performant. Nous avons fait [une page dédiée](quelle-api-minecraft-choisir.md#les-api) à cela.

Ce qui fait la puissance de Paper ce sont ses multiples options disponibles dans la configuration qui permettent de tout modifier pour optimiser au mieux son serveur. Mais c'est surtout son système de génération de monde utilisant plusieurs coeurs de processeur ce qui le rend très efficace !

### Configuration

Dans cette partie nous allons nous baser sur un serveur utilisant Paper, cependant si vous utiliser Bukkit, Spigot vous pouvez le suivre aussi, sauf qu'il faudra prendre en compte que certains fichier ne sont pas disponible sur certains type de serveur.&#x20;

{% hint style="warning" %}
**Depuis la version 1.19**, le fichier `paper.yml` est divisé en deux et se trouve dans le dossier `config` à la racine du serveur. La majorité de la configuration se trouve dans `paper-world-defaults.yml`.
{% endhint %}

{% tabs %}
{% tab title="bukkit.yml" %}
`chunk-gc` --> `period-in-ticks` mettre la valeur à 400.

`ticks-per` --> `monster-spawns` mettre la valeur à 4
{% endtab %}

{% tab title="spigot.yml" %}
`tick-inactive-villagers` mettre la valeur à `false`

`merge-radius` mettre les valeurs `item` à `4.0` et `exp` à `6.0`
{% endtab %}

{% tab title="paper.yml" %}
`max-auto-save-chunks-per-tick` mettre la valeur à 8

`optimize-explosions` mettre la valeur à `true`

`mob-spawner-tick-rate` mettre la valeur à 2

`disable-chest-cat-detection` mettre la valeur à `true`

`container-update-tick-rate` mettre la valeur à 3

`max-entity-collisions` mettre la valeur à 4

`grass-spread-tick-rate` mettre la valeur à 4

`hopper` --> `disable-move-event` mettre la valeur à `true`

`prevent-moving-into-unloaded-chunks` mettre la valeur à `true`

`use-faster-eigencraft-redstone` mettre la valeur à `true`

`per-player-mob-spawns` mettre la valeur à `true`
{% endtab %}
{% endtabs %}

