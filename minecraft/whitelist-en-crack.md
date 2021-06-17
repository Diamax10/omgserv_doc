---
description: >-
  Tutoriel destiné à l'utilisation de la whitelist avec un serveur qui autorise
  les versions crack.
---

# Mettre une whitelist sur un serveur acceptant les versions crack

## Méthode traditionnelle

Pour ajouter un joueur qui ne s'est jamais connecté:

* `/whitelist off` et laissez le joueur entrer sur le serveur.
* `/whitelist add NOMDUJOUEUR`.
* Lorsque celui-ci est ajouté, effectuez `/whitelist on`.

Pour les joueurs déjà enregistrés via cette manipulation plus besoin de désactiver la whitelist.

En bref pour l'ajouter, il faut que le joueur se soit connecter au minimum **une fois** sur le serveur. **Pour contourner cela, suivez la méthode suivante.**

{% hint style="info" %}
**Pourquoi vous devez faire ça ?** Car comme votre serveur n'est plus connecté aux serveurs Mojang, il est incapable de déterminer l'identifiant du joueur associé au pseudo rentré. Pour qu'il puisse faire une relation entre les deux, il faut obligatoirement qu'il ait déjà vu le joueur, d'où l'obligation au joueur de se connecter sans whitelist.
{% endhint %}

## Méthode avec un plugin

Cette méthode nécessite un serveur de type Spigot, Paper, Tuinity ... bref un serveur pouvant accepter des plugins.

Téléchargez et glissez le plugin suivant dans votre dossier `plugins` : [https://www.spigotmc.org/resources/whitelist-players.56220/](https://www.spigotmc.org/resources/whitelist-players.56220/)

Ce plugin vous permettra d'accepter automatiquement les joueurs sur votre serveur sans qu'ils aient à se connecter au moins une fois dessus.

{% hint style="warning" %}
La whitelist de votre serveur doit être désactivée, sinon le plugin ne pourra pas fonctionner correctement. Pour désactiver la whitelist faites la commande `/whitelist off`
{% endhint %}

Maintenant pour ajouter un joueur à la whitelist géré par le plugin vous devez faire la commande `/wl add <pseudo>` et pour en enlever un faites `/wl remove <pseudo>`

Pour activer la whitelist du plugin faites `/wl on`

{% hint style="info" %}
Toutes les commandes du plugin sont disponibles sur la page Spigot du plugin
{% endhint %}

