# AIT YAHIA Maya 

## Design pattern Visitor 

Cette semaine, j'ai regardé les vidéos sur le design pattern Visitor, qui permet d'ajouter de nouvelles fonctionnalités à un ensemble d'objets sans en modifier la structure. Il repose sur le principe du double dispatch, où chaque objet accepte un visiteur et délègue l'action à une méthode spécifique en fonction du type de l'objet. Cela permet une grande modularité et extensibilité, car de nouveaux comportements peuvent être ajoutés sans toucher aux objets eux-mêmes.

Prenons l'exemple d'un système d'expressions mathématiques. Si nous avons l'expression (1 + (3 * 2)), un visiteur Evaluator peut être utilisé pour calculer la valeur de cette expression, renvoyant 7. Un autre visiteur, Printer, pourrait afficher cette expression sous forme de notation polonaise, par exemple + 1 * 3 2. La séparation des responsabilités entre les objets de calcul et les actions (comme l'évaluation ou l'affichage) permet d'ajouter de nouveaux comportements sans modifier les classes des expressions.

Le modèle repose sur la méthode acceptVisitor:, où un objet "accepte" un visiteur et délègue l'exécution à une méthode appropriée, comme visitPlus ou visitTimes, selon le type d'objet. Cette séparation améliore la flexibilité et la maintenabilité du code.
