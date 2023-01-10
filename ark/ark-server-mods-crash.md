---
description: >-
  Vous avez tenté d'installer des mods depuis le module d'installation
  automatique, et depuis votre serveur ARK : Survival Evolved se stoppe
  directement après le démarrage, cette page est là pour vous !
---

# Serveur qui crash suite à l'installation de mods

## Informations

Il faut savoir que de temps en temps, l'installation automatique des mods créer des erreurs, la plus commune étant d'empêcher complètement le serveur de démarrer, il suffira de faire un choix parmis les solutions suivantes :&#x20;

* Depuis l'onglet **Réinstallation** d'**OMGServ**, faites une installation propre puis installez vos mods en suivant l'aide pour [installer des mods manuellement](ark-installation-mods.md). Sachant que le serveur est lourd et va prendre un certain temps pour OMGServ pour tout réinstaller.
* En passant par **FTP**, en nettoyant manuellement ce qui cause cette erreur, tout aussi simple, surtout plus rapide et permet de garder tous les paramètres du serveur.

## Réinstallation du serveur

Si vous avez décidé de réinstaller le serveur, il vous suffit de vous rendre dans l'onglet Réinstallation d'OMGServ et de vous faire un système tout propre.

Cela peut prendre jusqu'à 2H, alors armez vous de patience.

Une fois fait, il suffira de vous rendre sur la page d'aide à [l'installation manuelle de mods](ark-installation-mods.md) pour avoir son serveur sans erreurs.&#x20;

## Utilisation de FTP&#x20;

Si vous avez fait le choix de réparer le souci vous même, ça prendra quelques minutes tout au plus en suivant les instructions suivantes.

Connectez vous grâce à un des services suivants :

* **WebFTP** (plus simple et intuitif) depuis l'onglet **WebFTP** d'**OMGServ**
* **FileZilla** (plus complexe mais plus stable et plus rapide) depuis l'onglet **Accès FTP** d'**OMGServ** et grâce au logiciel [FileZilla](https://filezilla-project.org/download.php?type=client) (gratuit)

Une fois dans le système, allez dans le dossier <mark style="color:purple;">/ShooterGame/Content/Mods</mark> où vous trouverez les dossiers 111111111, CrystalIsles, FjordurOfficial, LostIsland, Ragnarok, TheCenter et Valgero ainsi que le fichier 111111111.mod .

Vous aurez également un ou plusieurs autres dossiers ou fichiers ici, **SUPPRIMEZ LES**, ce sont les fichiers qui créent les crashs du serveur au démarrage. Il s'agit tout simplement des mods incomplets qui se sont téléchargés depuis le module automatique **OMGServ et** qui bloquent tout.

Une fois fait, il suffira de vous rendre sur la page d'aide à [l'installation manuelle de mods](ark-installation-mods.md) pour avoir son serveur sans erreurs.
