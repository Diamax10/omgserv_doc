---
description: Installer Geyser de zéro sur Spigot ou Paper.
---

# Installer Geyser

### Pré-requis

* Serveur sous Spigot ou Paper (recommandé)

### Assignation d'un port

Aller dans la section "Plugins" du panel. Cliquer sur "Assigner un nouveau port". Une nouvelle ligne apparaît, notez quelque part l'adresse IP et le port générés.

<figure><img src="../.gitbook/assets/Screenshot 2024-05-20 at 18.16.11.png" alt=""><figcaption><p>Assignation d'un nouveau port pour le serveur</p></figcaption></figure>

### Téléchargements

Téléchargez la dernière version de Geyser sur [le site officiel](https://geysermc.org/download). Puis mettez le fichier .jar téléchargé dans le dossier `plugins` de votre serveur.&#x20;

Si vous voulez autoriser les joueurs Bedrock sans compte Java vous devez [télécharger Floodgate](https://geysermc.org/download#floodgate) en plus. N'oubliez pas de le mettre dans le dossier `plugins`.

### Configuration

Démarrer ou redémarrer (pas de reload) votre serveur Minecraft afin de générer les fichiers de configuration Geyser.

Une fois démarré complètement (vérifiez la console), éteignez le, pour éviter d'éventuelles erreurs.

Allez dans le dossier `plugins` du serveur. Un (ou deux) nouveau dossier doit apparaître `Geyser-Spigot` (et `floodgate`).

Allez dans le dossier `Geyser-Spigot` puis éditez le fichier config.yml.

#### Section `bedrock`

Dans la section `bedrock`, dé-commentez la ligne `address` (vers la ligne 17) en enlevant le `#` devant. Puis mettez en valeur votre adresse IP précédemment générée.

Sur la ligne `port` (vers la ligne 19) mettez en valeur le port précédemment généré.

Voici un exemple de configuration

```yaml
bedrock:
  # The IP address that will listen for connections.
  # Generally, you should only uncomment and change this if you want to limit what IPs can connect to your server.
  address: 62.210.234.69
  # The port that will listen for connections
  port: 40008
```

#### Section `remote`

Dans la section remote, changez les valeurs de `address`, `port` et `auth-type` en `auto`.

Voici un exemple de configuration

```yaml
remote:
  # The IP address of the remote (Java Edition) server
  # If it is "auto", for standalone version the remote address will be set to 127.0.0.1,
  # for plugin versions, it is recommended to keep this as "auto" so Geyser will automatically configure address, port, and auth-type.
  # Leave as "auto" if floodgate is installed.
  address: auto
  # The port of the remote (Java Edition) server
  # For plugin versions, if address has been set to "auto", the port will also follow the server's listening port.
  port: auto
  # Authentication type. Can be offline, online, or floodgate (see https://github.com/GeyserMC/Geyser/wiki/Floodgate).
  # For plugin versions, it's recommended to keep the `address` field to "auto" so Floodgate support is automatically configured.
  # If Floodgate is installed and `address:` is set to "auto", then "auth-type: floodgate" will automatically be used.
  auth-type: auto
```

{% hint style="info" %}
N'hésitez pas à lire les commentaires qu'il y a dans la configuration. Même si c'est un anglais, cela vous permet de savoir ce que ça fait et quelles valeurs sont possibles.
{% endhint %}

#### Fin de la configuration

Sauvegardez le fichier et démarrez le serveur. Une fois serveur démarré, cela devrait fonctionner. N'hésitez pas à regarder la console de votre serveur, vous devriez voir un ligne disant que Geyser est bien démarré, du type:

```log
[xx:xx:xx] [epollEventLoopGroup-3-1/INFO]: Started Geyser on 62.210.234.69:40008
```

### Résolution de problèmes

#### Adresse IP déjà utilisée

Si vous avez une erreur du type:

```
[xx:xx:xx] [epollEventLoopGroup-3-2/ERROR]: [Geyser-Spigot] Échec du démarrage de Geyser sur 62.210.234.69:40008
```

Et que vous avez bien généré cette adresse IP et ce port dans la section "Plugins" du panel; alors c'est qu'un autre serveur sur votre hôte utilise ce port frauduleusement.

Vous pouvez ouvrir un ticket au support afin qu'ils agissent pour libérer le port. Mais dans l'immédiat vous pouvez générer un nouveau port pour votre serveur et recommencer la configuration.
