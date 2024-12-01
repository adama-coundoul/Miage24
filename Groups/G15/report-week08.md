# AIT YAHIA Maya 

## Design pattern Composite :

Cette semaine, j'ai regardé les vidéos sur le design pattern Composite, qui permet de structurer des objets en hiérarchies. 
Par exemple, dans un diagramme, chaque élément (texte, cercle, segment) peut être un objet individuel ou un groupe d'objets (composite). 
Tous ces objets, qu'ils soient simples ou composites, partagent une même interface, permettant de les manipuler de manière uniforme. 
Cela simplifie l'ajout de nouveaux comportements sans modifier la structure existante.

## Kata (les mouvements des pions): 

J'ai refactoré ma méthode targetSquareLegal, qui gérait avant tous les mouvements, en appelant maintenant des petites méthodes dédiées à chaque type de mouvement. 
Cela permet d'éviter une méthode trop longue et complexe, remplie de nombreuses conditions if. 
J'ai également commencé à réfléchir à la manière d'implémenter le dernier mouvement "en passant".

# Dahouane Youssra

Cette semaine, nous avons étudié deux concepts essentiels : l'héritage et la délégation.

## Héritage

L’héritage permet de créer une hiérarchie de classes où une sous classe hérite des caractéristiques et comportements d’une super-classe. Il facilite la réutilisation du code en permettant aux sous-classes de spécialiser ou étendre les fonctionnalités. Par exemple, si une super-classe TextEditor définit un formatage générique, ses sous-classes comme FastFormattingTextEditor ou SlowFormattingTextEditor peuvent implémenter des formats spécifiques.

## Délégation

La délégation permet à une classe de confier une tâche à un autre objet. Cela permet de modifier le comportement sans modifier la classe principale.
Par exemple, une classe TextEditor délègue l'exécution d'une méthode format à un objet spécialisé (FastFormatter, SlowFormatter, etc.). L’objet délégué peut être remplacé à tout moment.

## Kata (Refactorisation du rendu des pièces)

J’ai créé des méthodes dans les classes MyBlackChessSquare et MyWhiteChessSquare qui renvoient les caractères appropriés pour chaque pièce (renderWhiteBishop, renderBlackKnight, renderWhiteKing, etc). Ensuite, j’ai modifié la méthode initialize dans MyFenParser pour associer chaque symbole de pièce à sa couleur et à sa classe appropriée. 


