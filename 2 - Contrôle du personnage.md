# Contrôle du personnage 

C'est l'heure de passer à l'étape essentielle d'un FPS : les contrôles du personnage. 

Notre personnage peut faire trois choses principales : 
  - 🖱️ Déplacer l'axe de la caméra à l'aide de la souris.  
  - 🎮 Se déplacer à l'aide des flèches directionnelles ou des touches ZQSD.  
  - 🕹️ Sauter avec la touche Espace.

## Variables globales 

Pour commencer, et en vus de préparer le suite du cours, nous devons créer quelques [variables globales](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Variables.md). 
Ces variables seront utiles pour les déplacements du personnage ou les gestions des dégâts. Nous en ajouterons d'autres par la suite. 

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/0_controle.JPG)

## Contrôle de la caméra 

Difficile de voir ce qu'il se passe quand notre caméra est coincée dans le ciel. Nous allons devoir commencer par intégrer la caméra au personnage pour pouvoir voir la scène correctement et faire la suite du programme.

Pour contrôler la caméra, nous allons ajouter une extension à notre projet : 

Ajoutez les extensions **Caméra 3D à la première personne** et **Verouillage du pointeur de la souris**.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_controle.JPG)

Ensuite, nous allons, dans les [évènements](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/%C3%A9v%C3%A8nements.md), ajouter ce qu'il faut pour voir à travers les yeux du personnage, et également pour bouger la caméra lorsqu'on déplace la souris.

Pour utiliser le pointeur, il faut l'activer lorsque le joueur clique sur l'écran. C'est seulement lorsque le pointeur est activés que la caméra va suivre la vue du joueur : 

Ensuite, une fois que le pointeur est verouillé, il faut : 
  - (1) Demander à la caméra de voir à travers les yeux du personnage. 
  - (2) Faire tourner le personnage en fonction de mouvement du pointeur sur l'axe X.
  - (3) On place la vue de la caméra à 2/3 de la hauteur du personnage pour donner l'impression de voir à travers ses yeux.
  - (4) Faire tourner le personnage sur l'axe Y en fonction du mouvement du pointeur sur l'axe Y. 
  - (5) pour éviter que le personnage puisse se retourner sur lui-même en regardant en l'air, on fixe des limites à l'axe Y.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/2_controle.JPG)

à l'ajout de chaque nouvelle action, teste le jeu pour comprendre leur fonction et anticiper les erreurs potentielles. 

Une fois que vous avez terminer, vous devriez avoir un personnage qui peut regarder dans toutes les directions : bravo ! 

## Contrôle des déplacements 

Pour l'instant, notre personnage peut bouger les yeux, mais il reste bloqué dans l'espace. Si vous l'avez mis en l'air, vous remarquerez qu'il ne tombe même pas. 

Nous allons ajouter le [comportement](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Comportement.md) **3D physics character** pour permettre au personnage d'être affecté par la gravité.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/3_controle.JPG)

Désormais, nous avont un personnage qui est affecté par la gravité, mais cela le fait traverser les objets et tomber dans le vide. 
Pour éviter cela, il faut ajouter le comportement **3D physics** à tout les objets qui servirons de décors (notammant les murs et le sol). 

Une fois que c'est fait, nous pouvons créer les évènements de déplacement du personnage en fonction de la variable **Vitesse**: 

> Dans les jeux de tir à la première personne (FPS), les commandes de base pour se déplacer sont Z (avancer), S (reculer), Q (aller à gauche), D (aller à droite).

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/4_controle.JPG)

Une fois que ces évènement sont terminés, le personnage peut se déplacer dans l'espace : notre jeu commence à prendre forme.

## Saut et Course 

Un personnage qui se déplace, c'est bien, mais s'il peut sauter et courir, c'est encore mieux ! 

Pour l'évènement de **saut**, rien de plus facile : il suffit de simuler un touche de saut lorsque le personnage appuie sur la barre Espace : 

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/5_controle.JPG)

Pour la **course**, c'est un peu différent : lorsque l'on va appuyer sur la touche de course, cela va augmenter notre vitesse. 
Il ne faut pas oublier de remettre la Variable Vitesse à sa valeur initiale lorsqu'on arrête d'appuyer sur la touche. 

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_controle.JPG)

Désormais, les bases du mouvement sont faites ! Nous pouvons déplacer notre personnage dans l'espace de manière fluide, notammant grâce à la caméra et la course. 

[3 - interactions avec l'environnement - Partie 1]()


