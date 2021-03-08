---
description: >-
  Dans ce tutoriel apprenez à créer un réseau de serveurs Minecraft reliés entre
  eux grâce à Bungeecord sur votre VPS !
---

# Créer un réseau de serveurs avec Bungeecord sur un VPS Linux

## Définition

Un réseau de serveurs est un ensemble de serveurs Minecraft indépendants \(ex: Spigot\) reliés par un serveur coordinateur \(ex: BungeeCord\). Ce dernier est un proxy qui "simule" un serveur Minecraft mais qui en réalité route le flux vers le bon serveur.

Par exemple, vous avez 2 serveurs Minecraft, imaginons un serveur survie et un serveur mini-jeux. Afin de pouvoir se téléporter entre ces deux serveurs sans se déconnecter, il faut que votre Minecraft croit que vous soyez sur un même serveur, c'est le rôle du proxy. Le joueur se connecte donc sur le proxy, puis ce dernier se chargera d'envoyer les informations du bon serveur au joueur.

## Installation

Dans ce tutoriel je pars du principe que vous avez un VPS, **configuré**, [**sécurisé**](https://docs.idelya-network.fr/vps/securiser-son-vps-linux) et avec [**Java d'installé**](https://docs.idelya-network.fr/vps/installer-java-sur-son-vps). Ce tutoriel a été rédigé avec une distribution comme Debian ou Ubuntu.

Commençons par créer un dossier qui contiendra les fichiers de notre proxy:

```bash
mkdir proxy && cd proxy
```

Ensuite, nous téléchargeons la dernière version de Bungeecord sur le site officiel. Généralement il faut directement aller chercher le fichier .jar sur la CI du projet qui se trouve ici : [https://ci.md-5.net/job/BungeeCord/](https://ci.md-5.net/job/BungeeCord/) Il faut prendre le _"Derniers artefacts construits avec succès"_ nommé `BungeeCord.jar`.

```bash
wget https://ci.md-5.net/job/BungeeCord/lastSuccessfulBuild/artifact/bootstrap/target/BungeeCord.jar
```

Afin d'avoir les fichiers de configuration par défaut, il faut allumer au moins une fois le proxy.

```bash
java -Xms128M -Xmx512M -jar BungeeCord.jar
```

{% hint style="info" %}
Un proxy Bungeecord ne consomme pas énormément de RAM, c'est plus le CPU et la bande passante qui seront sollicités. Il faut donc mieux avoir un très bon CPU et peu de RAM. 

La consommation de RAM va dépendre du nombre de plugin installés sur le proxy, plus il y aura de plugin, plus cela consommera de la RAM et naturellement du CPU. 

On estime qu'avec un proxy sans aucun plugin un consommation de 1Mo de RAM par joueur, donc si vous souhaitez avoir 500 joueurs, un peu plus de 500Mo de RAM sera nécessaire \(bien sûr ces données sont purement indicatives et dépendent de pleins de critères\).
{% endhint %}

## Configuration

Par défaut Bungeecord écoute sur le port `TCP 25577` qui n'est pas le port par défaut de Minecraft, c'est à dire que pour se connecter au Bungeecord, il faudra saisir dans Minecraft `adresseIP:25577` ce qui peut être embêtant dans certaines conditions. En plus de modifier cela nous allons voir quelques autres options configurable.

### config.yml

Le fichier `config.yml` nous permet de modifier toute la configuration du proxy. Voici une liste des paramètres dans le désordre qui sont souvent modifiés, bien-sûr je vous invite à regarder aussi les autres paramètres.

```yaml
# Défini la limite de joueur sur le proxy (-1 étant illimité)
player-limit: -1

# À mettre sur false si vous voulez accepter les cracks
online_mode: true

# La description du serveur afficher dans la liste des serveurs Minecraft
# (outil pour en générer un facilement: https://mctools.org/motd-creator)
motd: 'Superbe serveur Bungeecord'

# La valeur 0.0.0.0 permet au serveur d'écouter sur toutes les IP (conseillé),
# la partie après les deux points est le port d'écoute (ici 25565 étant celui de Minecraft par défaut)
host: 0.0.0.0:25565

# Nombre de joueurs max affiché dans la liste des serveurs Minecraft
# (mais n'est pas la limite réel, pour cela voir le paramètre player-limit)
max_players: 200

# Mettre à true si vous voulez que le joueur soit redirigé à la connexion vers 
# le premier serveur disponible défini dans priorities
force_default_server: true

# Je conseille de mettre à true, nous verrons dans la suite à quoi ça sert
ip_forward: true 

# Je conseille de mettre à false car ceci peut vite spam la console, pour faire simple
# à chaque fois qu'un joueur rafraîchira sa liste de serveur, ça mettra un message
log_pings: false 
```



