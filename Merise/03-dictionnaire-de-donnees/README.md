# Le dictionnaire de données

Le dictionnaire de données est une première étape dans la modélisation d'un système et de sa base de données. En partant d'un cahier des charges, il permet de lister les propriétés, leurs configurations ainsi que les entités qui seront manipulées dans le système.

Il n'a pas de forme normée à respecter. Cependant, on retrouve assez souvent les colonnes :

- propriété
  - le nom d'une propriété que le système doit gérer
- commentaire
  - des informations de configuration supplémentaires (format d'une date, foreign key, not null, ...)
- entité
  - à quelle entité cette propriété se rattache
- type
  - quel est le type (VARCHAR, INT, DATE, BOOLEAN, FLOAT, ...) de la propriété
- identifiant
  - est-ce que la propriété est une PRIMARY KEY ou non.

Exemple :

| Propriété | Commentaire | Entité   | Type     | Identifiant |
|-----------|-------------|----------|----------|-------------|
| reference |             | produit  | VARCHAR  | X           |
| libelle   |             | produit  | VARCHAR  |             |
| prix      |             | produit  | FLOAT    |             |
| identite  |             | client   | INT      | X           |
| nom       |             | client   | VARCHAR  |             |
| prenom    |             | client   | VARCHAR  |             |
| adresse   |             | client   | VARCHAR  |             |
| date      |             | commande | DATETIME |             |
| adresse   |             | commande | VARCHAR  |             |
| quantite  |             | commande | INT      |             |
| identite  | FOREIGN KEY | commande | INT      |             |
| reference | FOREIGN KEY | commande | VARCHAR  |             |
| numero    |             | commande | INT      | X           |
