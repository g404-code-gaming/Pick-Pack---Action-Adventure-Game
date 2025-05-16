# Amélioration du personnage

Dans Pick&Pack, le joueur peut rammasser de l'argent, et, une fois la partie terminée, peut améliorer son personnage.

Dans la **scène d'amélioration**, Mettez tout les éléments que peut améliorer le personnage : 
  - Les Points de vie
  - Les Munitions max de l'arme à distance
  - La Vitesse de course du personnage
  - Les Boutons sur lesquel je joueur va cliquer pour améliorer
  - Le prix de chaque améliration

[image 1]()

Dans un premier temps, mettez à jour les variables textuelles dans les évènements, afin que le joueur vois ses caractéristiques et son argent en temps réel.

[image 2]()

Avant de passer au gros morceau, ajouter l'évènement pour permettre de retourner au Menu.

[image 3]()

Ensuite, créez les évènements permettant de cliquer sur les boutons pour acheter des améliorations. Ces évènements fonctionnent comme suis : 
  - Lorsque le joueur clique sur un bouton, on vérifie s'il a assez d'argent pour acheter l'amélioration.
  - S'il remplis les conditions, on soustraie le prix de l'amélioration à l'argent global du joueur, puis on augmente la caractéristique concernée.

[image 4]()

## Intégration du Menu dans le niveau : la fin du jeu

Pour la fin du jeu, nous allons utiliser une porte : lorsque le joueur regarde la porte en étant proche d'elle, cela lui fait finir le niveau. 

Le but du jeu est d'atteindre cette porte. 

[image 5]()

Ajoutez le code permettant d'ouvrir la porte et de terminer le niveau. Il ne faut pas oublier de désactiver le pointeur et de mettre à jour les variables d'argent et de niveau.

[image 6]()

Avec tout ça, nous avons désormais un Menu fonctionnel dans lequel nous pouvons améliorer notre personnage. 

Tester différentes améliorations avant de passer à la suite. 


