# Exercice 17 - page de login

Réaliser le diagramme de séquence pour la page de connexion d'un site web.

- une personne rentre ses informations (email et mot de passe) sur le formulaire html
- la page html envoie une requête POST au controlleur LoginController, contenant les informations de connexion
- le controlleur utilise le UserRepository pour pouvoir récupérer un User avec l'email correspondant
- le UserRepository fait une requête SQL à la base de données
- si un User n'est pas trouvé, le controlleur envoie une réponse HTTP 400 à la page html, qui affiche l'erreur
- sinon, le controlleur vérifie si le mot de passe du User en base de données correspond avec ce qui a été envoyé par le formulaire
- si ils sont différents, le controlleur envoie une réponse HTTP 400 à la page html, qui affiche l'erreur
- sinon, le controlleur crée un token d'authentification, l'envoie à la page html, et la page html affiche un message de bienvenue
