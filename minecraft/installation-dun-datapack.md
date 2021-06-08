---
description: Dans ce tutoriel vous allez apprendre à installer un datapack
---

# Installation d'un datapack

## Un datapack qu'est-ce que c'est ?

Un datapack permet de modifier certain aspect du jeu comme la génération, les avancements et autre, il offre l'avantage de pouvoir être utiliser sur des serveurs de type vanilla ou snapshot mais également sur toutes les autres plateformes de serveur minecraft.

{% hint style="info" %}
Les datapck son uniquement disposible pour les version 1.13 et supérieurs de minecraft.

Un datapck se presente sous la forme d'un fichier zip.
{% endhint %}

{% hint style="warning" %}
Un datapack n'est pas un plugins ou un mod et permet moins de choses que les plugins ou mods. Son installtion doit c'effectuer sur votre serveur minecraft, il n'est pas necessaire d'effectuer une installation client églaement.
{% endhint %}

## Installation d'un datapack

Dans un premier temps, vous allez devoir récupère le nom de votre map. Pour se voir vous devez vous rendre sur **votre panel** ensuite vous rendre dans l'onglet **propriétés.** Une fois sur cette page vous devez localiser la partie nommé "**Nom de la map**" \(voire image ci-dessous\).

![](../.gitbook/assets/image%20%281%29.png)

Dans notre cas, le nom de la map est "world", vous allez ensuite devoir vous rendre dans les fichiers de votre serveur pour se faire je vous renvoie sur le tutoriel [Accéder au FTP](acceder-au-ftp.md).

Une fois connecter en FTP a votre serveur, vous devez vous rendre dans le dossier portant le nom de votre map dans mon cas le dossier "world'. Ensuite dans ce dossier localiser le dossier "**datapack**", une fois de ce dossier, il ne vous reste plus qu’à glisser votre datapack au format zip dedans et redémarrer votre serveur.

Pour vérifier que votre datapack a été chargé correctement, vous pouvez vous connecter à votre serveur est fait la commande :

```text
/datapack list
```

Si vous voyez votre datapack c'afficher en vert dans la liste félicitation, vous avez installé votre datapack correctement !

