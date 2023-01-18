---
description: >-
  Dans ARK : Survival Evolved plus que sur n'importe quel jeu, la configuration
  peut prendre des jours et des jours pour en faire le tour ! Voici une petite
  page pour vous aiguiller
---

# Informations et utilisation des fichiers configuration

## Informations générales

Tout d'abord, sachez qu'il y a dans votre serveur deux fichiers qui vous seront très probablement utiles.

Pour y accéder, rendez vous dans l'onglet **WebFTP** d'**OMGServ**, puis rendez vous dans le dossier <mark style="color:purple;">/ShooterGame/Saved/Config/LinuxServer/</mark>

Vous y trouverez alors les fichiers <mark style="color:orange;">Game.ini</mark> et <mark style="color:orange;">GameUserSettings.ini</mark>, ils seront déjà bien remplis après avoir rempli les règles dans l'onglet **Propriétés** d'**OMGServ**, mais il y a moyen de les remplir à la main pour rajouter des règles personnalisées.

Chaque règle dans ces fichiers fonctionnent s'ils sont sous la bonne balise, elles sont reconnaissable car c'est les seules lignes des fichiers qui sont entre crochets.

## Game.ini

### Informations

C'est un fichier que vous utiliserez assez rarement, il touche habituellement les valeurs d'expériences gagnées sur le serveur et des informations serveurs comme le nombre de joueurs spectateurs, ou encore les modes de jeu.

### Utilisations

####

#### Augmentation des statistiques des joueurs et des créatures

Si vous souhaitez augmenter la valeur que prend votre personnage ou les créatures en leur attribuant des points, cette règle est pour vous.

Voici la table des statistiques.

* 0 -> Change la **Vie**
* 1 -> Change la **Stamina**
* 2 -> Change la **Torpeur**
* 3 -> Change l'**Oxygène**
* 4 -> Change la **Faim**
* 5 -> Change la **Soif**
* 6 -> Change la **Température** (N'a l'air de rien changer dans le jeu)
* 7 -> Change le **Poids**
* 8 -> Change le **Multiplicateur de Dégâts**
* 9 -> Change de **Multiplicateur de Vitesse**
* 10 -> Change la **Résistance à la Température**
* 11 -> Change le **Multiplicateur de Vitesse de craft**

Plusieurs lignes sont paramétrables sous la balise <mark style="color:orange;">\[/script/shootergame.shootergamemode]</mark>, sachant que le <mark style="color:red;">X</mark> dans chaque ligne doit être modifié par les chiffres de la table de statistiques ci dessus pour préciser quelle statistique modifier. Le chiffre <mark style="color:green;">Y</mark> est à modifier selon la multiplication qu'on souhaite appliquer à la statistique (attention c'est une multiplication, les valeurs montent et descendent très vite !)

Pour modifier les statistiques gagnées par les joueurs, voici ce qu'il faut renseigner :

* **PerLevelStatsMultiplier\_Player\[**<mark style="color:red;">**X**</mark>**]=**<mark style="color:green;">**Y**</mark>

Pour modifier les statistiques gagnées par les créatures sauvages :

* **PerLevelStatsMultiplier\_DinoWild\[**<mark style="color:red;">**X**</mark>**]=**<mark style="color:green;">**Y**</mark>

Pour modifier les statistiques gagnées avec les niveaux bonus lors de l'apprivoisement :&#x20;

* **PerLevelStatsMultiplier\_DinoTamed\[**<mark style="color:red;">**X**</mark>**]=**<mark style="color:green;">**Y**</mark>

Pour modifier les statistiques gagnées à partir du moment où la créature est apprivoisée :&#x20;

* **PerLevelStatsMultiplier\_Tamed\_Add\[**<mark style="color:red;">**X**</mark>**]=**<mark style="color:green;">**Y**</mark>

Puis enfin pour modifier les statistiques qui font d'un bébé issu d'un oeuf est meilleur qu'une créature apprivoisé au même niveau

* **PerLevelStatsMultiplier\_DinoTamed\_Affinity\[**<mark style="color:red;">**X**</mark>**]=**<mark style="color:green;">**Y**</mark>

####

#### Augmentation des stacks des objets

Si vous trouvez que la pile d'objet en jeu est trop petite ou trop grande vous pouvez la modifier, mais armez vous de courage, vous ne pourrez modifier à la main qu'un stack d'objet à la fois ! Sachez quand même que certains mods pour les stacks sont simple à installer, bien plus que de toucher à ces lignes de codes, si vous vous y intéressez, utilisez notre page pour [installer un mod sur votre serveur](ark-installation-mods.md) en vous renseignant sur les mods de stacks.

Ces lignes sont paramétrables sous la balise <mark style="color:orange;">\[/script/shootergame.shootergamemode]</mark>

Vous y trouverez deux choses à renseigner, le <mark style="color:red;">CodeItem</mark> est le code de l'objet, et la quantité <mark style="color:red;">X</mark> la taille de la pile (ou du stack) que vous souhaiter avoir.

* **ConfigOverrideItemMaxQuantity=(ItemClassString="**<mark style="color:red;">**CodeItem**</mark>**",Quantity=(MaxItemQuantity=**<mark style="color:red;">**X**</mark>**, bIgnoreMultiplier=true))**

Au lieu de tout faire à la main, vous pouvez copier directement les codes depuis ce [lien](https://pastebin.com/zNfNpMAv), il vous suffit de faire sur votre clavier Ctrl+F et de chercher le nom de l'objet en anglais, vous le trouverez vite. **Néanmoins attention** ce [lien](https://pastebin.com/zNfNpMAv) est fait pour que les stacks soient démesurés, faites attention et modifiez le nombre en conséquence.&#x20;

####

#### Augmentation du nombre de structure sur une selle-plateforme

Sous la balise <mark style="color:orange;">\[/script/shootergame.shootergamemode]</mark> vous pouvez modifier la règle suivante, ou le <mark style="color:red;">X</mark> représente la multiplication du nombre de structure : Les selles du jeu de base sont limitées à **32**, donc un multiplicateur de **2** laissera une limite de **64**, un multiplicateur de **10** laissera une limite de **320**, etc...&#x20;

Les selles modées ne sont pas toujours sur une base de 32, pour éviter les abus, veuillez vous référer au chapitre pour [augmenter ou limiter le nombre maximum de structure sur une selle](informations-et-utilisation-des-fichiers-configuration.md#augmenter-le-nombre-maximum-de-structures-sur-une-selle-plateforme).

* **PerPlatformMaxStructuresMultiplier=**<mark style="color:red;">**X**</mark>

####

#### Augmenter la vitesse de pousse des champs

Sous la balise <mark style="color:orange;">\[/script/shootergame.shootergamemode]</mark> vous pouvez rajouter et modifier la règle suivante, où <mark style="color:red;">**X**</mark> représente le multiplicateur de pousse des champs, 1 est la valeur de base, plus le nombre est grand plus les plantes pousseront vite.

* **CropGrowthSpeedMultiplier=**<mark style="color:red;">**X**</mark>

####

#### Modifier la rareté des loots des balises

Sous la balise <mark style="color:orange;">\[/script/shootergame.shootergamemode]</mark> vous pouvez rajouter et modifier la règle suivante, où <mark style="color:red;">**X**</mark> représente le multiplicateur de récompenses, 1 est la valeur de base, plus le nombre est grand plus les récompenses seront rares/nombreuses.

* **SupplyCrateLootQualityMultiplier=**<mark style="color:red;">**X**</mark>

## GameUserSettings.ini

### Informations

Contrairement au premier fichier, vous risquez de plus souvent toucher à celui là, il est très utilisé pour modifier quasiment la totalité de la configuration du serveur.

### Utilisations

####

#### Difficulté et niveau max des créatures

Sur toutes les cartes, il est conseillé de jouer avec la difficulté à 1 dans les **Propriétés** d'**OMGServ**, ce qui fait que les loots sont maximum et le niveau des créatures est également maximum. Néanmoins sur certaines cartes comme The Island, le niveau maximum des dinosaures est de 120.

Pour maximiser les chances d'avoir un serveur avec des niveaux équilibrés ou des dinos plus hauts niveaux, deux choses à faire :&#x20;

* Sous la balise <mark style="color:orange;">\[ServerSettings]</mark> vérifiez qu'il y a la règle <mark style="color:purple;">DifficultyOffset=1</mark>, et rajoutez sur une nouvelle ligne la règle <mark style="color:purple;">OverrideOfficialDifficulty=5.0</mark>, ce qui force les créature à avoir un niveau multiple de **5**, et mettra le niveau maximum des créatures apprivoisables à **150**, le niveau des créatures dans les caves ou dans les arènes de boss peuvent dépasser ce nombre.
* Installer le mod [Better Spawn](https://steamcommunity.com/sharedfiles/filedetails/?id=2064588662), qui fait en sorte que le niveau des créatures soit complètement aléatoire, alors que dans la plupart des cas le jeu priorise les créatures bas niveau.

####

#### Augmenter le nombre maximum de structures sur une selle-plateforme

Sous la balise <mark style="color:orange;">\[ServerSettings]</mark> vous pouvez modifier une ligne où <mark style="color:red;">**X**</mark> est le nombre de structure maximum que la selle peut supporter, cette règle existe car certains mods ont des selles avec des capacités en structures beaucoup plus élevées, cette règle permet donc d'éviter de dépasser une certaine valeur limite en structures :&#x20;

* **MaxPlatformSaddleStructureLimit=**<mark style="color:red;">**X**</mark>
