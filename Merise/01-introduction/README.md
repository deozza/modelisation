# Introduction

## Sommaire

<!--toc:start-->
- [Méthode d'informatisation universelle](#méthode-dinformatisation-universelle)
- [Modélisation ?](#modélisation)
- [Merise](#merise)
  - [Définir les besoins utilisateurs](#définir-les-besoins-utilisateurs)
  - [Vérifier la cohérence de la demande](#vérifier-la-cohérence-de-la-demande)
  - [Structure les données à informatiser](#structure-les-données-à-informatiser)
  - [Rester simple et une aide à la conception](#rester-simple-et-une-aide-à-la-conception)
<!--toc:end-->

## Méthode d'informatisation universelle

- méthode informatique de modélisation, de conception, d'analyse
- doit pouvoir :
  - définir les besoins utilisateurs
  - vérifier la cohérence de la demande
  - structurer les données à informatiser
  - rester simple et une aide à la conception

## Modélisation ?

- représentation simplifiée d'une réalité sur laquelle on veut être renseigné
- exemples : carte, plan, schéma
- servent à
  - communiquer
    - vérifier que l'analyste a compris les besoins des utilisateurs
  - préparer
    - concevoir une solution

## Merise

- méthode française mise au point en 1979
- adoptée et utilisée par les organisations gouvernementales, commerciales et industrielles
- basée sur le modèle `entité-relation`
- traitement des données et des processus
  - 3 phases de traitement des données :
    - modèle conceptuel de données (MCD)
    - modèle logique de données (MLD)
    - modèle physique de données (MPD)
- viable peu importe les technologies et les applications
- reste une abstraction
  - pas d'interface, d'UI, d'UX
  - pas de vérification directe des fonctionnalités
  - pas de vérification directe des flux de données

### Définir les besoins utilisateurs

- on recueille l'expression des besoins afin de connaître quelles données vont être manipulées dans le système
- on ne commence même pas à maquetter avant de valider les données à traiter

### Vérifier la cohérence de la demande

- définition des fonctions couvertes par le métier
  - donc définition des limites du projet, ce qu'il fera et ce qu'il ne fera pas
- définitions des processus de traitement
  - à quel moment telle donnée est créée, par qui, pour quoi, qu'est-ce qui est nécessaire pour sa création

### Structure les données à informatiser

- appliquer une méthode graphique pour grouper les types de données par catégorie, les représenter, mettre des liens entre elles
- abstraction pour se détacher du réel et pouvoir couvrir le plus de cas métiers possibles

### Rester simple et une aide à la conception

- développer prend du temps
- modifier une application prend encore plus de temps
- modéliser est rapide et permet d'augmenter les chances de concevoir correctement du premier coup
- permet de concentrer une grande partie de la réflexion à une étape où
  - le projet vient de démarrer
  - il y a très peu de dépendances
  - c'est facile et peu coûteux de modifier et recommencer
- servira de base pour la conception de l'application et de son architecture
