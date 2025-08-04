# Lexique

Pour faciliter la compréhension, nous ferons des analogies avec des logiciel de tableur (google sheet / microsoft excel)

## Sommaire

- [Propriété](#propriété)
  - [Types de propriétés](#types-de-propriétés)
  - [Options de propriétés](#options-de-propriétés)
- [Entité](#entité)
- [Donnée](#donnée)
- [Relation](#relation)

## Propriété

- définie par un nom unique au sein de l'entité, d'un type et d'options
- même concept qu'une colonne dans un tableur

### Types de propriétés

| type      | description                                                      |
|-----------|------------------------------------------------------------------|
| VARCHAR   | chaine de caractères ne pouvant pas dépasser une certaine taille |
| CHAR      | chaine de caractères d'une taille fixe                           | 
| INT       | nombre entier                                                    |
| FLOAT     | nombre à virgule flottante                                       |
| BOOLEAN   | true ou false                                                    |
| DATETIME  | date et heure                                                    |
| TIMESTAMP | temps écoule en ms depuis le 01/01/1970                          |

### Options de propriétés

| options        | description                                                                   |
| -------------- | ----------------------------------------------------------------------------- |
| NOT NULL       | La propriété ne peut être vide                                                |
| UNIQUE         | La valeur ne peut pas être répétée dans la table                              |
| AUTO_INCREMENT | La valeur est un INT qui augmente de 1 à chaque nouvel enregistrement         |
| DEFAULT        | Spécifier quelle est la valeur par défaut si aucune n'est fournie             |

## Entité

- représentation d'un élément matériel ou immatériel, abstrait ou concret, qui agit dans le système
- définie par
  - un nom unique au sein du système
  - une liste de propriétés
  - un identifiant parmi ces propriétés
- même concept qu'une feuille de classeur dans un tableur

## Donnée

Une donnée est l'enregistrement d'une information dans une propriété d'une table.

On peut rapprocher le concept de la donnée en base de données à celui de la cellule dans un tableur.

**Exemples :**

Pour une entité `user` avec les propriétés `firstname`, `lastname`, `dateOfBirth` et `active`, on pourra avoir les données suivantes :

| firstname | lastname | dateOfBirth | active |
| --------- | -------- | ----------- | ------ |
| John      | Doe      | 1992/08/01  | 1      |
| Jane      | Smith    | 1985/05/15  | 1      |
| Alice     | Johnson  | 1978/11/23  | 0      |
| Bob       | Brown    | 2000/02/29  | 1      |

On peut également parler d'`occurence` ou d'`instance`.

## Relation

- lien sémantique entre plusieurs entités
- on peut également parler d'`association`
- définie par un verbe d'action
- il est possible d'avoir une relation avec une seule entité
  - on appelle ça une relation `réflexive` ou `récursive`
- existe uniquement dans un SGBDR (*RDBMS* en anglais)
