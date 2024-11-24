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
