# Équipement et attaques

Dans le jeu Pick&Pack, le personnage possède des outils dont il peut se servir pour miner ou attaquer. Dans l'exemple, il s'agira d'une hache et d'un fusil, mais il peut s'agir de n'importe quoi d'autre tant qu'il y a une arme de corps-à-corps et une arme à distance.  
  - L'arme de mêlée frappe plus vite, mais n'a pas beaucoup de portée.  
  - L'arme à distance tire à longue portée, mais possède des munitions limitées.

Le personnage pourra changer d'arme pour utiliser celle qui lui semble la plus adaptée à la situation.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_1.JPG)

### Liste des éléments à ajouter

Il nous faut ajouter de nouveaux objets à notre scène. Pour simplifier les choses, ils sont tous listés ici :  
  - 🏹 une **arme à distance**  
  - ⚔️ une **arme de mêlée** ou outil  
  - 📜 un texte pour les munitions **TextMunition**  
  - 💎 un objet à détruire pour gagner de l'argent. Par exemple, un morceau de **minerai**

Il nous faut également ajouter de nouvelles variables : commençons par ajouter la variable globale des munitions maximales.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_2.JPG)

Ensuite, il faut ajouter les variables du personnage. Il faut dissocier les variables de l'arme de mêlée et de celle de tir.  
  - **arme** : détermine l'arme que possède actuellement le joueur.  
  - **Cooldown** : le temps nécessaire à attendre pour pouvoir frapper à nouveau.  
  - **Dégâts** : les dégâts que l'attaque va faire.  
  - **Munition max** : les munitions que l'arme à distance peut contenir au maximum. Cette valeur sera égale à la variable globale Munition.  
  - **Munition** : les munitions actuelles de l'arme à distance. Quand elle tire, elle perd 1 munition, et ne peut pas tirer si elle en a 0.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_3.JPG)

Pour finir, ajoutez un nouveau groupe d'objets : **Detruire**. Ce groupe contient tous les objets que vous pouvez détruire avec vos attaques. Ces objets doivent tous avoir une variable **PV** et une variable **Argent**.

> Si vous ne voulez pas que vos objets rapportent de l'argent, vous pouvez mettre Argent = 0.

## Afficher et changer d'arme

Commençons par voir l'arme et permettre au joueur de changer d'arme.

Dans un premier temps, ajoutez les objets d'armes et ceux des munitions sur l'interface. Si vous le souhaitez, vous pouvez également ajouter un réticule de visée au milieu de l'écran.  
Pensez bien à rendre les armes invisibles au départ en modifiant l'opacité.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_4.JPG)

Pour changer d'arme, nous allons utiliser la **molette de la souris**, comme dans beaucoup d'autres jeux FPS.  
  - Lorsque la molette monte vers le haut : on utilise l'arme à distance  
  - Lorsque la molette descend vers le bas : on utilise l'arme de mêlée

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_5.JPG)

Testez votre jeu pour voir si le changement d'arme se fait correctement.

## Attaquer avec les armes

Fondamentalement, les deux armes fonctionnent de la même manière : lorsque le joueur clique sur le bouton gauche de la souris, il attaque.

Pour gérer le fonctionnement de l'attaque, nous allons ajouter une extension **Raycaster**.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_6.JPG)

L'extension permet de tracer une ligne entre la caméra et l'endroit vers lequel elle regarde. Elle permet aussi de détecter les objets qui sont sur la trajectoire, ce qui permet de savoir si on regarde un objet ou non.

Ajoutez les évènements d'attaque.  
On commence par l'attaque de mêlée, qui est plus simple à faire :

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_7.JPG)

Ensuite, on rajoute celle à distance : elle fonctionne de la même manière, mais consomme des munitions et ne peut pas tirer s’il n’y en a pas.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_8.JPG)

### Destruction d'un objet

Nous venons de faire les attaques : elles enlèvent des points de vie aux objets de type **Detruire**. Désormais, nous voulons faire disparaître les objets lorsqu’ils n’ont plus de PV.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_9.JPG)

### Interface

Pour finir la partie sur l’arme, ajoutez l’évènement mettant à jour les munitions du joueur.  
Afin qu’il sache combien de munitions il lui reste, mais aussi combien de munitions il peut avoir au maximum, nous utilisons les deux variables en même temps : **Munition** + **Munition_max**.

> Le fait de coller plusieurs morceaux de texte les uns à la suite des autres pour ne former qu’un seul texte plus grand s’appelle la **concaténation**.

![image](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/Image/arme_10.JPG) 

### Bonus - Visuel et son 

Ajoutez un moyen de reconnaître lorsque le joueur touche une cible avec une attaque. 
Par exemple : 
  - Ajoutez un son lorsque l'attaque touche une cible.
  - Modifier temporairement l'opacité de la cible pour indiquer qu'elle est atteinte par l'attaque.
  - Ajoutez des effets spéciaux (explosions, lumières, ...).

[6 - Menu et Amélioration](https://github.com/g404-code-gaming/Pick-Pack---Action-Adventure-Game/blob/main/6%20-%20Menu.md)
