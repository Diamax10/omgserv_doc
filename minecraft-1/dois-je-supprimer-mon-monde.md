---
description: >-
  There are several reasons to delete your world to reset it. We will see
  different cases where it is necessary to delete your world to reset it.
---

# Should I delete my world?

There are several reasons to delete your world to reset it. We will see different cases where it is necessary to delete your world to reset it.

## Minecraft version change

### Version upgrade \(ex: 1.15 -&gt; 1.16\)

Whether you are in Vanilla or with mods or plugins, **when you change Minecraft version** there are often biomes modifications, additions of new blocks naturally present in the world.

For example between 1.15 and 1.16 there are big changes in the nether so in order to take full advantage of these changes, it is necessary to remove the world in order to reset it with the new version.

{% hint style="danger" %}
**However**, deleting the world means **loss of all constructions** made on it, which can be annoying when surviving alone or with friends. You should know that chunks not discovered by the players, when they will be, will be automatically generated with the new version and thus the new blocks.
{% endhint %}

> So if you don't want to lose your constructions but you want to have the new blocks, you have to go to chunks undiscovered with the previous version \(often far from your spawn point\).

### Version downgrading \(ex: 1.16 -&gt; 1.12\)

When downgrading it is necessary to reset the world, otherwise the server will not want to start.

## Add or remove a mod

When you add or delete mods you may have to delete your world. But you're going to tell me, when exactly? Well almost all the time.

### The mod modifies biomes

This is the case for example of Biomes O' Plenty, this mod adds biomes so if you add it you have to remove your current world and change the generation type in your `server.properties` file. Same if you remove it.

### The mod adds blocks

When the mod adds blocks, there are two cases :

* You add the mod, there is no need to remove the world.
* You remove the mod, you have to remove the world only if you use its blocks on the world, otherwise you'll have a nice error saying that Minecraft can't find the block.

## Switch from modded to Vanilla

If you upgrade your modded server to a Vanilla server \(with or without plugins\), in 99% of the cases it is necessary to remove its world. To find out if it is necessary to delete your world, ask yourself the following questions and look at the answers given above:

* Do I change Minecraft version ?
* Did my old mods add blocks or modify biomes?

