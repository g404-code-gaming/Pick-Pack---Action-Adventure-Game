# 8 - Création des ennemis

Maintenant que nous avons un personnage qui évolue au fil du jeu, nous allons passer à une autre partie très intéressante d'un jeu en 3D : la création et la programmation des **ennemis**.

Dans Pick&Pack, nous allons ajouter deux types d'ennemis : 
  - (1) Une **Tourelle**. Elle ne bouge pas, et lorsqu'elle détecte le joueur, elle lui tire dessus. 
  - (2) Un **Personnage**. Il reste immobile tant qu'il ne détecte pas le joueur, mais dés que ce dernier approche un peu trop, le personnage se met à poursuivre le joueur.

  ![image 1]() 

  C'est la dernière étape du projet : avec ça, nous auront tout ce qu'il faut pour construire un jeu complet et amusant ! 

  ## Tourelle 

  La **tourelle** est un ennemi fixe qui peut tirer des projectiles sur le joueur. 

  Ajouter un [objet](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Objets.md) tourelle à la scène. Il faut l'intégrer au groupe **Détruire**, et lui ajouter le comportement **Physic 3D** et **Fire Bullet**. N'oubliez pas de définir les Points de vie et l'Argent qu'elle rapporte dans les variables.

  Ajouter ensuite les évènements pour la tourelle. 
    - (1) Lorsque le personnage du joueur est à une certaine distance de la tourelle, l'évènement s'active.
    - (2) La tourelle tourne alors en direction du personnage et lui tire dessus (pensez à ajouter un objet pour le projectile et a ajouter le Comportement Fire Bullet à la tourelle). 
    - (3) Généralement, le projectile ne part pas dans le bon sens, n'a pas la bonne taille ou d'autres paramètres : il faut ajoutez des conditions pour avoir les paramètres qui vous conviennent.
    - (4) On ajoute ensuite l'évènement qui détruit les projectiles s'ils touchent des murs. 

![image 2]() 

 Il faut que le projectile de la tourelle fasse partie du groupe **Danger** pour blesser correctement le joueur. Indiquez dans ses variables les dégâts qu'il fait, puis tester le jeu pour voir si votre tourelle fonctionne correctement.

 ## Personnage ennemi 

 Le Personnage est un ennemi mobile qui se met à poursuivre le joueur lorsqu'il le repère. 

 
