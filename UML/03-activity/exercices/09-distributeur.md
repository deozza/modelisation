# Exercice 9 - distributeur de boisson

À partir des fonctionnalités suivantes, réalider le diagramme d'activité :

- afficher un message d'accueil
- rentrer le code d'une boisson
- si la boisson est dispo
  - afficher le prix
  - payer
    - si le paiement est refusé, afficher un message d'erreur puis retourner au message d'accueil
  - annuler le paiement si besoin et retourner au message d'accueil
  - distribuer la boisson puis retourner au message d'accueil
- si la boisson n'est pas dispo, afficher un message d'erreur puis retourner au message d'accueil
