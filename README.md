# 2.Merise : Modèle Conceptuel de Données (MCD)
Le modèle Conceptuel de Données **Entité** / **Association** repose sur les concepts :
- Entités
- Propriétés

Ce modèle est souvent nomme **Entité-Relation**

Cela permet de décrire un ensemble de données relatives à un domaine défini afin de les intégrer ensuite dans une Base de Données.

## A. Entité et Entité Type
|Entité|Entité Type|
|:----------|:---------------|
| Une entité est un objet, une chose concrète ou abstraite qui peut être reconnue distinctement. (ma voiture, ma maison, un pays et même Toi ). | Une entité type est la réprésentation communune que l'on adopte pour des entités qui possèdent les même caractéristiques. (Personne, voiture, région) |

<img src="assets/mcd-001.png" style="width:150px" alt="img"/>

## B. Propriétés (ou attributs)
Chacunes de ces entités sont constitués de **propriétés (ou attributs)**. Par exemple, pour notre nouvelle entité **Person**, celle-ci a pour attributs son `nom`,`prénom`, `age`, ...

<img src="assets/mcd-002.png" style="width:150px" alt="img"/>

## C. Association et Association Type
|Association|Association Type|
|:----------|:---------------|
|Il s'agit simplement d'un lien entre plusieurs entités |Répresentation d'un ensemble de relations qui possèdent les même caractéristiques, lien entre plusieurs entités type. (Ex: Le mariage de deux personnes).|

Ces associations sont reliés entre elles par un **verbe** d'action ou d'état (être, paraître sembler, ...)

![](assets/mcd-003.png)

**Rôle** est une donnée élémentaire de l'association (ou d'une entité). En effet, Un attribut propre à l’association est un attribut qui ne peut appartenir à aucune des entités qu’il relie individuellement, mais qui caractérise spécifiquement leur relation.

![](assets/mcd-005.jpg)

#### Comment identifier un attribut propre à l’association ?
Lors de la conception du **MCD**, on peut se poser ces trois questions clés :

L'attribut appartient-il naturellement à une seule entité ?
- Si oui, il doit rester dans l'entité.
- Ex : "Nom_Acteur" appartient à ACTEUR, pas à l'association.

L’attribut caractérise-t-il la relation entre les entités ?
- Si oui, il appartient à l’association.
- Ex : "Rôle" ne caractérise ni ACTEUR ni FILM seul, mais leur relation.

Si l’association disparaît, l’attribut a-t-il encore un sens ?
- Si non, c’est un bon indice que l’attribut appartient à l’association.
- Ex : "Date_Emprunt" n’a de sens que si l’association "emprunte" existe entre un ÉLÈVE et un LIVRE.


## D. Identifiant
Chaque **Entité** doit être identifié de manière *unique*; clé naturelle. En effet, l'identifiant est une valeur qui identifie sans ambiguïté une entité. Elle est généralement souligné.

![](assets/mcd-006.jpg)
