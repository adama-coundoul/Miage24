# AIT YAHIA Maya 

## Design pattern Visitor 

Cette semaine, j'ai regardé les vidéos sur le design pattern Visitor, qui permet d'ajouter de nouvelles fonctionnalités à un ensemble d'objets sans en modifier la structure. Il repose sur le principe du double dispatch, où chaque objet accepte un visiteur et délègue l'action à une méthode spécifique en fonction du type de l'objet. Cela permet une grande modularité et extensibilité, car de nouveaux comportements peuvent être ajoutés sans toucher aux objets eux-mêmes.

Prenons l'exemple d'un système d'expressions mathématiques. Si nous avons l'expression (1 + (3 * 2)), un visiteur Evaluator peut être utilisé pour calculer la valeur de cette expression, renvoyant 7. Un autre visiteur, Printer, pourrait afficher cette expression sous forme de notation polonaise, par exemple + 1 * 3 2. La séparation des responsabilités entre les objets de calcul et les actions (comme l'évaluation ou l'affichage) permet d'ajouter de nouveaux comportements sans modifier les classes des expressions.

Le modèle repose sur la méthode acceptVisitor:, où un objet "accepte" un visiteur et délègue l'exécution à une méthode appropriée, comme visitPlus ou visitTimes, selon le type d'objet. Cette séparation améliore la flexibilité et la maintenabilité du code.

# Dahouane Youssra 

Cette semaine, nous avons étudié deux design patterns : Composite et Visitor. 

## Composite 

Composite permet de structurer des objets en hiérarchies arborescentes, où chaque nœud peut être une feuille (un objet simple) ou un composite (un objet contenant d'autres nœuds « children »). Tous ces objets sont traités de manière uniforme grâce à une interface commune, facilitant l'ajout de nouvelles fonctionnalités sans modifier la structure existante. Par exemple, dans un système de fichiers, un dossier est un composite car il peut contenir des sous-dossiers (qui sont aussi des composites) et des fichiers (qui sont des feuilles).

## Visitor 

Visitor permet d'ajouter de nouvelles opérations à des objets d'une structure sans modifier les objets eux-mêmes. L'idée est de séparer l'algorithme de l'objet sur lequel il opère. Cela se fait en créant un visitor qui contient des méthodes pour traiter chaque type d'objet. Dans un système de gestion de produits, plutôt que d'intégrer les comportements directement dans les classes des produits, on délègue des opérations comme l'application d'une remise ou le calcul des taxes à des visiteurs. Par exemple, un DiscountVisitor applique une remise, tandis qu'un TaxVisitor calcule la taxe.

## Visitor et Double Dispatch

Le pattern Visitor utilise le double dispatch pour déterminer comment un objet doit être visité. Lors du premier dispatch, l'objet transmet son type au Visitor, qui, lors du second dispatch, appelle une méthode spécifique en fonction du type de l'objet. Cela permet à chaque objet de définir comment il doit être visité, sans avoir besoin de conditions.

