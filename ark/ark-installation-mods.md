---
description: >-
  L'installation automatique des mods sur OMGServ est quelques fois dans les
  choux, voici la manière manuelle de les installer pour une fonctionnalité sans
  égards
---

# Installation manuelle de mods

## Informations

Vous apprendrez ici à récupérer vos mods, les mettre sur votre serveur et paramétrer votre serveur pour qu'ARK : Survival Evolved fonctionne avec vos mods.

Pour commencer un peu d'infos pratiques :

Les mods pour Ark : Survival Evolved sont identifiés par un identifiant, une suite de 9 ou 10 chiffres en général, ils fonctionnent que si le dossier et le fichier .mod sont ensemble (par exemple pour le mod Structure+ : composé du dossier 731604991 et du fichier 731604991.mod, issus de la page [https://steamcommunity.com/sharedfiles/filedetails/?id=731604991](https://steamcommunity.com/sharedfiles/filedetails/?id=731604991))



## Télécharger et récupérer les mods

### Depuis Steam

Rendez vous sur le [Steam Workshop d'ARK : Survival Evolved](https://steamcommunity.com/app/346110/workshop/) depuis Steam, et cherchez vos mods, il vous suffira d'appuyer sur le bouton "S'abonner" pour télécharger le mod.

Vous trouverez vos mods téléchargés via ce système dans votre dossier Steam :&#x20;

* En général <mark style="color:purple;">C:\Program Files (x86)\Steam\steamapps\common\ARK\ShooterGame\Content\Mods</mark>&#x20;
* En cas de doute vous pouvez faire clic droit sur Ark depuis Steam, puis Propriétés -> Fichiers Locaux -> Parcourir, puis aller dans les dossiers <mark style="color:purple;">ShooterGame/Content/Mods</mark>&#x20;

### Depuis Epic Games

Mauvaise nouvelle pour les joueurs Epic Games, à moins d'avoir un ami sur Steam ou l'aide de la communauté, impossible de récupérer les mods dans le même état que sur Steam.

Vous trouverez néanmoins des [sites](http://steamworkshop.download/) pour télécharger le dossier du mod, il faudra alors demander à vos amis ou à la communauté de vous fournir le fichier .mod

Pour cela commencez par vous rendre sur le [Steam Workshop d'ARK : Survival Evolved](https://steamcommunity.com/app/346110/workshop/) puis cherchez les mods que vous souhaitez. En allant dessus il vous suffira de récupérer le lien de la page (exemple du mod Structure+ : [https://steamcommunity.com/sharedfiles/filedetails/?id=731604991](https://steamcommunity.com/sharedfiles/filedetails/?id=731604991)) et de le mettre dans un des [sites](http://steamworkshop.download/) qui proposent le téléchargement des mods !

Il suffira ensuite de récupérer d'une manière externe le fichier .mod de chaque mod, et de le garder aux côtés de votre mod précédemment acquis et de passer à l'étape suivante.



## Mise en ligne des mods

Connectez vous désormais grâce à un des services suivants :&#x20;

* **WebFTP** (plus simple et intuitif) depuis l'onglet **WebFTP** d'**OMGServ**&#x20;
* **FileZilla** (plus complexe mais plus stable et plus rapide) depuis l'onglet **Accès FTP** d'**OMGServ** et grâce au logiciel [FileZilla](https://filezilla-project.org/download.php?type=client) (gratuit)&#x20;

Une fois dans le système tout propre, allez dans le dossier <mark style="color:purple;">/ShooterGame/Content/Mods</mark> où vous trouverez le dossier 111111111, le fichier 111111111.mod, ainsi que les dossiers CrystalIsles, FjordurOfficial, LostIsland, Ragnarok, TheCenter et Valgero.&#x20;

Puis uploadez directement les mods dans le dossier serveur <mark style="color:purple;">ShooterGame/Content/Mods</mark>&#x20;

**ATTENTION** il faut qu'il y ai a la fois le dossier **ET** le fichier .mod du même identifiant&#x20;

Cette étape peut être un peu longue, étant donné que certains mods sont lourds, la mise en ligne va dépendre surtout de votre connexion internet.&#x20;

##

## Paramétrer le serveur

Une fois que tout est bon jusque là, il vous reste plus qu'à tout activer !

Depuis l'onglet **Mods** dans votre panneau de configuration **OMGserv** : ****&#x20;

\-> Activez les mods que vous souhaitez

\-> Vérifiez que la mise à jour automatique des mods soit **DESACTIVEE**

Et dans l'onglet **Propriétés** configurez votre serveur si besoin, puis démarrez le serveur. Le serveur prendra un peu de temps pour tout charger, puis il sera rapidement accessible.
