  

# 1 | [#Reserver](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/1)  

  

   

  

-----------------------------------------  

  

# 2 | [2024_07_01: Git Package](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/2)  

  

 # To Do Today
-  

# Draft links
- https://github.com/EloiStree/HelloUnityPackage/wiki


# Brouillons d'exercice:

## Exercice 1
- Suivant un package droner d'un drone dans une sphère de 20 cm.
  - Créé un dossier dans Unity avec votre propre format de drone
  - Déposer un script de tag sur le prefab de votre drone et placer le dans le dossier ressource
  - Décorer le dossier comme si vous vouliez le publier sur un magasin Unity
  - Publier le sur GitHub et fait un pull request sur le projet git manifest du groupe
-  Utiliser le Git manifest du groupe pour créé une piscine de drone à utiliser dans Unity3D

## Exercice 2
- Importer un package de circuit pour drone dans Unity.
  - Fait un circuit sur une distance de 16x16x16
  - Tag le point d'entrée et le point de sortie
  - Tag le préfab du circuit et placer le dans Resource
  - Placer le sur Github et ajouter le au manifest de groupe.
 
## Fin de l'exercice  
 Importer le circuit d'autres étudiants dans votre manifest et fait un tour avec votre drone en solitaire.
  
  

  

-----------------------------------------  

  

# 3 | [2024_07_02: Websocket and Rotation](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/3)  

  

 
# Brouillons d'exercice:

## Exercice 1
- Via un websocket client en C#
  - Apprendre à ce connecter à au websocket server (server fournir, voir iMMo Relay)
  - Apprendre à envoyé un message et en recevoir 
  - Apprendre à envoyé des bytes
  - Apprendre à signer un message avec RSA (skip si niveau programmation pas assez élever)
  - Envoyé un entier en bytes reposition le drone au point de départ du circuit.
  - Envoyé un entier dans le format de iMMo bouge le drone sur un écran à 12 joueurs.
  
## Exercice 2
Exercice de "TAS", interdit d'utiliser des manettes dans cette execice.
- Junior: Via un circuit construit avec les packages du jour avant.
  - Apprendre à bouger et faire tourner un drone en solo
- Medior: Via un circuit dynamique des packages du jour avant.
  - Apprendre à faire la course avec le drone en solo.
- Expert: Apprendre à faire la course avec le drone en mode acrobatique 

Le but est de pratiquer les rotations d'un object dans l'espace.   

  

-----------------------------------------  

  

# 4 | [2024_07_03: Mirror and Job System](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/4)  

  

 # Brouillons d'exercice:

## Exercice 1
- Apprendre à recevoir des données du server Mirror en utilisant un package.
  - Rejoindre le server de jeu avec le code websocket d'hier 
  - Via un NativeArray d'entier, trouver l'index de son drone
  - Via cette index, trouver les informations de son drone.
  - Via la position et la rotation du drone sur le server continuer l'exercice d'hier

## Exercice 2
- Apprendre à dessiner un triangle avec un position et une rotation dans un Mesh Unity hors ligne
- Apprendre à bouger ce triangle à partir d'un Vector3 et d'une rotation
- Apprendre à créé un job qui affiche des triangles depuis un group de Vector3 et de Quaternion
- Via le native array avec les informations du drone fournit par Mirror afficher tout les joueurs  et les "bots" dans la partie
- Exercice modéré: Créé une continuité entre les frames réseaux reçu.
- Exercice expert: prédire la continuité de la frame suivant  

  

-----------------------------------------  

  

# 5 | [2024_07_04: LOD and Optimisation](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/5)  

  

 
# Brouillons d'exercice:

## Exercice 1
- Via le job system déterminer la distance entre un drone dans l'exercice d'hier et ça présence dans la camera.
- Via le job system déterminer l'utilisation d'une pool de préfab.
- Utiliser l'outil de LOD de Unity sur c'est préfab
- Si le drone est à porté, utiliser le modèle 3D de l'étudiant correspondant à son identifiant dans le native array.
  - Modèle par défaut si pas identifier
- Niveau expert, choisissez un de ses sujets: 
  - Créé un imposteur pour les drones au loin
  - Utiliser le Draw Mesh pour tout les drones à moyen portée 
  - Faire une transition entre Imposteur, Draw Mesh, une piscine d'objet et du LOD.  

  

-----------------------------------------  

  

# 6 | [2024_07_05: Android XR and Open XR](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/6)  

  

 # Casque présent:
Par Technocité:
- [MetaQuest Pro](https://www.google.com/search?q=meta+quest+pro)
- [Pico 4](https://www.google.com/search?q=pico+4)
- [HTC VIVE XR Élite](https://www.google.com/search?q=HTC+Vive+XR+Elite)
- [HTC VIVE Pro 2](https://www.google.com/search?q=HTC+Vive+Pro+2)
- [Pimax Crystal](https://www.google.com/search?q=pimax+crystal)
- [Oculus quest 2](https://www.google.com/search?q=meta+quest+2)

Par Eloi:
- [Quest 1-2-3](https://www.google.com/search?q=Quest+1+2+3+headset+vr)
- [Oculus Rift CV1](https://www.google.com/search?q=oculus+rift+CV1)
- [Lynx R1](https://www.google.com/search?q=Lynx+R1)
- [Homido Mini (^^'  )](https://www.google.com/search?q=homido+mini)


# Brouillons d'exercice:

## Exercice 1
- Avec Quest pour les juniors et autres caques pour les experts. Créé un projet avec un Cube tournant via Unity3D.
- Junior: Utiliser juste la VR sur PC sans builder sur Android.
- Medior: Faire l'exercice avec des casques hors cours (non Quest).
- Expert: Utiliser le code de Meta Phanto pour en faire une application de réalité Mixed
- Expert, Open source: utiliser le Lynx R1

## Exercice 2

- Ajouter le code d'un drone en solo et utiliser le Input System de Unity pour le bouger.

## Exercice 3

- Essayer de faire tourner le code de cette semaine dans un casque de VR
  - Dupliquer votre projet de cette semaine 
  - Essayer d'installer Open XR dans votre projet non VR et de le faire tourner
  - Expert: fait tourner le projet en réalité Mixed.
  - Expert plus: Explorer XRToolkit 2
  

  

-----------------------------------------  

  

# 7 | [2024_07_16: Hello XR and Meta Quest](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/7)  

  

 
# Brouillons d'exercice:

## Exercice 1

- En groupe, installer un à deux jeux pour le casque donné.
- Passer de group en groupe dans le but de tester au moins deux casques différents.

# Exercice 2
- Groupe selon les Quests présent dans la formation.
- Installer SideQuest sur votre machine
- Via SideQuest installer un des jeux proposés
- Via SideQuest, connecter votre PC à votre ordinateur par Wifi, ou par cable, dans le but de voir ce les autres membres du groupe.
- Via SideQuest changer d'application sur le Quest pendant qu'un autre élève joue.
- Via OBS pour ceux qui connaissent, enregistré le playthrough 



  

  

-----------------------------------------  

  

# 8 | [2024_07_17: Package Manager for Level Design and XR](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/8)  

  

 
# Brouillons d'exercice:

## Exercice 1

- Avec le casque que vous avez, créé un projet Unity de réalité mixed avec un cube qui tourner
- Essayer de le builder sur le casque
- Expert: assurez vous que le jeu tourne en réalité mixed
- Expert: Utiliser vos compétences acquis pour ajouter un décors volant de 16x16x16 max.

## Exercice 2
- Via un package donné qui est le meme qu'ont reçu  les développeurs créé un case de 16x16x16 avec un level design facile, medium, difficile.
- Avant de commencer, prenez le temps en groupe de 12 de vous concertez dans le but de faire une carte global avec des cases de 16x16x16
- Créé un à plusieurs niveaux et baliser les prefabs de script tag
- Via GitHub publier votre package dans le format du package manager.
  - Pour un level static:
    - Les prefabs de votre level est en 0x0x0 et la carte fait maximum 256x256x256 de distance. 
  - Pour un level dynamique: le level doit être sauver dans un dossier Resources.

Durant l'exercice, vos package seront recharger tout les 10 minutes et jouer par le code des développeurs si tout c'est bien passé la semaine d'avant.

  

  

-----------------------------------------  

  

# 9 | [2024_07_18: XR and the industrie](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/9)  

  

 # Brouillons d'exercice:

## Exercice 1
- En groupe, de 3 créé un pecha kucha basé sur des recherches internet dans le google slide partager au groupe.
  - avec le top 9 des meilleurs applications de réalité mixed
  - avec le top 9 des meilleurs mechanisms XR qui vous ont impressionné
  - Finniser le slide avec un 1 app et un mécanisme qui si vous deviez en code un, ce serait ça.
- Si il y a doublons à 15h30, les sides sont retiré 
- A 16h, les quatres groupe présent leur slide. 


  

  

-----------------------------------------  

  

# 12 | [Topic, Guide: Cool guide about use of Coroutine and MoveNext](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/12)  

  

 https://web.archive.org/web/20120713001629/http://www.altdevblogaday.com/2011/07/07/unity3d-coroutines-in-detail/  

  

-----------------------------------------  

  

# 10 | [Topic: Casque disponible durant la formation](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/10)  

  

 # Casque présent:
Par Technocité:
- [MetaQuest Pro](https://www.google.com/search?q=meta+quest+pro)
- [Pico 4](https://www.google.com/search?q=pico+4)
- [HTC VIVE XR Élite](https://www.google.com/search?q=HTC+Vive+XR+Elite)
- [HTC VIVE Pro 2](https://www.google.com/search?q=HTC+Vive+Pro+2)
- [Pimax Crystal](https://www.google.com/search?q=pimax+crystal)
- [Oculus quest 2](https://www.google.com/search?q=meta+quest+2)

Par Eloi:
- [Quest 1-2-3](https://www.google.com/search?q=Quest+1+2+3+headset+vr)
- [Oculus Rift CV1](https://www.google.com/search?q=oculus+rift+CV1)
- [Lynx R1](https://www.google.com/search?q=Lynx+R1)
- [Homido Mini (^^'  )](https://www.google.com/search?q=homido+mini)  

  

-----------------------------------------  

  

# 14 | [Topic: Drone Racing Shape](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/14)  

  

 ![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/2687d116-6184-4251-865d-8b1b658816f6)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/4d8730fb-d8d3-4839-9a14-5a6f83d184b6)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/00c54efc-2df8-4509-b462-9bbc40b090df)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/439cebcd-53f2-4403-9528-0ffcf2b65cb1)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/f6d2f343-1e0f-4e4a-9905-89c17176e188)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/a3335650-594a-4b40-bbb4-f65d788a1b6f)


![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/ea014a2e-a66b-4625-8585-52ab4063aaec)
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/assets/20149493/e78c8f23-e4f3-4348-bd5c-207291b5e26b)

  

  

-----------------------------------------  

  

# 13 | [Topic: June 2024 Meta Presence tool ](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/13)  

  

 Git ignore: https://www.toptal.com/developers/gitignore/api/unity
Git: https://github.com/EloiStree/HelloVR_June2024
  

  

-----------------------------------------  

  

# 15 | [Topic: June 2024 Open XR ToolKit3 on Unity3D](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/15)  

  

   

  

-----------------------------------------  

  

# 11 | [Topic: Use manifest to sync package on the same project.](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneMons/issues/11)  

  

 During this workshop, we are going to work indirectly with 24 students (12 Dev, 12 Game Designer)

To synchronise all this work, I used Google Sheet in the previous project, Magic Door 24:
[![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/assets/20149493/a989b9b2-1e6f-4e87-8e40-61d76be77cb0)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRI-M60nMVqr8Y9U5JUmLPagetZSnvPIgGvUH9k-_SpExI79eswPicqGHH7coprFGV8HFQ6Zp0HesqK/pubhtml)  
[https://docs.google.com/spreadsheets/d/e/2PACX-1vRI-M60nMVqr8Y9U5JUmLPagetZSnvPIgGvUH9k-_SpExI79eswPicqGHH7coprFGV8HFQ6Zp0HesqK/pubhtml](https://docs.google.com/spreadsheets/d/e/2PACX-1vRI-M60nMVqr8Y9U5JUmLPagetZSnvPIgGvUH9k-_SpExI79eswPicqGHH7coprFGV8HFQ6Zp0HesqK/pubhtml)    
Magic Door 24: https://eloistree.itch.io/magicdooratelierdegroupetechnocite  

Here we are going to try to use GitHub Pull Request: 
[https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneManifest](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDroneManifest)

  

  

-----------------------------------------  

