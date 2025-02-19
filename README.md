# 2.Merise : Relations
Maintenant que vous savez créer des associations entre différentes entités, il est temps de passé aux relations. Il existe plusieurs types de relations. 

## 1. Relation binaire
Une association entre deux entités. Prenons pour exemple:

```markdown
Un étudiant possède un diplomé
```

- **Entité étudiant** : (Nom, Prénom et Naissance)
- **Entité diplome** : (Titre, Niveau)
- **Association** : possède (année, mention)

Soit analysons les deux relations:

- Un étudiant possède **0:n** diplôme(s) => zéro ou plusieurs 
- Un diplôme est possédé par **1:n** étudiants => un ou plusieurs

**FAIRE LE MODEL**

## 2. Partage d'une même collection
**Une collection** est l'ensemble des participants d'une association

```markdown
Une personne possède ET/OU habite dans une maison
```

- **Entité étudiant** : (Nom, Prénom et Naissance)
- **Entité diplome** : (Titre, Niveau)
- **Associations** : Habiter ET posseder

Analysons les relations:

- Une personne possède **1:1** logement => un et un
- Une personne habite **1:n** logement => un et plusieurs
- Un logement est possédé par **0:n** personne(s)=> zéro et plusieurs
- Un logement est habité par **1:n** personne(s) => un et plusieurs 

**FAIRE LE MODEL**

## 3. Relation sur une même entité: soit une relation 1-aire, entité récursive
```markdown
Un employé est supervisé par une employé
```

Etrange que cela soit, c'est une entité très intéressante. En effet, on pourrait transposer ce modèle sur d'autres exemple, comme:

- Des commentaires d'un blog, on des sous commentaires
- Des catégories d'articles, peuvent avoir des sous catégories

Dans ce cas, on appelle cela des entité récurcives.

Analysons

- **Entité employé** : (Nom, Prénom et Naissance)
- **Associations** : Supervision

Soit

- Un employé est supervisé par **0:1** superviseur
- Un superviseur supervise **0:n** employé.

**FAIRE LE MODEL**

## 3. Relation n-aires
