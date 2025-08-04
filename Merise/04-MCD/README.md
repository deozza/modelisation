# Le Modèle Conceptuel de données

## Sommaire

- [Sommaire](#sommaire)
- [Définition](#définition)
- [Migration d'un dictionnaire de données vers un MCD](#migration-dun-dictionnaire-de-données-vers-un-mcd)
  - [Étape intermédiaire : le MLD-R](#étape-intermédiaire-le-mld-r)
  - [Les cardinalités](#les-cardinalités)

## Définition

- écriture formelle des données utilisées par le système
- représentation statique et facile à comprendre

## Migration d'un dictionnaire de données vers un MCD

- entitée
  - représentée sous forme d'un rectangle
    - en haut le nom de l'entité
    - en bas la liste des propriétés
- relation
  - représentée sous forme d'une ellipse
    - au centre le nom de la relation
    - peut contenir des propriétés
      - devient alors une entité-relation

### Étape intermédiaire : le MLD-R

- même si le MLD vient après le MCD, il peut être intéressant de faire le MLD-R ici
- permet de visualiser autrement comment les propriétés sont organisées au sein des entités et quelles sont les associations entre les entités

Exemple :

| Code mnémonique    | Désignation                         | Entité   | Type    | Taille     | Contraintes            | Remarques                |
|--------------------|-------------------------------------|----------|---------|------------|------------------------|--------------------------|
| reference          | Code d'identification du produit    | produit  | CHAR    | 50         | NOT NULL, UNIQUE       |                          |
| libelle            | Nom du produit                      | produit  | VARCHAR | 255        | NOT NULL               |                          |
| prix               | Prix hors taxe                      | produit  | FLOAT   | 11,2       | NOT NULL               |                          |
| nom                | Nom de famille                      | client   | VARCHAR | 255        | NOT NULL               |                          |
| prenom             | Prénom principal                    | client   | VARCHAR | 255        | NOT NULL               |                          |
| email              | Adresse email de contact            | client   | VARCHAR | 255        | NOT NULL, UNIQUE       | Format email à respecter |
| date               | Date de commande                    | commande | DATE    |            | NOT NULL, DEFAULT NOW()|                          | 
| commande_adresse   | Adresse de livraison                | commande | VARCHAR | 255        | NOT NULL               |                          |
| quantite           | Quantité du produit commandé        | commande | INT     | 3          | NOT NULL               | Nombre positif           |
| produit_reference  | Référence du produit commandé       | commande | CHAR    | 50         | NOT NULL               |                          |
| numero             | Numéro de la commande               | commande | INT     | 9          | NOT NULL, UNIQUE       |                          |
| client             | Email de la personne qui a commandé | commande | VARCHAR | 255        | NOT NULL               |                          |


- produit(<ins>reference</ins>, libelle, prix)
- client(<ins>email</ins>, nom, prenom)
- commande(<ins>numero</ins>, date, commande_adresse, quantite, #produit_reference, #client)

On souligne l'identifiant de l'entité et on ajoute `#` devant une propriété qui sert de passerelle pour une relation.

### Les cardinalités

Les cardinalités sont un outil permettant de comprendre les règles de gestion dans un système d'informations et d'apporter des contraintes sur les relations entre les entités. En effet, on peut savoir grâce à elles, combien d'exemplaires de l'eentité A peuvent être liés à l'entité B, et combien d'exemplaires de l'entité B peuvent être liés à l'entité A.

C'est pour cela que les cardinalités sont toujours en couples (une pour chaque côté de la relation) et avec 2 valeurs (un minimum et un maximum). En général, voici les valeurs que l'on donne aux cardinalités :

| valeurs | description                      |
| ------- | -------------------------------- |
| 0,1     | aucun ou 1 exemplaire au maximum |
| 0,N     | aucun ou plusieurs exemplaires   |
| 1,N     | au moins un exemplaire           |
| 1,1     | 1 exemplaire                     |

Exemple de MCD :

()[https://www.fsmwarden.com/developpez/Courses_Hippiques(Jockeys_etc)Merise.jpg]
