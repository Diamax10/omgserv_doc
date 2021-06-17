---
description: 'Dans ce tutoriel, apprenez à installer un datapack sur votre serveur Minecraft'
---

# Installation d'un datapack

## Un datapack qu'est-ce que c'est ?

Un datapack permet de modifier certains aspects du jeu comme la génération, les avancements et autres. Il offre l'avantage de pouvoir être utilisé sur des serveurs de type vanilla mais également sur toutes les autres plateformes de serveur Minecraft \(Forge, Spigot, etc\).

{% hint style="info" %}
Les datapack sont uniquement disponible pour les versions 1.13 et supérieures de Minecraft.

Il se présente sous la forme d'un fichier zip.
{% endhint %}

{% hint style="warning" %}
Un datapack n'est pas un plugin ni un mod et permet de faire moins de choses que les plugins ou les mods. 

Son installation s'effectue sur votre serveur Minecraft uniquement \(comme les plugins\).
{% endhint %}

## Installation d'un datapack

Dans un premier temps, vous allez devoir récupérer le nom de votre map. Pour se faire vous devez vous rendre sur **votre panel** ensuite vous rendre dans l'onglet **propriétés.** Une fois sur cette page vous devez localiser la partie nommée "**Nom de la map**" \(voir image ci-dessous\).

![](../.gitbook/assets/image%20%281%29.png)

Dans notre cas, le nom de la map est "world", vous allez ensuite devoir vous rendre dans les fichiers de votre serveur pour se faire je vous renvoie sur le tutoriel [Accéder au FTP](acceder-au-ftp.md).

Une fois connecté en FTP à votre serveur, vous devez vous rendre dans le dossier portant le nom de votre map dans mon cas le dossier "world". Ensuite dans ce dossier localisez le dossier "**datapack**", une fois dans ce dossier, il ne vous reste plus qu’à glisser votre datapack au format zip dedans et redémarrer votre serveur.

Pour vérifier que votre datapack a été chargé correctement, vous pouvez vous connecter à votre serveur et faire la commande :

```text
/datapack list
```

Si vous voyez votre datapack s'afficher en vert dans la liste, félicitation ! Vous avez installé votre datapack correctement !

