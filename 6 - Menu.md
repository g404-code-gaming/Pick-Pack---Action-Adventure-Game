# Menu et Amélioration

Normalement, dans un jeu vidéo, le Menu n'est pas la première chose qui est faite : on attend en général que la partie principale du jeu soit terminée avant de passer au Menu.

Ici, nous allons faire une exception, car le menu va être essentiel pour le jeu, et permettre d'améliorer notre personnage. Cela nous permettra de le travailler davantage que sur d'autres projets.

## Création du Menu et des autres fenêtres 

Nous allons avoir besoin de plusieurs nouvelles scènes pour construire notre menu : 
  - Un **Menu principal** 
  - Une **fenêtre de sélection des niveaux**
  - Une **fenêtre des contrôles**
  - Une **fenêtre des améliorations**

![image 1](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_1.JPG)

## Menu principal 

Ajoutez des [objets](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Objets.md) de type boutons sur la scène. Il en faut un pour chacune des fenêtres crées précédemments (autre que le menu principal).

Il faut également un bouton pour quitter le jeu. 

![image 2](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_2.JPG)

Concernant les évènements, le Menu principal se résume généralement comme suis : 
    - Le bouton 'EXIT' fait quitter le jeu.
    - Les autres boutons font changer de scène.

![image 3](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_3.JPG)

Il est également possible de rajouter un fond d'écran, un titre, ou tout autre chose qui puisse donner vie au menu.

## Fenêtre des contrôles 

La fenêtre des contrôles indique au joueur quelle touche utiliser pour faire les différentes actions possibles dans le jeu. 

![image 4](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_4.JPG)

La seule action possible dans cette fenêtre est un **bouton de sortie** permettant de revenir au menu principal.

## Fenêtre de sélection de niveau 

Il y aura **plusieurs niveaux** dans le jeu. Le joueur a la possibilité de choisir le niveau qu'il souhaite faire. Néanmoins, il ne peut pas choisir un niveau s'il n'a pas fait les niveaux précédents.

![image 6](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_6.JPG)

Commencez par rajouter la [variable globale](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Variables.md) **Niveau**, qui indique le nombre de niveau réussis par le personnage. 

![image 5](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_5.JPG)

Ensuite, Ajoutez les évènements permettant de lancer le niveau. pour les niveaux au dessus du premier, il faut que l'action ne fonctionne que si le joueur a un Niveau assez haut.

![image 7](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/6_menu_7.JPG)

Nous ajouterons l'évolution des niveaux plus tard dans le projet.

Une fois que les fenêtres les plus 'faciles' sont faites, nous allons pouvoir construire la fenêtre servant a améliorer le personnage.

[7 - Amélioration](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/7%20-%20Am%C3%A9lioration.md)
