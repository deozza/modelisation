# Exercice 18 - formulaire de contact

Réaliser le diagramme de séquence pour la page de contact d'un site web.

- une personne rentre ses informations (email, objet et contenu du message) sur le formulaire html
- le formulaire envoie ce payload au ContactController, dans le backend
- le ContactController fait appel au ContactForm pour valider que le formulaire soit valide
- s'il n'est pas valide, le ContactController envoie un message HTTP 400 à la page html, qui affiche l'erreur
- s'il est valide, le ContactController envoie ces données au MailService pour créer un email
- une fois le mail créé, le MailService contacte un serveur SMTP pour l'envoyer
- chaque module remonte un message de succès, jusqu'à la page html qui affiche la confirmation d'envoi d'email
