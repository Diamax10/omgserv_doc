---
description: >-
  Dans ce tutoriel apprenez à paramétrer VoiceChat facilement sur un serveur
  Minecraft.
---

# Paramétrer VoiceChat

Pour paramétrer VoiceChat rien de plus simple:

* Arrêter son serveur
* Demander un port, pour cela aller dans la section "Plugins" du panel OMGSERV, puis cliquer sur le bouton "Assigner un nouveau port"
* Se souvenir du port et de l'adresse IP attribuée
* Aller dans le fichier de configuration de VoiceChat (pour le plugin il est nommé `voicechat-server.properties`)
* Modifier les champs:
  * `bind_address`, mettre l'adresse IP attribuée
  * `port`, mettre le port attribué
  * `voice_host`, mettre l'adresse IP attribuée
* Enregistrer le fichier puis démarrer le serveur

{% hint style="info" %}
Si cela ne fonctionne pas et si dans la console du serveur, vous voyez un message de VoiceChat "Adresse déjà utilisée" ou "Address already used", refaite la procédure en demandant un nouveau port dans l'onglet "Plugins".
{% endhint %}
