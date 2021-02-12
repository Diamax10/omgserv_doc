---
description: >-
  Parce que tout le monde n'a pas les compétences de créer un serveur Minecraft
  en ligne de commande, ce script vous permettra de le faire facilement !
---

# Script automatique de création d'un serveur Minecraft

1- Le système d'exploitation Debian 10 \(Buster\) est obligatoire, l'accès root est facultatif, pour réinstaller votre VPS, dirigez vous sur votre panel onglet "réinstallation".

2- Connexion au VPS via le protocole SSH, un outils type Putty est recommandé \(pour Windows\), vos informations de connexion vous sont envoyées par mail, n'oubliez pas de vérifier vos spams. Une fois ces informations récupérées, connectez-vous à votre VPS.

3- Collez cette ligne de commande dans votre terminal et appuyez sur la touche entrée :

```bash
sudo wget -P /opt https://github.com/zendrique/mc-script/releases/download/1.4/boot.sh && sudo bash /opt/boot.sh
```

_\(note : clique droit pour coller dans un terminal :smirk:\)_

4- Suivez les instructions et répondez aux questions demandées.

À noter : pour vous connectez à votre VPS via un client de type Filezilla ou WinSCP, vous devez utiliser le protocole SFTP, qui, pour faire simple, est la même chose que le protocole FTP.

Pour vous connecter en SFTP : En nom d'utilisateur et mot de passe vous devez renseigner les même que utilisés pour vous connecter en SSH et utiliser le port 22

