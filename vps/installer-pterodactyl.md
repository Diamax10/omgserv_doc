---
description: >-
  Dans ce tutoriel, nous allons voir comment installer Pterodactyl sur un VPS
  OMGSERV et comment le sécuriser un minimum.
---

# Installer Pterodactyl

## Préambule

Ce tutoriel a été rédigé en Janvier 2023, bien que nous essayons de garder nos tutoriels le plus longtemps possible, certaines commandes sont susceptibles d'évoluer dans le temps.

Si vous souhaitez juste faire un serveur Minecraft, les offres [illimité](https://www.omgserv.com/fr/location/serveur-minecraft/illimite/) et [Xtrem](https://www.omgserv.com/fr/location/serveur-minecraft/xtrem/) sont un moyen simple d'avoir un serveur Minecraft fonctionnel rapidement et sans réelles connaissances.

## Prérequis

Dans ce tutoriel nous aurons besoins:

* Un VPS OMGSERV ([VPS SSD](https://www.omgserv.com/fr/location/vps/ssd/) ou [VPS Game](https://www.omgserv.com/fr/location/vps/game/))
* Un nom de domaine (vous pouvez en [obtenir un gratuitement ici](https://www.freenom.com/fr/index.html))
* D'une connexion Internet stable (il est déconseillé d'être dans un train ou un avion pour ce tutoriel)

## Installation du VPS

Tout d'abord rendez-vous dans l'onglet "Réinstallation" sur le panel OMGSERV et sélectionnez Debian version 11 "Bullseye". Une modal s'ouvre, vous invitant à renseigner des informations concernant votre future installation.

Dans le champ "Hostname", saisissez le sous-domaine associé à votre serveur. Dans ce tutoriel, nous allons utiliser le sous-domaine `node.exemple.local`.

Dans le champ "Nom d'utilisateur", saisissez le nom d'utilisateur qui sera créé pour accéder à votre VPS. Cela peut être votre prénom, votre pseudo, un nom de jeu, vous êtes de choisir ce que vous voulez. Cependant, il faut éviter d'utiliser des caractères spéciaux. Dans ce tutoriel, nous allons utiliser le nom d'utilisateur `vps_admin`.

Dans les options avancées, vous pouvez choisir la langue du VPS et d'autres options liées à l'authentification avec le VPS, laissez les par défaut. Dans ce tutoriel, nous allons mettre notre VPS en Anglais pour des raisons d'habitudes.

Une fois tout cela fait, vérifiez les informations que vous avez renseigné, puis, vous pouvez cliquer sur le bouton "Installer".

![](../.gitbook/assets/image.png)

## Connexion au VPS

Une fois le serveur installé, vous devriez normalement recevoir un mail de la part d'OMGSERV contenant toutes les informations de votre VPS. Si vous ne trouvez pas le mail dans votre boîte principale, vérifiez les spams mais aussi la boîte promotionnelle (sur Gmail notamment).

Pour vous connecter au VPS, nous allons utiliser un client SSH dont voici une liste non-exhaustive:

* [Putty](https://www.putty.org/) (Windows)
* [Termius](https://termius.com/) (Windows, MacOS, Linux)
* [Ásbrú Connection Manager](https://www.asbru-cm.net/) (Linux)

Connectez-vous au VPS en renseignant les identifiants SSH reçu par mail dans votre client SSH préféré.

## Première connexion

Une fois connecté au VPS, commencez par mettre à jour ses dépendances.

```shell
sudo apt update
sudo apt upgrade -y
```

La première fois que vous exécuterez la commande, le mot de passe de l'utilisateur en cours vous sera demandé. Lors de la saisie du mot de passe, celui-ci n'est pas affiché pour des raisons de sécurité (mais ne vous inquiétez pas, il s'écrit bien).

Pour coller un mot de passe étant dans votre presse papier, faites :

* Sous Windows: clic droit
* Sous MacOS: Cmd + V
* Sous Linux: Ctrl + Shift + V

{% hint style="info" %}
Utiliser la commande `sudo` vous permet de passer en mode administrateur (root).
{% endhint %}

## Sécurisation du VPS

Sécuriser un VPS est très important de nos jours. Les adresses IP de datacenter, voire, toutes les adresses IP du monde sont scannées continuellement par des robots, essayant de trouver la moindre faille de sécurité.&#x20;

Notre VPS comportant un serveur SSH exposé au grand public, il sera donc très probablement victime d'attaques brute-force, orchestrées par des pirates de l'Internet voulant obtenir des accès à des VPS pour les infecter et les utiliser à des fins illégales.

Pour prévenir ces attaques et se protéger, nous allons installer Crowdsec, une application scannant les logs de nos différents services et bloquant les pirates.

Pour l'installer quelques commandes suffisent (ces commandes sont tirées de leur [documentation](https://doc.crowdsec.net/docs/getting\_started/install\_crowdsec)).

```shell
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.deb.sh | sudo bash
sudo apt install crowdsec crowdsec-firewall-bouncer-iptables
sudo systemctl enable crowdsec-firewall-bouncer
```

## Installation du panel Pterodactyl

Pour la suite de ce tutoriel, nous allons nous servir de la [documentation officielle](https://pterodactyl.io/project/introduction.html) de Pterodactyl.

### Dépendances

Pour commencer nous allons installer les sources nécessaires pour l'installations des différents services utilisés par Pterodactyl.

```shell
sudo apt install curl

curl -sSL https://packages.sury.org/php/README.txt | sudo bash -x

curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

curl -sS https://downloads.mariadb.com/MariaDB/mariadb_repo_setup | sudo bash
```

Puis nous installons les services.

```shell
sudo apt -y install php8.1 php8.1-{common,cli,gd,mysql,mbstring,bcmath,xml,fpm,curl,zip} mariadb-server nginx tar unzip git redis-server

curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

### Téléchargement du panel

Nous allons télécharger le panel et le mettre dans son dossier d'installation.

```shell
sudo mkdir -p /var/www/pterodactyl
cd /var/www/pterodactyl

sudo curl -Lo panel.tar.gz https://github.com/pterodactyl/panel/releases/latest/download/panel.tar.gz
sudo tar -xzvf panel.tar.gz
sudo chmod -R 755 storage/* bootstrap/cache/
```

### Création des utilisateurs de base de données

Pour que le panel puisse fonctionner et qui vous puissiez créer des base de données facilement depuis le panel, nous avons besoin de créer deux utilisateurs dans la base de données gérant tout ça.

```shell
sudo mysql -u root -p
# Tapez sur la touche ENTRER (pour saisir un mot de passe vide)
```

À partir de ce moment là, vous êtes dans la console de la base de données. Dedans, vous devez écrire des commandes SQL.

Sur les deux premières commandes, vous allez devoir **définir un mot de passe** qui servira pour l'utilisateur du panel.&#x20;

Mettez un mot de passe aléatoire de plusieurs dizaines de caractères (vous pouvez utiliser des outils en ligne comme motdepasse.xyz pour générer un mot de passe aléatoire) et sauvegardez les dans un endroit sûr.&#x20;

Ici nous allons mettre comme mot de passe `A8iKi9Te53j9e9NXD4zaR6vN` et `3X75BHr8X3e8scw7jWV4pnBF`.

<pre class="language-sql"><code class="lang-sql">CREATE USER 'pterodactyl'@'127.0.0.1' IDENTIFIED BY '<a data-footnote-ref href="#user-content-fn-1">A8iKi9Te53j9e9NXD4zaR6vN</a>';
CREATE USER 'pterodactyluser'@'127.0.0.1' IDENTIFIED BY '<a data-footnote-ref href="#user-content-fn-2">3X75BHr8X3e8scw7jWV4pnBF</a>';

CREATE DATABASE panel;

GRANT ALL PRIVILEGES ON panel.* TO 'pterodactyl'@'127.0.0.1' WITH GRANT OPTION;
GRANT ALL PRIVILEGES ON *.* TO 'pterodactyluser'@'127.0.0.1' WITH GRANT OPTION;

FLUSH PRIVILEGES;
exit;
</code></pre>

## Configuration

### Panel

Il est temps maintenant de configurer l'environnement du panel afin qu'il sache comment fonctionner.

```shell
sudo cp .env.example .env
sudo composer install --no-dev --optimize-autoloader
# Répondez "yes"

sudo php artisan key:generate --force
```

Les commandes suivantes vont vous proposer de remplir des champs. Saisissez vos valeurs, voici un exemple:

<pre class="language-shell"><code class="lang-shell">sudo php artisan p:environment:setup

# Saisissez votre adresse mail (optionbel)
Egg Author Email [unknown@unknown.com]:
<strong>> contact@exemple.local
</strong></code></pre>

La seconde question de cette commande est l'URL qui permettra d'accéder à votre panel Pterodactyl. Dans ce tutoriel, nous allons utiliser `https://panel.exemple.local`. N'oubliez surtout pas le `https` !

<pre class="language-shell"><code class="lang-shell">Application URL [http://panel.example.com]:
<strong>> https://panel.exemple.local
</strong>
# Définition du fuseau horaire du panel
Application Timezone [UTC]:
<strong>> Europe/Paris
</strong></code></pre>

Les prochaines questions portent sur la configuration de divers drivers de gestion de données du panel. Répondez pour tous `redis`.

<pre class="language-shell"><code class="lang-shell">Cache Driver [Filesystem]:
  [redis    ] Redis (recommended)
  [memcached] Memcached
  [file     ] Filesystem
<strong>> redis
</strong>
Session Driver [Filesystem]:
  [redis    ] Redis (recommended)
  [memcached] Memcached
  [database ] MySQL Database
  [file     ] Filesystem
  [cookie   ] Cookie
<strong>> redis
</strong>
Queue Driver [Sync]:
  [redis   ] Redis (recommended)
  [database] MySQL Database
  [sync    ] Sync
<strong>> redis
</strong></code></pre>

Ensuite répondez "yes" puis "yes" ou "no" selon vos envies de partage de metrics avec Pterodactyl.

<pre><code>Enable UI based settings editor? (yes/no) [yes]:
<strong> > yes                                                              
</strong>
Enable sending anonymous telemetry data? (yes/no) [yes]:
<strong> > no
</strong></code></pre>

Puis nous allons finir par configurer les identifiants de connexion à Redis. Comme nous utilisons la configuration par défaut, vous pouvez appuyer sur la touche `Entrer` pour toutes les questions.

<pre class="language-shell"><code class="lang-shell">Redis Host [127.0.0.1]:
<strong> >                                                     
</strong>
Redis Password:
<strong> > 
</strong>
Redis Port [6379]:
<strong> >
</strong></code></pre>

### Base de données

```shell
sudo php artisan p:environment:database
```

<pre><code>Database Host [127.0.0.1]:
<strong> > 
</strong>
Database Port [3306]:
<strong> > 
</strong>
Database Name [panel]:
<strong> > 
</strong>                     
Database Username [pterodactyl]:
<strong> > 
</strong>
Database Password:
<strong> > <a data-footnote-ref href="#user-content-fn-3">********************</a>
</strong></code></pre>

### Emails

```shell
sudo php artisan p:environment:mail
```

<pre><code> Which driver should be used for sending emails? [SMTP Server]:
  [smtp    ] SMTP Server
  [mail    ] PHP's Internal Mail Function
  [mailgun ] Mailgun Transactional Email
  [mandrill] Mandrill Transactional Email
  [postmark] Postmark Transactional Email
<strong> > mail
</strong>
Email address emails should originate from [no-reply@example.com]:
<strong> > <a data-footnote-ref href="#user-content-fn-4">no-reply@node.exemple.local</a>
</strong>
Name that emails should appear from [Pterodactyl Panel]:
<strong> > Panel
</strong></code></pre>

### Finalisation

```shell
sudo php artisan migrate --seed --force
```

```shell
sudo php artisan p:user:make
```

<pre><code>Is this user an administrator? (yes/no) [no]:
<strong> > yes
</strong>
Email Address:
<strong> > admin@exemple.local
</strong>
Username:
<strong> > admin
</strong>
First Name:
<strong> > Admin
</strong>
Last Name:
<strong> > Local
</strong>
 Password:
<strong> > <a data-footnote-ref href="#user-content-fn-5">***************</a>
</strong>
+----------+--------------------------------------+
| Field    | Value                                |
+----------+--------------------------------------+
| UUID     | 108281cd-9872-4de0-a192-7a63364d2372 |
| Email    | admin@exemple.local                  |
| Username | admin                                |
| Name     | Admin Local                          |
| Admin    | Yes                                  |
+----------+--------------------------------------+
</code></pre>

```shell
sudo chown -R www-data:www-data /var/www/pterodactyl/*
```

<pre class="language-shell"><code class="lang-shell">sudo crontab -e

Select an editor.  To change later, run 'select-editor'.
  1. /bin/nano        &#x3C;---- easiest
  2. /usr/bin/vim.basic

<strong>Choose 1-2 [1]: 1
</strong></code></pre>

<pre class="language-shell"><code class="lang-shell"># ...
# For more information see the manual pages of crontab(5) and cron(8)
# 
# m h  dom mon dow   command
<strong>* * * * * php /var/www/pterodactyl/artisan schedule:run >> /dev/null 2
</strong></code></pre>

```shell
sudo nano /etc/systemd/system/pteroq.service
```

{% code title="pteroq.service" %}
```editorconfig
# Pterodactyl Queue Worker File
# ----------------------------------

[Unit]
Description=Pterodactyl Queue Worker
After=redis-server.service

[Service]
# On some systems the user and group might be different.
# Some systems use `apache` or `nginx` as the user and group.
User=www-data
Group=www-data
Restart=always
ExecStart=/usr/bin/php /var/www/pterodactyl/artisan queue:work --queue=high,standard,low --sleep=3 --tries=3
StartLimitInterval=180
StartLimitBurst=30
RestartSec=5s

[Install]
WantedBy=multi-user.target
```
{% endcode %}

```shell
sudo systemctl enable --now redis-server
sudo systemctl enable --now pteroq.service
```

[^1]: Mot de passe à modifier

[^2]: Mot de passe à modifier

[^3]: N'oubliez pas de saisir le mot de passe définis précédemment

[^4]: N'oubliez pas de modifier

[^5]: Saisissez un nouveau mot de passe pour votre utilisateur admin
