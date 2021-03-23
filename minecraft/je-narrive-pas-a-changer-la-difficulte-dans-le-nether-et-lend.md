---
description: This is a problem that can happen with servers running Spigot or Paper.
---

# I can't change the difficulty in the Nether and End

For this we have developed a plugin to correct this problem [available here](https://www.spigotmc.org/resources/difficultyfixer.89415/). To use it, just follow the instructions below:

* Put the plugin in the plugins folder of your server 
* Restart your server 
* Look in the console which worlds the plugin has changed the difficulty, it should display a message like : 
  * `[DifficultyFixer] Difficulty of world_nether changed to NORMAL` 
* Once this is done you can delete the plugin from your plugins folder. 
* Normally now your Nether and End worlds are synchronized with the difficulty of the normal world.

{% hint style="danger" %}
If you use a world management plugin like **Multiverse Core**, the plugin is useless, it will not be able to change the difficulty of the world. For that, refer to the documentation of your plugin, there must be specific commands to change the difficulty of the worlds.
{% endhint %}

