# Diagrame de cas d'usage

## Sommaire

- [Présentation](#présentation)
- [Acteurs](#acteurs)
- [Cas d'usage](#cas-dusage)
- [Association](#association)

## Présentation

- récapitulatif graphique des interactions entre acteurs et cas d'utilisation
- permet de déterminer
  - à quoi va servir le logiciel
    - l'expression des besoins des utilisateur.ices
  - ce qui est important pour le projet
  - ce qui conditionne la réussite du projet
    - le MVP

Diagramme de cas d'usage pour un distributeur automatique de billets :

![](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/what-is-a-use-case-diagram-in-UML/UML_use_case_example-800x707.PNG)

## Acteurs

- entité extérieure au système modélisé qui interagit directement avec lui
- interagit en utilisant un service du système ou en fournissant un service au système
  - utilisateur.ice
  - API
  - base de données
  - automate
- on peut distinguer l'acteur qui utilise le système de l'acteur qui fournit un service au système par *acteur principal* et *acteur secondaire*
  - un acteur principal se met à gauche du système
  - un acteur secondaire se met à droite du système
- correspond à un rôle abstrait, et pas une chose en particulier
  - acteur != personne
  - une personne peut avoir différents rôles, donc être représentée par plusieurs acteurs

![](data:image/png;base64,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)

- des acteurs peuvent être hiérarchisés entre eux

![](https://www.uml-diagrams.org/use-case-diagrams/use-case-actor-rel-gener.png)

## Cas d'usage

- une fonctionnalité, une suite d'actions, un service rendu, un comportement du système qui amène une réponse, un résultat significatif pour un acteur
- l'ensemble des cas d'usage décrit le but du système

![](https://www.uml-diagrams.org/use-case-diagrams/use-case-default.png)

## Association

- on peut hiérarchiser les cas d'usage (comme les acteurs)

![](https://www.uml-diagrams.org/use-case-diagrams/use-case-generalization.png)

- on peut également associations des cas d'usages avec des relations directes
  - on appelle ça des dépendances
  - *extend* ajoute un cas d'usage optionnel
  - *include* ajoute un cas d'usage requis

![](https://www.uml-diagrams.org/use-case-diagrams/use-case-extend.png)
![](https://www.uml-diagrams.org/use-case-diagrams/use-case-include.png)
