# Diagramme de classe

## Sommaire

  - [Présentation](#présentation)
  - [Construction](#construction)
    - [Classes](#classes)
      - [Accessibilité](#accessibilité)
      - [Propriété](#propriété)
      - [Méthode](#méthode)
    - [Interface](#interface)
    - [Classe abstraite](#classe-abstraite)
    - [Relations](#relations)
    
## Présentation

- représentation la plus haut niveau d'un système
- sert de modèle pour l'implémentation d'un programme en orienté objet
- permet de visualiser comment les modules d'une application intéragissent entre eux

## Construction

Exemple d'un diagramme de classes pour un système bancaire :

![](https://cdn-proxy.slickplan.com/wp-content/uploads/2025/08/banking-uml-class-diagram.jpg)


### Classes

- représentée par un rectangle divisé en 3 parties
  - le haut contient le nom de la classe
  - le milieu contient les propriétés
  - le bas contient les méthodes

#### Accessibilité

- public => `+`
- private => `-`
- protected => `#`

#### Propriété

- définie par une méthode d'accès, son  nom et son type

#### Méthode

- définie par une méthode d'accès et sa signature (nom + arguments et leurs types + type de retour)

### Interface

- représentée comme une classe mais
  - son nom est entouré par `<<>>`
  - la partie du milieu, les propriétés, est vide

### Classe abstraite

- représentée comme une classe mais
  - son nom est en *italique*

### Relations

- l'héritage est représenté par une flêche avec un trait plein
- l'implémentation est représentée par une flêche avec un trait pointillé
- relation simple est représentée par un trait plein
  - avec des cardinalités, comme dans un MLD de la méthode Merise



