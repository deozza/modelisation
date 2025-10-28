# Diagramme de séquence

## Sommaire

<!--toc:start-->
  - [Présentation](#présentation)
  - [Construction](#construction)
    - [Acteur.ices et classes](#acteurices-et-classes)
      - [Ligne de vie](#ligne-de-vie)
    - [Messages](#messages)
      - [Aller ou retour](#aller-ou-retour)
      - [Synchrone ou asynchrone](#synchrone-ou-asynchrone)
      - [Temps d'activation](#temps-dactivation)
    - [Fragments](#fragments)
      - [Boucles](#boucles)
      - [Conditions](#conditions)
<!--toc:end-->

## Présentation

- diagramme d'intéraction, comportemental
- permet de décrire comment les éléments d'un système intéragissent entre eux et avec les acteurs
  - représentation temporelle (=chronologie) des intéractions
- point de vue interne sur le fonctionnement du système
- impossible de modéliser tout un système avec un seul diagramme
  - obligé de regrouper plusieurs diagrammes
    - en général un par cas d'usage
- pourra aider à la conception d'un diagramme de classes, ou se reposer dessus pour déterminer les intéractions

## Construction

Diagramme de séquence pour la recherche d'un produit sur un site e-commerce :

![](https://app.diagrams.net/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Fjgraph%2Fdrawio-diagrams%2Fdev%2Fexamples%2Fsequence-diagram-examples.drawio#%7B%22pageId%22%3A%22i7KtP-Vs8fw_sYRqWalm%22%7D)

### Acteur.ices et classes

- représentation des éléments qui intéragissent pour réaliser la fonctionnalité
- acteur.ices représentées par un bonhomme
- classes représentées par un rectangle
- leur nom doit être précédé d'un `:`
- sont organisés par ordre d'activation

#### Ligne de vie

- ligne pointillée qui s'étend du bas de l'acteur/classe jusqu'en bas du diagramme
- les messages sont envoyés le long de cette ligne de vie, par ordre chronologique de haut en bas

### Messages

#### Aller ou retour

- message aller
  - appel, par un élément du système, d'une fonction d'un autre élement du système
  - est décrit par
    - le nom de la fonction
    - les arguments de la fonction et son type de retour
    - une flêche avec un trait plein
- message retour
  - retour de la fonction appelée, renvoyée vers l'élément qui l'a appelée
  - est décrit par
    - une flêche avec un trait en pointillés
- message réflexif
  - si un élément appel une fonctionnalité interne, alors on rajoute une flêche qui part et termine sur cet élément

#### Synchrone ou asynchrone

- une fonction synchrone va bloquer le flux d'exécution tant qu'elle n'a pas été résolue
- si la fonction demandée est synchrone, alors le bout de la flêche est plein
  - sinon, le bout est une flêche ouverte

#### Temps d'activation

- on représente le temps d'activation d'un élément du système par un bloc le long de la ligne de vie

### Fragments

- permet de rajouter de la logique algorithmique au diagramme

#### Boucles

- permet de répéter l'appel de messages
- ajout d'un bloc `loop` avec l'itération à suivre

#### Conditions

- ajout d'un bloc alternatif noté `alt`
  - divisé en deux parties
    - la première en haut contient la condition à respecter
    - la seconde en bas contient l'alternative
    - les deux sont séparées par une ligne pointillée
