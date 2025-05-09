# Point de vie et danger dans l'environnement

Pour commencer à faire interagir notre personnage avec le monde qui l'entoure, nous allons ajouter un peu de difficulté en programmant la mort du personnage et la gestion de ses points de vie.

## Lac d'acide 

Le sol de la carte sera rempli d'acide : notre personnage est immédiatement tué s'il tombe dans l'acide. Il suffit alors de recharger le niveau lorsque le personnage tombe dans l'acide :

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_0.JPG)

C'est tout : maintenant, notre personnage meurt en tombant au-delà de la plateforme de jeu. Nous pourrions déjà commencer à faire un petit niveau où le personnage doit avancer sans tomber, mais nous allons d'abord rajouter les points de vie.

## Points de vie

Pour gérer toutes les caractéristiques du joueur qui sont propres au niveau, nous allons lui créer des [variables d'objet](https://github.com/g404-code-gaming/GDevelop_Cour/blob/main/Variables.md).

Pourquoi lui refaire des variables alors que nous avons créé des variables globales ? Parce que notre personnage va pouvoir évoluer d'un niveau à l'autre : nous avons donc besoin de dissocier les informations propres au niveau et celles qui vont être conservées en dehors du jeu.

Ajoutez donc les variables suivantes sur le Personnage :

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_1.JPG) 

Ajoutez un évènement au début du jeu pour initialiser toutes les variables du personnage en fonction des variables globales.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_2.JPG)

Maintenant, il faut rajouter les évènements qui nous font perdre des PV lorsqu'on subit des dégâts. Pour simplifier le programme, nous allons créer un groupe d'objets **Danger** qui contiendra tous les objets de la scène capables de nous faire des dégâts.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_3.JPG)

Pour chacun de ces objets, rajoutez une variable d'objet **Dégât** : ce sera la quantité de points de vie qu'ils enlèvent au personnage.

Toutefois, nous ne pouvons pas utiliser la condition "Collision" classique, car elle ne fonctionne que sur les objets en 3D. Ajoutez une extension pour pouvoir gérer les collisions en 3D.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_4.JPG)

Désormais, nous avons tout ce qu'il faut pour rajouter les évènements des PV :  
- Créez un premier évènement pour reconnaître la collision avec un objet dangereux. - Pour éviter que notre personnage ne subisse trop de dégâts d'un coup, utilisez la variable **Invincible** comme condition : le personnage ne peut pas subir de dégâts tant que cette variable n’est pas fausse.  
- Ensuite, un **Chronomètre** va servir à rendre le personnage vulnérable à nouveau.  
- Enfin, lorsque le personnage a 0 PV, il meurt et on retourne au début du jeu.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_5.JPG)

Testez le jeu pour vérifier que tout fonctionne !

## Affichage de l'interface et des Points de vie

Pour savoir combien de points de vie possède le personnage, nous allons utiliser une UI.

Créez un nouveau **calque** UI sur lequel placer une **barre de PV** et un **TextPV**. Ces objets peuvent être en 2D : pas besoin de 3D pour une interface.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_6.JPG)

Nous pouvons désormais ajouter un évènement qui met à jour la taille de la barre de vie et le texte en fonction des points de vie du joueur.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_7.JPG)

## Optionnel 

Rajoutez un moyen visuel pour que le joueur comprenne qu’il a été blessé. Par exemple, un voyant ou un écran rouge qui s’allume lorsqu’il subit des dégâts.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/1_PV_8.JPG)

Désormais, nous avons un système de gestion de mort fontionnel ! 

[4 - interactions - Partie 2]()
