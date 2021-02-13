---
description: >-
  Tutoriel destiné à l'utilisation de la whitelist avec un serveur qui autorise
  les versions crack.
---

# Mettre une whitelist sur un serveur acceptant les versions crack

Pour ajouter un joueur qui ne s'est jamais connecté:

* `/whitelist off` et laissez le joueur entrer sur le serveur.
* `/whitelist add NOMDUJOUEUR`.
* Lorsque celui-ci est ajouté, effectuez `/whitelist on`.

Pour les joueurs déjà enregistrés via cette manipulation plus besoin de désactiver la whitelist.

En bref pour l'ajouter, il faut que le joueur se soit connecter au minimum **une fois** sur le serveur.

**Pourquoi vous devez faire ça ?** Car comme votre serveur n'est plus connecté aux serveurs Mojang, il est incapable de déterminer l'identifiant du joueur associé au pseudo rentré. Pour qu'il puisse faire une relation entre les deux, il faut obligatoirement qu'il ait déjà vu le joueur, d'où l'obligation au joueur de se connecter sans whitelist.

## English version

For a new player:

* `/whitelist off` and let the player enter the server.
* Add `/whitelist add PLAYERNAME`.
* When this is added, run `/whitelist on`.

For players already registered via this operation there is no need to disable the whitelist.

In short, to add it, the player must have logged in at least **once** on the server.
