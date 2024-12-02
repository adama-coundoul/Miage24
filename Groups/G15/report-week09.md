## COUNDOUL Adama

### Delegation vs. Inheritance

Inheritance focuses on creating static and incremental definitions, which often lead to rigid and less adaptable designs. It is particularly useful for establishing abstractions and organizing hierarchies.

On the other hand, delegation provides more flexibility and modularity by allowing dynamic behavior at runtime.

When comparing these approaches, several criteria can be considered. The first is the ease of adding new formatting algorithms and integrating them into the system. The second is whether it is possible to package and deploy a new algorithm independently from the others. Finally, one must evaluate if the system can dynamically switch between different algorithms during runtime.

# Dahouane Youssra

Cette semaine, nous avons étudié deux concepts essentiels : l'héritage et la délégation.

## Héritage

L’héritage permet de créer une hiérarchie de classes où une sous classe hérite des caractéristiques et comportements d’une super-classe. Il facilite la réutilisation du code en permettant aux sous-classes de spécialiser ou étendre les fonctionnalités. Par exemple, si une super-classe TextEditor définit un formatage générique, ses sous-classes comme FastFormattingTextEditor ou SlowFormattingTextEditor peuvent implémenter des formats spécifiques.

## Délégation
La délégation permet à une classe de confier une tâche à un autre objet. Cela permet de modifier le comportement sans modifier la classe principale. Par exemple, une classe TextEditor délègue l'exécution d'une méthode format à un objet spécialisé (FastFormatter, SlowFormatter, etc.). L’objet délégué peut être remplacé à tout moment.

## Héritage vs Délégation
La délégation est plus flexible et modulaire que l'héritage car elle repose sur une relation dynamique entre objets, permettant des changements à l'exécution et une réutilisation ciblée du comportement. En revanche, l'héritage est une relation statique définie à la compilation, ce qui le rend moins adaptable aux modifications, bien qu'il simplifie la hiérarchie des classes.
