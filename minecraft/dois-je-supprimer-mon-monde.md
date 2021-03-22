---
description: >-
  Il y a plusieurs raison de devoir supprimer son monde pour le réinitialiser.
  Nous allons voir différents cas où il est nécessaire de supprimer son monde
  pour le réinitialiser.
---

# Dois-je supprimer mon monde ?

### Changement de version Minecraft

#### Amélioration de version \(ex: 1.15 -&gt; 1.16\)

Que vous soyez en Vanilla ou avec des mods ou bien avec des plugins, **lors d'un changement de version Minecraft** il y a souvent des modifications de biomes, des ajouts de nouveaux blocs présent naturellement dans le monde.

Par exemple entre la 1.15 et la 1.16 il y a des gros changements dans le nether donc afin de profiter pleinement de ces modifications, il est nécessaire du supprimer le monde afin de le réinitialiser avec la nouvelle version.

{% hint style="danger" %}
**Cependant**, supprimer le monde veut dire **perte de toutes les constructions** effectuées dessus, ce qui peut être embêtant lors d'une survie en solo ou entre amis. Il faut savoir que les chunks non découverts par les joueurs, lorsqu'ils le seront, seront automatiquement généré avec la nouvelle version et donc les nouveaux blocs.
{% endhint %}

> Donc si vous ne souhaitez pas perdre vos constructions mais que vous souhaitez avoir les nouveaux blocs, il faut aller dans des chunks non découverts avec la précédente version \(souvent loin de votre point d'apparition\).

#### Rétrogradation de version \(ex: 1.16 -&gt; 1.12\)

Lors d'une rétrogradation de version il est nécessaire de réinitialiser le monde, sinon le serveur ne voudra pas démarrer.

### Ajout ou suppression d'un mod

Lorsque vous ajouter ou supprimer des mods il est possible que vous deviez supprimer votre monde. Mais vous allez me dire, quand exactement ? Et bien presque tout le temps.

#### Le mod modifie les biomes

C'est le cas par exemple de Biomes O' Plenty, ce mod ajoute des biomes donc si vous l'ajouter vous devez supprimer votre monde actuel et changer le type de génération dans votre fichier `server.properties`. De même si vous le supprimez.

#### Le mod ajoute des blocs

Lorsque le mod ajoute des blocs, il y a deux cas :

* Vous ajoutez le mod, il n'y a pas de besoin de supprimer le monde.
* Vous supprimez le mod, vous devez supprimer le monde uniquement si vous utilisez ses blocs sur le monde, sinon vous aurez une belle erreur disant que Minecraft ne trouve pas le bloc.

### Passage de moddé à Vanilla

Si vous passez votre serveur moddé à un serveur Vanilla \(avec ou sans plugins\), dans 99% des cas il est nécessaire de supprimer son monde. Pour savoir s'il est nécessaire de supprimer son monde, posez vous les questions suivantes et regardez les réponses apportées précédemment :

* Je change de version de Minecraft ?
* Mes anciens mods ajoutaient des blocs ou modifiaient les biomes ?

