# Argent et pièce dans le niveau

Afin de rendre le jeu plus intéressant et de préparer le système d'amélioration dans le jeu, il faut permettre à notre personnage de ramasser des pièces dans le niveau.

Commencez par rajouter un [objet](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Objets.md) en forme de pièce et à en mettre quelques-unes dans le niveau.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_1.JPG)

Ensuite, il nous faut, comme pour les Points de vie précédents, ajouter les variables permettant de compter les pièces : ajoutez une variable globale et une variable d'objet **Argent**.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_2.JPG) 

> On doit dissocier l'argent possédé par le joueur dans un niveau de celui possédé au total, car si le joueur perd la partie et recommence, il doit perdre l'argent accumulé pendant le niveau, mais garder celui acquis auparavant.

Ajoutez l'évènement permettant de récupérer les pièces :

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_3.JPG)

Il faut également rajouter, au lancement de la scène, un évènement pour initialiser la variable du joueur, afin que l'on sache combien d'argent on possède au total.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_4.JPG)

## Apparition des pièces sur l'interface 

Ajoutez les éléments de l'interface permettant de savoir combien de pièces possède le joueur : il faut un **TextGold** et un objet pour indiquer qu'il s'agit de l'argent, par exemple, une **pièce**.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_5.JPG)

Enfin, il faut ajouter l'évènement permettant de mettre à jour cette valeur.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/piece_6.JPG)

Et voilà ! Nous avons un système monétaire dans le jeu. Nous verrons plus tard à quoi nous servira l'argent que nous pouvons ramasser, et nous allons également ajouter d'autres moyens d'en obtenir.

[5 - équipement et attaque](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/5%20-%20%C3%A9quipment%20et%20attaque.md)
