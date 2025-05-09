# Argent et pièce dans le niveau

Afin de rendre le jeu plus intéressant et de préparer le système d'amélioration dans le jeu, il faut permettre à notre personnage de rammasser et des pièces dans le niveau. 

Commencez par rajouter un [objet](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Objets.md) en forme de pièce et a en mettre quelques unes dans le niveau.

(image 1)

Ensuite, ils nous faut, comme pour les Points de vie précédents, ajoutez les variables permettant de compter les pièces : ajoutez une variable globale et une variable d'objet **Argent**.

(image 2) 

> On dois dissocier l'argent posséder par le joueur dans un niveau de celui possédé au total, car si le joueur perd la partie et recommence, il dois perdre l'argent accumulé pendant le niveau, mais garder celui acquis auparavant.

Ajoutez l'évènement permettant de récupérer les pièces : 

(image 3) 

Il faut également rajouter au lancement de la scène un évènement pour initialiser la variable du joueur, afin que l'on sache combien d'argent on possède au total.

(image 4)

## Apparition des pièces sur l'interface 

Ajoutez les éléments de l'interface permettant de savoir combien de pièce possède le joueur : il faut un **TextGold** et un objet pour savoir qu'il s'agit de l'argent, par exemple, une **pièce**.

(image 5) 

Enfin, il faut ajouter l'évènement permettant de mettre à jour cette valeur.

(image 6)

Et voilà ! Nous avons un système monétaire dans le jeu. Nous verrons plus tard à quoi nous servira l'argent que nous pouvons rammasser, et nous allons également ajouter d'autres moyens d'en obtenir.

[5 - équipement et attaque]()
