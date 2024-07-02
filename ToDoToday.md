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
