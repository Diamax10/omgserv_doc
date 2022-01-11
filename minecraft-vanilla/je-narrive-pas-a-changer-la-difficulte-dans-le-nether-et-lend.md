---
description: C'est un problème qui peut arriver avec les serveurs sous Spigot ou Paper.
---

# Je n'arrive pas à changer la difficulté dans le Nether et l'End

Pour cela nous avons développé un plugin afin de corriger ce problème [disponible ici](https://www.spigotmc.org/resources/difficultyfixer.89415/). Pour l'utiliser rien de plus simple, suivez les instructions ci-dessous:

* Mettez le plugin dans le dossier `plugins` de votre serveur
* Redémarrez votre serveur
* Regardez dans la console quels mondes le plugin a changé la difficulté, il doit afficher un message du type :
  * `[DifficultyFixer] Difficulty of world_nether changed to NORMAL`
* Une fois cela fait, vous pouvez supprimer le plugin de votre dossier `plugins`.
* Normalement maintenant vos mondes Nether et End sont synchronisés avec la difficulté du monde normal.

{% hint style="danger" %}
Si vous utilisez un plugin de gestion de monde comme **Multiverse Core**, le plugin ne sert à rien, il n'arrivera pas à modifier la difficulté du monde. Pour cela, référez-vous à la documentation de votre plugin, il doit y avoir des commandes spécifiques pour changer la difficulté des mondes.
{% endhint %}

