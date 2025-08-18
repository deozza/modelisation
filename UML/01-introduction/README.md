# Introduction

## Sommaire

- [Modélisation ?](#modélisation)
- [UML](#uml)
  - [Définition](#définition)
  - [2 manières d'appliquer UML](#2-manières-dappliquer-uml)
  - [Description des systèmes](#description-des-systèmes)
    - [Structurelle](#structurelle)
    - [Fonctionnelle](#fonctionnelle)

## Modélisation ?

- représentation simplifiée d'une réalité sur laquelle on veut être renseigné
- exemples : carte, plan, schéma
- servent à
  - communiquer
    - vérifier que l'analyste a compris les besoins des utilisateurs
  - préparer
    - concevoir une solution

## UML

### Définition

- fondé par l'OMG
  - Object Management Group, créé en 1989 pour promouvoir la programmation orientée objet
  - Grady Booch + Ivar Jacobson + James Rumbaugh
- Unified Modeling Language
  - > Langage visuel dédié à la spécification, la construction et la documentation des artefacts d'un système logiciel
  - **langage, pas méthode**
    - contrairement à Merise, par exemple, qui est une méthode de modélisation
- version 1.0 en 1997, version 2.5 en 2012
- devenu une standard reconnu par ISO en 2005
- utilisé pour représenter visuellement et communiquer autours de la conception de systèmes complexes
  - facilite le travail en équipe
  - simplifie la communication avec des non-développeurs
  - fait gagner du temps sur la partie conception

### 2 manières d'appliquer UML

**Esquisse :**

- brouillon, fait rapidement à la main
- pour itérer rapidement
- pour communiquer facilement entre collègues
- utilisation typique en méthode Agile

**Plan :**

- diagramme formel, normé et détaillé
- pour servir de documentation
- pour se baser dessus pendant la phase de conception

- dans les deux cas, éviter de modéliser tout un système en une seule fois
- modéliser les fonctionnalités principales d'un système
  - ou un seul domaine applicatif
- puis développer
- confirmer que tout est fonctionnel, modifier le code et les diagrammes si besoin
- recommencer

*Comme en développement classique, où on teste le plus rapidement possible si une fonctionnalité est satisfaisante, plutôt que de tout développer d'un coup et de tester à la fin.*

### Description des systèmes

![](https://media.geeksforgeeks.org/wp-content/uploads/20231222121300/UML-Diagrams.jpg)

#### Structurelle

- représentation visuelle pour dépeindre l'architecture d'une application
  - modélisation des classes, leurs relations, ...
- diagramme de classe
- diagramme de composition
- diagramme d'objet
- diagramme de composant
- diagramme de package
- diagramme de déploiement

#### Fonctionnelle

- réprésentation visuelle des intéractions entre les objets et de leurs comportements
- diagramme de machine d'états
- diagramme d'activité
- diagramme de cas d'usages
- diagramme de séquence
