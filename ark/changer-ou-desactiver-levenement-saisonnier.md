---
description: >-
  Marre des dinosaures tout en couleurs ? Envie de profiter des bonus de
  reproduction de l'évènement de la Saint Valentin ? Cette page d'aide est faite
  pour vous !
---

# Changer ou désactiver l'évènement saisonnier &#x20;

## Informations

Vous le savez probablement, il existe dans ARK : Survival Evolved de nombreux évènements qui s'activent automatiquement à certains moments dans l'année, comme Noël, Halloween... la liste complète est disponible sur certains [sites communautaires](https://ark.fandom.com/wiki/Events).  &#x20;

Ces évènements apportent pleins de choses, comme des récompenses à trouver dehors, des aides pour les apprivoisements, de reproductions, de l'expérience et des dinosaures multicolores.



## Modifier ou retirer l'évènement

Pour modifier ou retirer l'évènement, il vous suffira de vous rendre dans les fichiers du serveur, et pour cela vous devrez passer par **WebFTP** :&#x20;

Depuis l'onglet **WebFTP** d'**OMGServ**, rendez vous dans le dossier suivant :  <mark style="color:purple;">ShooterGame/Saved/Config/LinuxServer</mark>

Vous y trouverez le fichier <mark style="color:orange;">GameUserSettings.ini</mark>, ouvrez le et cherchez <mark style="color:orange;">\[ServerSettings]</mark>, qui devrait être la toute première ligne.

Il vous suffira de rajouter une ligne en dessous selon l'évènement que vous voulez, mais attention, les majuscules doivent être respectées :&#x20;

* **ActiveEvent=vday** (Pour l'évènement de la Saint Valentin)
* **ActiveEvent=Easter** (Pour l'évènement de Pâques)
* **ActiveEvent=birthday** (Pour l'évènement d'Anniversaire)
* **ActiveEvent=Summer** (Pour l'évènement d'été)
* **ActiveEvent=FearEvolved** (Pour l'évènement d'Halloween)
* **ActiveEvent=TurkeyTrial** (Pour l'évènement de Thanksgiving)
* **ActiveEvent=WinterWonderland** (Pour l'évènement de Noël)
* **ActiveEvent=None** (Pour désactiver les évènements)&#x20;



## Retirer les dinosaures multicolores

Un dernier détail pour ceux qui décident de jouer sans évènements pour retrouver des dinosaures de couleurs normales, retirer l'évènement va empêcher ces dinosaures de couleurs vives d'apparaître, mais ceux déjà créés resteront là ! Pour les retirer deux solutions s'offrent à vous :&#x20;

* Les tuer, c'est barbare et long quand on imagine la quantité de créatures disponible sur la carte, mais la technique fonctionne.
* Utilisez les commandes : simple et efficace. Il suffira d'appuyer sur touche Tab pour ouvrir la console, tapez la commande "enablecheats MotDePasseAdmin" en renseignant votre mot de passe administrateur a la place de MotDePasseAdmin, puis "cheat DestroyWildDinos" en respectant l'orthographe, les majuscules et les espaces. Toutes les créatures sauvages disparaitront et laisseront place aux nouvelles créatures qui apparaitront sans couleurs vives d'évènements.
