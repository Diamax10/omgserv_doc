---
description: Tel est la question.
---

# Pterodactyl ou PufferPanel ?

> C'est un sujet qui peut faire débat chez certains. Vous êtes plutôt Pterodactyl ou plutôt PufferPanel ? Ou bien tout simplement perdu ? Ça tombe bien, aujourd'hui ce sujet est fais pour vous ... les personnes perdues.

## Pterodactyl

### Historique

Parlons de ce magnifique projet qu'est Pterodactyl. Sa première version [beta sortie en 2016](https://github.com/pterodactyl/panel/releases/tag/v0.1.0-beta) a suscité beaucoup d'engouement auprès des administrateurs de serveur Minecraft. À cette époque le marché des panels de gestion de serveurs Minecraft était dominé par Multicraft.

Ce dernier était l'un des meilleurs, regroupant toutes les fonctionnalités nécessaires pour la bonne gestion de son serveur, avec un panel épuré et tout cela de manière sécurisé avec un daemon capable d'être installé sur chacun des noeuds facilement. Mais toutes ces fonctionnalités avaient un prix, une dizaine d'euros par mois environ, cela dépendait du nombre de noeud. Il existait des versions gratuites et open source de panels de gestion similaire mais aucuns n'étaient satisfaisant réellement.

C'est là qu'est arrivé, Pterodactyl. Un projet open source porté par [Dane Everitt](https://daneeveritt.com), essayant de regrouper un maximum de fonctionnalité possible. L'un des avantages de ce nouveau panel est la conteneurisation des serveurs de jeux grâce à Docker. Ainsi, il est possible de gérer précisemment chaque ressources allouées aux serveurs \(RAM, CPU, stockage\) et les permissions d'accès pour chaque utilisateur. Grâce à cela, tout était séparé de manière sécurisé entre la machine hôte et les serveurs.

Pendant 5 ans, le panel était en développement en version beta. Ceci a permis aux développeurs d'améliorer le panel, d'avoir beaucoup \(voire énormément\) de retours utilisateurs et de bien comprendre leurs attentes. 5 ans après le lancement du projet, en 2020, la version 1, stable, est enfin annoncée, comprenant un nouveau design, des nouvelles technologie en matière de développement pour le panel et daemon des noeuds maintenant appelé "Wings".

### v1.0

Rédaction en cours ...

## PufferPanel

### Historique

PufferPanel est un projet qui [a vu le jour en 2013](https://github.com/PufferPanel/PufferPanel/releases/tag/v0.4-beta) et est tout simplement [le parent de Pterodactyl](https://gist.github.com/LordRalex/cee5ec702b68e90f36958b4026d52f88).

### Aujourd'hui v2.0

## Comparaison

### Avantages de Pterodactyl

* Sous Docker \(sécurité, séparation, gestion ressources\)

### Inconvénients de Pterodactyl

* Sous Docker \(fonctionne pas toujours ex: OpenVZ fonctionnalités limitées\)
* Demande des connaissances en Linux pour l'installation

### Avantages de PufferPanel

* Pas sous Docker
* Simple à installer

### Inconvénients de PufferPanel

* Pas sous Docker

## Conclusion

Ça dépend, parfois l'un est mieux et parfois c'est l'autre. Pour quelqu'un qui n'y connais rien je dirai PufferPanel, pour ceux sous des VPS OpenVZ / LXC PufferPanel sinon Pterodactyl.

