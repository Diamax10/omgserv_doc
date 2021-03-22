---
description: Tutorial for using the whitelist with a server that allows crack versions.
---

# Put a whitelist on a server accepting crack versions

For a new player:

* `/whitelist off` and let the player enter the server.
* Add `/whitelist add PLAYERNAME`.
* When this is added, run `/whitelist on`.

For players already registered via this operation there is no need to disable the whitelist.

In short, to add it, the player must have logged in at least **once** on the server.

{% hint style="info" %}
**Why do you need to do this?** Because your server is no longer connected to the Mojang servers, it is unable to determine the player ID associated with the entered nickname. In order for it to be able to make a connection between the two, it must have already seen the player, hence the requirement for the player to log in without a whitelist.
{% endhint %}

