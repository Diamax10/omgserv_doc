---
description: >-
  Parfois les mises à jour des moteurs de serveur peuvent mettre du temps à être
  implémentés par le support, ce tutoriel vous montre comment installer sa
  propre version de Paper ou autres !
---

# Utiliser sa propre version de Paper

### Base

* Commencez par faire une sauvegarde de votre serveur si vous souhaitez réimporter vos fichiers plus tard ~~ou garder des souvenirs~~ nous avons fait un super tutoriel sur ça [ici](../omgserv/sauvegarde-et-restauration.md).
* Téléchargez le fichier .jar de votre moteur de serveur, pour nous ici ça sera Paper qui est disponible en téléchargement sur le site officiel [papermc.io](https://papermc.io/downloads).

{% hint style="info" %}
Pour télécharger une ancienne version de Paper, il faut cliquer sur le bouton "Legacy" en bas de la page et répondre "Non" à toutes les questions.&#x20;

En répondant "Non" à toutes ces questions vous vous engagez à ne pas recevoir de support de la part de Paper car ces versions **sont anciennes** et plus supportées par Paper.
{% endhint %}

* Réinstallez votre serveur en OpenMod, pour cela dans le menu à gauche allez dans "Réinstallation" puis sélectionnez "OpenMod".
* Glissez le fichier .jar téléchargé précédemment dans la zone prévue à cette effet et attendre que tout se télécharge bien ... cela dépend de votre connexion internet.
* Cliquez ensuite sur "Installer en OpenMod", une fenêtre s'ouvre vous invitant à sélectionner un "JAR de démarrage", prenez le fichier .jar que vous venez de télécharger.
* Cliquez sur "Continuer".
* Allez ensuite dans la menu "Propriétés" (toujours à gauche), puis à droite vérifiez la version de Java sélectionnée.
  * Pour les versions en dessous de 1.16 sélectionnez **Java 8**,
  * Pour la 1.16 sélectionnez **Java 11**,
  * Pour la 1.17 sélectionnez **Java 16**,
  * Pour la 1.18 sélectionnez **Java 17**.
* N'oubliez de sauvegarder vos modifications en bas de la page.
* Et voilà, vous avez installé votre propre version de moteur de serveur :partying\_face:
* Vous pouvez démarrer votre serveur si vous le souhaitez.

### Compléments

#### Restauration de sauvegarde

Si vous aviez fait une sauvegarde de votre serveur précédemment vos pouvez la restaurer pour retrouver vos fichiers d'avant. Cependant faites attention, si vous aviez des plugins ou des mods, il se peut qu'ils ne soient plus compatible avec la nouvelle version de votre serveur.

#### Mise à jour ou changement de version

À tout moment vous pouvez mettre à jour ou changer le fichier .jar. Pour cela, téléchargez le fichier .jar que vous souhaitez mettre puis dans le FTP, mettez le fichier .jar à la racine. Ensuite dans le menu "Dashboard" dans l'encart "Type serveur" puis "Version" cliquez sur le bouton "Changer" vous devriez voir votre fichier sous la catégorie "OpenMod", vous avez juste à le sélectionner et à "changer de version".
