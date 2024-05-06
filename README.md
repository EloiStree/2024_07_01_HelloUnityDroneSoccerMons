# 2024_07_01: Hello Unity Shield Drone

L'idée: pratiquer Unity3D par le jeu  
L'objectif: préparer à utiliser les compétences apprisent en entreprise.  
Comment: par la pratique sur un jeu multijoueur et l'utilisation du package manager.  


**Developeur:**  
Mon objectif est de m'amuser avec vous sur la pratique de Git, les rotations, les réseaux et l'optimiation pour casque XR.  
Créer des applications sur les Quests, Android en général, demande de parler ensemble d'optimisation.  

**Designer:**  
Apprendre les bases de ce qu'est la XR et pratiquer via la mise en place d'un circuit de drones créé à 12 via le package manager.  

**Developeur:**    
Day 1: [Git Package](WorkshopPerDay/2024_07_01.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/2))  
Day 2: [Webscoket et Rotation](WorkshopPerDay/2024_07_02.md)   ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/3))  
Day 3: [Mirror et Job System](WorkshopPerDay/2024_07_03.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/4))    
Day 4: [LOD et Optimisation](WorkshopPerDay/2024_07_04.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/5))  
Day 5: [Android XR ](WorkshopPerDay/2024_07_05.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/6))  

**Designer**  
Day 1: [Les bases de la XR avec Meta](WorkshopPerDay/2024_07_16.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/7))  
Day 2: [Bonjour Unity XR](WorkshopPerDay/2024_07_17.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/8))  
Day 3: [XR et l'industrie](WorkshopPerDay/2024_07_18.md)  ([I](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/9))  


## Plan de l'atelier
  
**Developeur:**  
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/assets/20149493/1594a8ae-438c-4737-8c00-1310653dfc28)  

- Apprendre à créer des boites à outils avec Git et Unity Package manager
  - Créer son drone et importer celui des autres élèves.
  - Créer une case de 16x16 d'un circuit pour drone via un package donner.
- Apprendre à bouger un drone via websocket sur un multi-joueur via Discord.
  - Interagir via websocket et inisation à ce qu'est une clé RSA
  - Apprendre des trucs et astuces sur les rotations et pratiquer en déplacent le drone.
- Via un package de broadcast en Mirror donné, apprendre à afficher les autres drones via des triangles avec le Job System de Unity (pas d'ESC)
  - S'abonner à un server Mirror via package. (apprendre les bases d'un jeu en réseaux sans en faire un)
  - Exercice pratique pour créé un Mesh de triangle qui bouge via le job system de Unity3D.
- Apprendre à maitriser différentes techniques d'optimisation pour la XR focus sur les LOD.
  - Cours théorique sur différentes techniques d'optimisation et focus sur le LOD, les Draw Mesh et les imposteurs
  - Apprendre à utiliser différentes pools d'objet basées sur la distance d'un objet via Job System.
- Avec ce qui a été fait précédemment, apprendre à bouger son drone et voir les autres dans un casque 
  - Apprendre ce qu'est Open XR et comment on écoute à un manette de jeu XR
  - Apprendre à builder l'exercice de la semaine sur le casque donné lundi, si pas déjà fait en auto-didacte.


**Designer**  
- Apprendre les bases de la VR/XR : passé, présent, futur ?
  - Comprendre ce qu'est la VR/XR
  - S'assurez que tout le monde à tester un à deux casques présents.
  - Théorie sur ce qui est utilisable en XR 
  - Installer SideQuest et sideloader ça première application. 
- Pratiquer avec Unity3D la création une première application XR en prolongeant l'exercice des développeurs.
  - Démonstration de comment créer une appication XR avec Unity3D
  - "Hello Cube" Apprendre à builder une APK d'un cube en XR
  - Pratiquer la création d'un package de niveaux pour drones à l'aide d'un outil du package manager.
  - Exporter le package créé  sur GitHub pour une utilisation dans un projet de groupe.
- Exploration de l'utilisation de la réalité mixte dans l'industrie et découvertes des boîtes à outils disponibles.
  - Histoire de la VR de 2014 à 2024 et son utilisation dans l'industrie
  - Introduction à ce qu'est MRTK et VRTK pour arriver sur XR Toolkit 3.0 vs Meta SDK
  - Pecha-Kucha de groupe sur la recherche de la meilleur application de réaltié mixed du marché.


Casques disponibles théoriquement durant la formation:  
[Les casques disponibles](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/issues/10)  

> La description de l'atelier fournie ici peut être sujette à des changements à tout moment, mais les principaux éléments sont présentés ci-dessous.
> 
> La dernière fois que j'ai mentionné que je pouvais parler d'Unity et de la réalité virtuelle pendant des mois, cela s'est finalement transformé en un cours de 5 mois. L'objectif de cette formation n'est pas 
 d'aborder tous les aspects, car l'informatique est un domaine qui demande une vie entière d'apprentissage.

> ⚠️ Important : Ce cours ne couvre pas les pratiques actuelles de création d'applications en XR, car celles-ci évoluent littéralement tous les 6 mois. Il est impossible de rester constamment à jour sans être activement impliqué dans le domaine. Ce n'est pas ma situation. Il existe des YouTubers spécialisés dans ce domaine, et tout cours construit sur ce sujet se référera de toute façon à eux.

## Certification Unity3D 2024  
  
La formation dans ça globalité à une orientation vers la certification Unity3D.  
  
Vous pouvez trouver ici un document que j'utilisai en 2017 sur le sujet:  
[https://docs.google.com/spreadsheets/d/1TI_-X7T4Dh67LKkINNmpfvuofxn3RCUhHVNInaRRUsw/edit?pli=1#gid=0](https://docs.google.com/spreadsheets/d/1TI_-X7T4Dh67LKkINNmpfvuofxn3RCUhHVNInaRRUsw/edit?pli=1#gid=0)  
  
Une autre Google Sheet sera fait où pour voir quel point de la certification peu être abordé durant ce cours.  
[ Ajouter le lien ici plus tard ]  
[Notes précédentes sur le sujet](https://github.com/EloiStree/HelloUnity/wiki/TF%23024)  


## Orthographe et anglais

Toute ma vie, je n'ai jamais réussi à écrire correctement.   
C'est pourquoi je n'ai jamais fait une carrière d'enseignant officiellement (^^' ).  
Exemple : Y a-t-il un "p" ou deux "pp" dans "développeur", en anglais et en français...  
Aucune idée, faut que je regarde sur google.  

Cela n'excuse en rien la situation, mais je ferai de mon mieux avec notre nouvel ami ChatGPT. 
Mes excuses d'avance à ce sujet.

Quant à l'anglais, hormis mes formations en Belgique, je travaille toujours en anglais.
Beaucoup de mes documents sont donc rédigés dans cette langue. 


# Le code ça prend du temps
![image](https://github.com/EloiStree/2024_07_01_HelloUnityShieldDrone/assets/20149493/05f5c159-1f51-4810-ab8e-6fe85af7cc32)
