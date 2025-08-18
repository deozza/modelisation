# Diagrame d'état machine

## Sommaire

- [Machine d'état fini](#machine-détat-fini)
  - [Machine d'état déterministique](#machine-détat-déterministique)
  - [Intérêt en développement](#intérêt-en-développement)
- [Présentation](#présentation)

## Machine d'état fini

- *finite state machine (FSM)*, automate (d'état) fini, ...
- abstraction mathématique pour concevoir des algorithmes
- fonctionnement :
  - définit avec un état par défaut
  - lit un input (*reçoit un évènement*)
  - selon l'input, va changer l'état courrant
- la FSM n'a pas de fonctionnalité propre
  - le reste de l'application se base sur l'état courrant de la FSM pour activer ou modifier ses fonctionnalités

![](https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_80/w_2000/https://archive.smashing.media/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2f37efe-a89c-48fd-9176-f289aa05ccd6/sm-high-res-opt.jpg)

### Machine d'état déterministique

- il n'y a qu'une seule transition possible d'un état à un autre par évènement
- une FSM avec plusieurs transitions est non-déterministique
  - pour savoir quelle transition suivre et quel nouvel état appliquer, on teste toutes les possibilités
  - possible de transformer une FSM non-déterministique en déterministique en rajoutant des transitions et des états intérmédiaires

### Intérêt en développement

- plutôt que d'avoir une liste de booleans pour déterminer l'état actuel du système
- utile pour modéliser un workflow
  - e-commerce, distributeur automatique de billet, formulaire de contact, ...
- utile en développement de jeux vidéos
  - pour autoriser certaines input des joueur.ses
  - pour déterminer le comportement d'un NPC

## Présentation

- même chose que le diagramme d'activité
  - peut ne pas avoir d'état final
    - puisque la FSM s'exécute en parallèle du programme

![](https://sparxsystems.com/images/screenshots/uml2_tutorial/sm01.GIF)
