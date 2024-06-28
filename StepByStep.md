Bonjour à vous :)

Le but de l'exercice est de faire vendredi deux matches de Drone Soccer.
- Un match humain contre humain en réalité mixte
- Un match code contre code.

Sur le chemin, deux modes de jeux seront visités :
- Une course de drones : pour apprendre le travail de groupe
- Un jeu d'obstacles : pour apprendre l'optimisation


----

# Day 1: Créer un circuit à douze

- [ ] Créer un compte GitHub
- [ ] Créér un répertoire vide avec un nom en rapport avec l'exercice
- [ ] Ajouter votre répertoire en utilisant un "pull request" [ici](https://github.com/EloiStree/2024_07_01_HelloUnityDroneSoccerMonsManifest/blob/main/ListOfDroneRacePackageGit.txt): 
- [ ] Créér un projet Unity Vide dit de quarantaine pour votre boite à outil
- [ ] Créér un projet Unity Vide dit de test pour votre project "commun"
- [ ] Cloner votre répertoire dans le dossier Asset de votre projet de quarantaine
- [ ] Dans ce dossier maintenant ajouter un fichier [package.json](https://github.com/EloiStree/2020_05_28_JimmyScreamFPS/blob/master/package.json)
- [ ] Ajouter un prefab "DroneRace_Nom_Prenom" en **alpha numérique**
- [ ] Ajouter dans votre prefab un cube à un position aléatoire entre -32 et 32 dans Unity
- [ ] "Add, Commit, Pull, Push" du répertoire Git
- [ ] Ajouter dans votre projet test votre répertoire grace au project manager de Unity.
- [ ] Aider les étudiants qui n'y arrivent pas pour que les 12 répertoires soit créé et valide.
- [ ] Ajouter les 13 répertoires sur le Git Manifest commun à votre project test
- [ ] Créé une scène Unity dans votre projet test
- [ ] Déposer les 13 préfabs au centre de votre scène.
- [ ] Vous devirez maintenant avoir un projet avec 13 cubes mis à des places aléatoires dans votre scène
- [ ] Faite une pause pour décider de la répartition de l'espace qui fait quel zone.
- [ ] Déplacer votre cube et donner lui un nom prénom à l'espace que vous allez utiliser.
   - [ ] Vous ne pouvez pas utiliser les 8 mètres du centre sur le sol car un terrain de drone soccer y sera.
- [ ] Ajouter au package manager de vos deux projets cet outil: [Race Steps](https://github.com/EloiStree/2024_06_31_DroneRaceStep)
- [ ] Utiliser les assets pour former un cours à 12 sans pour autant travailler ensemble
- [ ] N'oublier pas de push et de pull régulièrement pour voir où en est le niveau.
- [ ] Utiliser "des cubes et des ronds" si vous désirez dronez un peu de level design pas d'asset store pour le moment.
- [ ] Histoire de s'amuser ajouter à votre deux projets cet outil: [Roots of knowledge Drone](https://github.com/EloiStree/2023_02_19_RootsOfKnowledgeDrone)
- [ ] Tester un peu votre scène de test avec le prefab de drone.
  - [ ] Ajouter vos input au besoin
- [ ] Assurez vous que sur tout vos points de passage, il y ai le script "DFlagMono_RootTag"
  - [ ] Assurez vous si vous créé de nouveau prefab avec RootTag que le GUID est différent 
- [ ] Vérifier que les 12 membres de votre group à réussi à faire l'exercice jusqu'ici.
- [ ] Nommez 2 intégrateurs qui se porterons garant de la qualité du circuit et du respect des règles de nommage de votre groupe.

Bonus 8x8 et le dossier resource (si on a le temps):
-  [ ] Créér des préfabs d'une taille de 8x8x8 mètre dans Unity et composer des bouts de circuits
-  [ ] Déposer sur le prefab Drone8x8x8GuidTagMono et Drone8x8x8Mono_WhatToMove
-  [ ] Déposer tout ces prefabs dans le dossier resource de votre boite à outil
-  [ ] Déposer le script Drone8x8x8Tag_Corner ou Drone8x8x8Tag_Line pour notifier quel type de cube c'est.
-  [ ] Utiliser les builder pour généré des circuits


----------

# Day 2: UDP, Websocket, RSA et IID

- [ ] Sur mon ordinateur tourne ce script: [Window Midi Note](https://github.com/EloiStree/2024_05_14_IntegerIndexDateToRemoteControl/blob/main/Python/Gate2Device/Integer_2_WindowMidiNote.py)
- [ ] A l'aide de "ipconfig" sur window, je peux vous afficher l'addresse IP local de mon ordinateur
- [ ] Mes parefeux sont déactivé pour l'exercice
- [ ] A l'aide de Chat GPT, créer un script dans votre language préféré pour envoyé des messages UDP sur 192.168.1.NNN:7005
- [ ] Cela devrait ressembler à ceci [Send UDP](https://github.com/EloiStree/2024_05_17_BasicPythonUdpWebsocketIID/tree/main/SendUDP)
- [ ] On voit vos messsages mais ça ne joue pas de la music.
  - [ ] C'est quoi un bit ?
  - [ ] C'est quoi un byte ?
  - [ ] C'est quoi un tableau de bytes ?
  - [ ] Savez vous compter en binaire ?
  - [ ] C'est quoi la différence en un float et un integer ?
  - [ ] C'est quoi un integer niveau des bits ?
  - [ ] C'est quoi le format "little endian"
  - [ ] Demander à Chat GPT comment envoyé un entier en little endian sur l'address UDP
  - [ ] Envoyé l'entier 1201100121 (12 01 100 121)
    - [ ] Input Type:12   Note:100 Channel: 01  Velocité: 121 
  - [ ] Pourquoi on envoit pas just "Note:10 Velocity:125 Channel:15" ou "N:10 V:125 C:2"
    - [ ] Un entier fait toujours 4 bytes contre 27 et 13 dans les examples données
    - [ ] Vous pouvez le faire tant que vous ne travailler pas avec du Bluetooth
      - [ ] Le Bluetooth est très lent à la transmission => latence et traffic
      - [ ] Example avec XInput Arduino 'AA' [Video](https://youtu.be/uG8gqFLLKuY)
      - [ ] C'est quoi du UART
      - [ ] C'est quoi un Port Série
      - [ ] C'est quoi la Baud Rate
    - [ ] Vous pouvez le faire tant que vous n'avez pas un server AWS, Azure ou Google
      - [ ] Chaque byte vous sera facturé
      - [ ] Chaque Watt vous sera facturé
- [ ] Indirectement Mirror et Photon utiliser la même technique avec le RPC et Command
  - [ ] C'est quoi Mirror ?
  - [ ] C'est quoi UNet
  - [ ] C'est quoi Photon ?
  - [ ] C'est quoi TNet ?
  - [ ] C'est quoi MQTT ?
  - [ ] Tu aurais pas oublier de nous expliquer ce qu'est un TCP ?
  - [ ] C'est quoi la différence entre un TCP et UDP ?
  - [ ] Il y a plus facile à utiliser que le TCP, le websocket
  - [ ] Example de Websocket: les Cloud Var de scratch
    - [ ] Un jeu multijoueur en 5 minutes: [https://scratch.mit.edu/projects/966307753/](https://scratch.mit.edu/projects/966307753/editor/)
    - [ ] Pourquoi les clouds var de scratch son accessible seulement aux utilisateurs "valider" ?
    - [ ] Si vous pouvez envoyé un entier, vous pouvez envoyé du text utf8,
      - [ ] si vous pouvez envoyé un text, vous pouvez envoyé de fichier
         - [ ] si vous pouvez envoyé un fichier, vous pouvez envoyé des images et vidéos
         - [ ] si vous pouvez envoyé du text, vous pouvez aussi faire de l'injection
    - [] Ca leur coute, c'est non sécurisé et ça peu controlabe sans vérification humain
      - [] En gros: "Never Trust the User"
- Pourquoi je vous parle de Websocket ?
  - Avec de l'UDP, vous pouvez m'envoyé un message, mais pour répondre faut que vous ouvriez un port du partfeu à la main.
  - Avec de l'UDP, vous pouvez m'envoyé des messages, mais je ne peux pas couper la connection (vous kick ou vous bannir)
  - L'UDP ne fonctionne pas sur les navigateurs webs !
  - [ ] Avez vous déjà entendu parler de `Port Forwarding`
    - [ ] L'UDP est pratique localement et sur la machine de l'utilisateur
    - [ ] L'UDP est pratique pour communiquer d'un application à un autre sur le même PC
      - [ ] Bien qu'il existe une autre méthode plus efficace les "memory files"
    - [ ] Les Port Fowarding est le fait d'ouvrir un port sur votre routeur et de rediriger les messages vers un port d'un ordinateur ciblé
      - [ ]  C'est par example comme cela que vous pouez héberger des serveurs de jeux: minecraft, battlefield et autres.
      - [ ]  Le problème de cette étape est quel demande des droits d'administrateurs, un savoir faire et est risqué pour votre réseaux.
      - [ ]  C'est pour cela que le "trou" dans le réseaux sera fait par le server héberger du jeu et pas les utilisateurs
      - [ ]  Example: On ne pourra pas demander à Technocité d'ouvrir un port ou de diminuer sa sécurité.
   - [ ] Allons directement dans la pratique.
     - [ ] Je vais héberger un [websocket server](https://github.com/EloiStree/2024_05_17_BasicPythonUdpWebsocketIID/blob/main/SendWebsocket/SendWebsocket.py) sur mon ordinateur
     - [ ] Via Chat GPT généré un websocket client pour m'envoyé des entiers en bytes little endian sur ws://192.168.1.NNN:8765
     - [ ] Notons qu'en réseaux il y a une notion de masque qui permet de n'accepter des messages que d'un zone réseaux
       - [ ] 127.0.0.1 et localhost représent votre ordinateur
       - [ ] 0.0.0.0 représent un address qui vient de n'importe où
     - [ ] Text vs Binaire
       - [ ]  En UDP, vous n'envoyé que du binaire et on peu le traduire en text si on le veut
       - [ ]  En Websocket, vous pouvez notifier que vous envoyé du text ou du binaire
       - [ ]  Dans votre code, envoyé des entier LE en bytes et votre Nom Prénom en text.
     - [ ] J'attends d'avoir 12 nom prénom et un entier le avant de continuer.
     - [ ] Maintenant que je l'ai fait localement avec vous, je vais héberger le code sur le PC chez moi.
     - [ ] Sauf si l'IP public change: ws://192.168.1.NNN:8765
       - [ ] Comment avoir l'address si l'IP public change ?
         - [ ]  Je stock l'IP de mon relay [ici](https://github.com/EloiStree/IP/blob/main/RELAY/HOME_IP.txt)
         - [ ]  Et le websocket de IID (voir plus tard) [ici](https://github.com/EloiStree/IP/blob/main/IIDWS/SERVER.txt) 
     - [ ] Adapter votre code pour pouvoir cibler un server 



