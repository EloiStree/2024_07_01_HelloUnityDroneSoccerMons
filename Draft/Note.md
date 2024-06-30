# Step by step but not corrected / Sans correction orthographique

Bonjour à vous :)

Le but de l'exercice est de faire vendredi deux matches de Drone Soccer.
- Un match humain contre humain en réalité mixte
- Un match code contre code.

Sur le chemin, deux modes de jeux seront visités :
- Une course de drones : pour apprendre le travail de groupe
- Un jeu d'obstacles : pour apprendre l'optimisation


----

# Day 1: Créer un circuit à douze

Main Git: 
- https://github.com/EloiStree/2024_06_31_DroneRaceStep
- https://github.com/EloiStree/2023_02_19_RootsOfKnowledgeDrone

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

# Day 2, matin : UDP, Websocket, RSA et IID Bouger des drones

Main Git: https://github.com/EloiStree/2024_05_11_GateIID_WS_UnityProject

On va faire une course de drones sur un jeu héberger sur Shadow.tech avec votre circuit d'hier


- Connectez vous sur le Discord [Integer Game](https://discord.gg/YK7z8p9v): https://discord.gg/YK7z8p9v
  - Télécharger une "porte" d'entier:  [Gate IID WS Unity](https://github.com/EloiStree/2024_05_11_GateIID_WS_UnityProject) [Release](https://github.com/EloiStree/2024_05_11_GateIID_WS_UnityProject/releases)
    - Si vous aimer le Python: [Gate IID WS Python](https://github.com/EloiStree/2024_05_17_BasicPythonUdpWebsocketIID)
  - Lancer la 'Gate' et laisser la tourner en tache de fond
    - Elle va vous servir à envoyer des entiers en étant authentifier sur un server mutualisé grace à une clé RSA qui vous attribue un "Network ID"
      - On va prendre le temps de comprendre cette phrase (^^' ) Vous inquiétez pas.
  - Créé un projet Unity3D vide pour Android
  - Import the Action Input System de Unity: https://docs.unity3d.com/Packages/com.unity.inputsystem@1.7/manual/index.html
  - Importer une boite à outils pour envoyé des messages UDP: [UDP Thread Sender](https://github.com/EloiStree/2020_11_29_UDPThreadSender)
  - Je vous ai préparé des scripts dont: QuickBytePushMono_SendByteToSoloTarget
  - Convertiser un entier en 4 bytes en format little endian et envoyé les sur la cible 127.0.0.1:3617
  - Vous deviez voir apparaitre des nombres sur Sent et sur Received sur la gate.
  - Envoyé le nombre 123456789 suivit de 987654321. Puis envoyé le nombre -199887766
  - Le drone qui tourne à droit vers le haut comme une toupie c'est vous :)-
  - Envoyé 0 si vous voulez l'arrêter. Suivit de 000010000 pour le faire descendre
    - TY JLH JLV JRH JRV : Drone ID, Left Right Rotation, Down Up, Left Right, Backward Forward
    - 0=0, 01 = -1f, 99 =1f  soont des pourcentages de -1f à 1f (de 01 à 99)
    - -20 tout mes drones
    - -N The N drone que je possède
    - +N Ce drone précisément si je le possède
    - L'idée ici est de compresser les données d'un manette sur 4 bytes
 - Télécharger cette boite à outil: https://github.com/EloiStree/2024_04_07_PushGenericAsIntegerDate.git
   - Celle-ci contient un préfab Gamepad Drone 16
   - Jetez y un coup d'oeil
   - Essayer de relier les deux librairies ensemble pour bouger votre drone dans le jeu
 - Trop facile ?
   - Pendant que je vérifie que tout le groupe arrive à faire l'exercice
   - Regardez deux trois vidéos de joysticks pour Android et ajouter les à votre projet
 - Publier sur Android ?
   - En fonction du temps, on peut vite le faire ou attendre vendredi  

# Day 2, après midi:

Travaillons vos rotations (^-^-)

- Le piège ! C'est le rotation.
- Les bases:
  - [ ] C'est quoi Euler ?
  - [ ] C'est quoi un Quaternion ?
  - [ ] C'est quoi Debug Draw ?
  - [ ] Transform.forward
  - [ ] Quaternion*Forward
  - [ ] Quaternion.LookAt
  - [ ] C'est quoi la commutativité des Quaternions ?
  - [ ] C'est quoi l'angle opposé d'un quaternion ?
  - [ ] Transform.InverseTransform ?
  - [ ] Direction et magnitude
  - [ ] Quaternion.Lerp
- Meilleur conseil de mon professeur de math M. Widar
  - Recenter un problème relativement. [E_RelocationUtility](https://github.com/EloiStree/2021_10_03_EloiGeneralToolbox/blob/main/Runtime/E_RegexUtility.cs)
    - On y perd en performance, mais c'est tellement plus efficace pour comprendre ce que l'on fait.
      - Ramener la rotation sur l'axe zero
      - Dessiner deux trois axes de couleurs
      - Retourner les données à leur origine
      - Je vous montre, mais vous allez vite pratiqué ^^...
-  Ajouter ceci au manifest.json de votre projet de ce matin
```
    "be.eloistree.udpthreadsender": "https://github.com/EloiStree/2020_11_29_UDPThreadSender.git",
    "be.eloistree.downloadserveripfrompage": "https://github.com/EloiStree/2024_06_15_DownloadServerIpFromPage.git",
    "be.eloistree.dronemultistructandparser": "https://github.com/EloiStree/2024_06_25_HelloDroneMultiStructAndParser.git",
    "be.eloistree.generatestorersakey": "https://github.com/EloiStree/2024_04_04_GenereteRsaKeyInUnity.git",
    "be.eloistree.iidwstunnelingrsa": "https://github.com/EloiStree/2024_04_04_UnityServerTunnelingRSAUnity.git",
    "be.eloistree.mirrordronesoccerstartpack": "https://github.com/EloiStree/2024_06_11_HelloMirrorDroneMultiStartPackUnity.git",
    "be.eloistree.pushgenericintegerdate": "https://github.com/EloiStree/2024_04_07_PushGenericAsIntegerDate.git",
    "com.unity.inputsystem": "1.7.0",
    
```
- Dans une nouvelle scène, déposer le prefab: Start Pack (Drag Example Prefab)
  - si le server est lancé, vous deviez avoir un scène avec des drones deux goals circulaires, un balle et deux goals carrés
    - Vous deviez avoir un script nommé: PullOfNetworkFromBytesMono.cs
    - Celui-ci vous donne tout les informations sur la partie en cours :) 
- Sur le serveur est chargé votre niveau de lundi.
  - Charger dans votre projet le même niveau
  - Puis essayer à l'aide de code uniquement de bouger le drone
    - Essayer d'abord sans objectifs, just bouger
    - Essayer d'atteindre un point dans l'espace
    - Essayer de faire le circuit
  - Vous vous sentez d'attaque ;) Bah alors attaquez.
    - Essayer de pousser la boule dans le goal adverse
  - L'attaque c'est trop facile ?
    - Essayer des défendre votre goal en repoussant les drones des autres
- **Attention !!!** Le but aujourd'hui est principalement de pratiquer les rotations.  
Vous avez le reste de la journée pour pratiquer.
On fait un match à la fin du cours.

Le but est vendredi de faire un match en XR 
- une version humain contre humain
- une version code contre code à 12 dans le match.


# Day 3, matin: Mirror ?

Un cours sur Mirror prend plus qu'une demi journée.
Mon but n'est pas de donner un cours sur commment faire des multijoueurs locaux.
Mais se serait dommage de skipper un outils si puissant et open source.

Le but de la matinée est d'explorer ensemble le code.
Et de parler concept.

- Cloner le projet suivant sur votre ordinateur
  - Git Code: https://github.com/EloiStree/2024_06_01_HelloMirrorDroneMulti.git 
  - Nous allons explorer à quoi ressemble un projet Mirror ensemble sans pratiquer directement
  - Comme vous avez cloner le projet, vous devrez pouvoir 

- Pratiquer le NTP sur Mirror ?
  - NTP Native Time Protocole permet de se syncrhoniser entre application à 2-60-500 milliseconds
  - Je vous propose de faire ensemble en live un Gandalf Sax en Mirror pratiquer:
    - Video: https://www.youtube.com/watch?v=BBGEG21CGo0
   

- [ ] C'est quoi un jeu en coop ?
- [ ] C'est quoi un jeu en coop via Steam ?
- [ ] c'est quoi un jeu en coop via Photon Quantum ?
- [ ] C'est quoi Photon ?
- [ ] C'est quoi UNet ?
- [ ] C'est quoi TNet ?
- [ ] C'est quoi la différence entre un jeu en TCP et en UDP ?
- [ ] C'est quoi la différence entre un jeu peer 2 peer et un jeu client server   
- [ ] C'est quoi la différence entre un jeu multijoueur avec confiance sur le client ?
  - [ ] Pourquoi voudrait ton faire confiance au client ?
- [ ] Que propose Unity pour faire du mutlijoueur ?
- [ ] C'est quoi Mirror
  - [ ]  C'est quoi un command ?
  - [ ] C'est quoi un RPC ?
  - [ ] C'est quoi un TargetRPC ?
  - [ ] C'est quoi un SyncVar ?
  - [ ] C'est quoi un Host
    - [] Différence entre un Host et un server ?
  - [ ] C'est quoi un NetworkId ?
  - [ ] C'est quoi un NetworkMono ?
  - [ ] C'est quoi un Player prefab ?
  - [ ] c'est quoi un spawnable prefab ? 

- [ ] Petit exercice Mirror
  - [ ] Je vais créé un projet Git sur GitHub
  - [ ] Cloner le projet sur votre ordinateur
  - [ ] Ajoutons Mirror dans le projet
  - [ ] Ajoutons un Basic NetworkId
  - [ ] Créons un prefab pour votre joueur
  - [ ] Ajoutons un double réseaux pour WebGl
  - [ ] Sur le joueur, ajoutons un script pour pousser des bytes et des integers IID
    - [ ] On regarde si on est sur le client
    - [ ] Si oui, on créé une commande avec un tableau de bytes
    - [ ] On fait pareil pour un entier
    - [ ] Pour premettre au server d'écouter à tout les joueurs, nous allons faire un singleton d'écouter
    - [ ] Nous allons créé un singleton mono pour permettre d'écouter depuis un Unity event.
    - [ ] Crééons une réaction sur le server en fonction des integers que vous m'envoyé.
  - [ ] Sur le joueur ajoutons un script qui me permet d'envoyé des bytes à un joueur spécifique.
  - [ ] Créons un singleton qui permet d'avoir tout les scripts permettant de pusher des bytes
    - [ ] Poussons un struct compresser en bytes à tout les joueurs 
      - [ ] Example un frame de 12 avec le tick date du server utc
  - [ ] Notre but c'est de jouer Gand Alf Sax avec le même timing
    - [ ] Téléchargeons un vidéo de Gand Alf Sax 
    - [ ] Ajoutons dans la scène un prefab avec un vidéo Player
    - [ ] Créons script GandAlfSaxNetworkMono avec un Client RPC start et un var SyncVar
    - [ ] Si le joueur est sur le server c'est le host et l'on set le time de la vidéo
    - [ ] Quand un action arrive, lancer la vidéo attendre 0.1 seconds et demander au client de se synchroniser.
    - [ ] Après 0.6 seconds afficher la vidéo et mettre le volume à N.

  - [ ] Une autre méthode serait de donner un Date NTP depuis de server avec N seconds d'avance
    - L'idée ici est de bypasser le lag et le perte de milliseconds sur le chemain.
    - Utiliser le date NTP pour syncrhoniser l'action sur le PC.
    - Creéons un script NTPActionsNetworkMono sur le joueur
    - Ajoutons un Server NTP string en SyncVar
    - Ajoutons un command pour envoyé une action avec un Date NTP + N Ticks
    - Ajoutons une liste qui ajoute le N Ticks Actions dans la liste.
      - Note:on pourrait avoir deux commands, un Unity Thread Safe et un Side Thread. 
    - Une fois la date dépassée dans le Update envoyé un Unity Event de l'action.
    - Racorder l'évent au délanchement du Gand Alf Sax;
      - Set video as ready to trigger: Load video  , set timing, pause
      - Unpause the vidéo 
  - [ ] Ajoutons un vote, Yes No avec les IID et déclanchons le vidéo quand tout le monde dit Yes.



# Day 3,  Bullet Hell et job système

Je vais vous apprendre à utiliser un des outils le plus puissant de Unity qui est assez simple à utiliser: Les job système.
Celui-ci permet d'exploiter tout la puissance de votre CPU.

Pour cela, nous allons pratiquer dans un jeu de survie.

- Retourner dans le projet d'hier.
  - PullOfNetworkFromBytesMono peu produir des S_LinearProjectilePoolItemCreationEvent
  - C'est des projectiles à éviter avec votre drone.
  - Être toucher vous ramène aux points de départ
  - Le but est de survivre le plus longtemps possible.

Via ce que je vous ai montré:
- Afficher les astéroides à l'écran
- Si vous arrivez à les afficher
  - Pratiquer le fait de détecter de future collision avec votre drone et fait le survivre.
 
Prenez l'exercice d'affichage aux sérieux car il est la base de l'exercice de demain.


# Day 4 Bullet Hell ++ et LOD

L'exercice d'aujourd'hui: pratiquer le job système et les LOD.
Choisissez des techniques d'optimisation dont on vu le matin selon votre niveau.

Le but de l'exercice, travaillez des effets visuels dont le détail change avec la distance.
Permettant d'avoir du beau malgré la présence de milier de projectile.

Il y a deux challenges à cet exercice:
- Arrivé à survivre le plus longtemps dans cette enfer de collisions
- Arrivé à garder son jeu au dessus de 55 FPS le plus longtemps avec des graphiques d'un MVP sur le store.
  - Utiliser Jimmy pour les testes de performances  [(  ^O^) aaaaaaaAAAAHHH](https://github.com/EloiStree/2020_05_28_JimmyScreamFPS)


  
# Day 5 Android XR 

Journée un peu plus chill.

Le but est d'apprendre à publier votre jeu de cette semaine sur les Quests et autres casques disponibles.
L'après midi, l'on testera les casques et le jeu Alyx (si pas déjà fait durant la semaine)

Avant de finir la journée, l'on finira par les deux matches promis en début de semaine.
(Sans les astéroides)





















----------------


# Achive

----------------

Trop long:

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
     - [ ] Je vais héberger un [websocket server](https://github.com/EloiStree/2024_05_17_BasicPythonUdpWebsocketIID/tree/main/SendWebsocket) sur mon ordinateur
     - [ ] Via Chat GPT généré un websocket client pour m'envoyé des entiers en bytes little endian sur ws://192.168.1.NNN:4513
     - [ ] Notons qu'en réseaux il y a une notion de masque qui permet de n'accepter des messages que d'un zone réseaux
       - [ ] 127.0.0.1 et localhost représent votre ordinateur
       - [ ] 0.0.0.0 représent un address qui vient de n'importe où
     - [ ] Text vs Binaire
       - [ ]  En UDP, vous n'envoyé que du binaire et on peu le traduire en text si on le veut
       - [ ]  En Websocket, vous pouvez notifier que vous envoyé du text ou du binaire
       - [ ]  Dans votre code, envoyé des entier LE en bytes et votre Nom Prénom en text.
     - [ ] J'attends d'avoir 12 nom prénom et un entier le avant de continuer.
     - [ ] Maintenant que je l'ai fait localement avec vous, je vais héberger le code sur le PC chez moi.
     - [ ] Sauf si l'IP public change: 'ws://81.240.94.97:4513' 
       - [ ] Comment avoir l'address si l'IP public change ?
         - [ ]  Je stock l'IP de mon relay [ici](https://github.com/EloiStree/IP/blob/main/RELAY/HOME_IP.txt)
         - [ ]  Et le websocket de IID (voir plus tard) [ici](https://github.com/EloiStree/IP/blob/main/IIDWS/SERVER.txt) 
     - [ ] Adapter votre code pour pouvoir cibler un server 
- [ ] Vous arrivez à faire une connection c'est bien... Mais il est où le mot de passe ?
  - [ ]   Pour pouriez stocker un mot de passe sur le server et le donner aux utilisateurs
    - [ ] C'est quoi un SHA256 ? [Tester](https://emn178.github.io/online-tools/sha256.html)
      - [ ] 'Ne stocker jamais les mots de passe sur le server ^^'
      - [ ] Pour vérifier, il lui faudra envoyé sur le réseaux son nom et mot de passe
    - [ ] Une autre solution est de s'accorder sur un [Caesar Cipher](https://www.dcode.fr/chiffre-cesar)
      - [ ] Mais on c'est pas idéal ( encore moi à notre époque avec le machine learning )
    - [ ] On pourrait crypter un message avec un Cipher++ et stocquer le paramètre sur notre ordinateur
      - [ ] C'est le concept d'une clé privé comme pour [AES](https://www.youtube.com/watch?v=O4xNJsjtN6E)
      - [ ] Sa nous permet de crypter et de signer des messages...
      - [ ] Mais je dois avoir la clé chez moi et vous chez vous... Pas idéal
    - [ ] Ce que l'on utilise depuis 1977, c'est le concept de RSA qui utilise une clé public et clé privé
      - [ ] Vous avez une clé privé que vous garder secret et j'ai une clé publique que vous pouvez partager
      - [ ] Ca vous permet d'encrypter des messages que je peux décrypter
      - [ ] Ca vous permet aussi de signer des documments.
        - [ ]   C'est quoi la différence en encrypter et signer ?
          - [ ]   Encrypter = mélanger avec la clé public et Décrypter = réordonner avec un clé privé du destinataire
          - [ ]   Signer = utiliser SHA256 pour créé un petit text basé sur un grand text avec la clé privé ensuit vérifier que ça produit un clé public donné
      - [ ] RSA 512 vs 1024 vs 2048 vs ... Plus la taille et grand plus il est dur à casser
        - [ ] Mais du coup, plus long encrypter et decrypter.
          - [ ]  Ca posse problème si vous voulez un jeu sans latence et sécurisé
        - [ ] Le RSA c'est bien... Mais c'est aussi très complexe à paramètrer.
          - [ ] Et je suis tomber sur cette vidéo la semaine passé : ["Fuck RSA"](https://www.youtube.com/watch?v=lElHzac8DDI)
          - [ ] Il est vrai que c'est pas un sujet simple.
      - [ ] Alternative? Elliptic Curve Cryptography [Wiki](https://en.wikipedia.org/wiki/Elliptic-curve_cryptography)
        - [ ] Beaucoup plus simple à utiliser, mieux protégé , paire de clé public privé ...
        - [ ] C'est bon du coup, on utilise ECC ? Bah, oui et non. Reposer la question dans un décennie
      - Vous le comprenez, c'est un long sujet: https://www.youtube.com/@Computerphile/search?query=key
      - Et sujet qui n'attend que d'être mis à terre avec le machine learning et les calcules quantiques
- [ ] Et donc ... On fait comment pour s'authentifier pratiquement ?
  - [ ]  Je vous proposerai bien un exercice avec ECC mais mes outils sont sur RSA 1024
  - [ ]  Créé un websocket client qui se connect à mon server IID actuel:
    - [ ] URI: ws://81.240.94.97:4501  [IP](https://github.com/EloiStree/IP/blob/main/IIDWS/SERVER.txt)
    - [ ] Nous allons procéder à un "handshake"
    - [ ] En text envoyé 'Hello VOTRE_PUBLIC_KEY_XML_1024'
    - [ ] Il vous retourne un 'SIGNIN:GUID'
    - [ ] Il vous faut extraire le GUID et le signer avec votre clé privé en utilisant SHA256 et pkcs1
    - [ ] Il faut maintenant le retourner 'SIGNED:B64OFGUIDSIGNED'
      - [ ] B64 quoi ? C'est une conversion de bytes en text et de text en byte utilisant 64 charactères 
    - [ ] Le server va vérifier votre signature depuis le text
    - [ ] Si c'est valide, il vous retourne un message 'RSA:Verified' et 'IndexLock:-N'
      - [ ]  RSA, confirme la find du hanshake. vous avez prouvez que vous être le proriétaire de la clé privé
      - [ ]  IndexLock c'est votre index sur le server -N (vous êtres un guest) +N (votre clé public est sur le server)
  - [ ] Je survole la matière pour un simple raison: c'est compliqué ( ^^')
    - [ ] C'est la raison même de mon project actuel Integer Games et les IID
      - [ ] Créé un serveur mutualisé pour éviter d'avoir à apprendre à héberger de server
      - [ ] Créé un format compresser pour partager des évènements ou de petites données d'ordinateur en ordinateur
    - [ ] J'ai donc des codes prêtes pour vous
  - [ ] N'oubliez pas que la raison de voir un sujet si chiant avec vous plutot que de faire du jeu.
     - C'est car j'ai du les utiliser de nombreuses fois dans ma carrière voir ["Pouquoi ce workshop"](https://github.com/EloiStree/2024_07_01_HelloUnityDroneSoccerMons/issues/33)
     - C'est
        - "très débile de mettre un server de mail dans un jeu fruit ninja"
        - "c'est très peu réutilisable de mettre le code d'un kinect dans un jeu directement"
        - "Les jeux hors store sont très souvent composé de plusieurs ordinateurs locaux sans être un multijoueur"
        - "Vous aurez besoin de communiquer avec un hardware et ils vous faudra des applications dédiées hors du jeu"
        - "beaucoup d'API fonction avec des portes en Websocket. Example: LM Studio"
      
- [ ] Les gates, Tunnel et Cloud Gaming
  - [ ] Connaissez vous [Shadow ?](https://support.shadow.tech/fr/articles/introduction-with-shadow-pc-gaming/install-shadow-on-android-tv/64e310046593fd01eb5e826e)
  - [ ] Connaissez vous [Modl.ai](https://modl.ai) ?
  - [ ] Connaissez vous ce qu'est le [multiboxing](https://www.youtube.com/@eloistreeraw/search?query=multiboxing) ?
  - [ ] Avec ce que l'on a étudier, comment ferriez vous pour multiboxer 50-500 AI sur des ordinateurs dans le cloud ?
  - [ ] Sachant que vous ne pouvez pas ouvrir les portes ou changer la sécurité du réseaux et de la machine
  - [ ] C'est ce que l'on va faire avec Mordhau :) puis avec notre jeu de drone.
- [ ] Créé un pr

