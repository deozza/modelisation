# Le dictionnaire de données

## Sommaire

- [Définition](#définition)
- [Application](#application)

## Définition

- inventaire exhaustif, à faire après l'expression du besoin
- document regroupant toutes les données à manipuler dans un système
- permet de définir ces données
  - faire une passerelle entre le métier et la technique
  - défition unique pour toute l'organisation

## Application

- sous forme d'un tableau
- le format n'est pas vraiment normé
- certaines caractéristiques sont présentes de manière générale :
  - `code mnémonique` : le libellé, le nom de la donnée
  - `désignation` (optionnel) : description de la donnée, à quoi elle correspond
  - `entité` (optionnel) : à quelle entité se rattache cette propriété
  - `type` : varchar, int, ...
  - `taille` : nombre de caractères, nombre de chiffres, ...
  - `remarques` : d'autres caractéristiques (strictement supérieur à 0, format à respecter, ...)
  - `contraintes` (parfois dans `remarques`) : options comme `NOT NULL`, `UNIQUE`, ...

Exemple de dictionnaire :

| Code mnémonique | Désignation                      | Entité  | Type    | Taille | Contraintes      | Remarques                |
|-----------------|----------------------------------|---------|---------|--------|------------------|--------------------------|
| reference       | Code d'identification du produit | produit | CHAR    | 50     | NOT NULL, UNIQUE |                          |
| libelle         | Nom du produit                   | produit | VARCHAR | 255    | NOT NULL         |                          |
| prix            | Prix hors taxe                   | produit | FLOAT   | 11,2   | NOT NULL         |                          |
| nom             | Nom de famille                   | client  | VARCHAR | 255    | NOT NULL         |                          |
| prenom          | Prénom principal                 | client  | VARCHAR | 255    | NOT NULL         |                          |
| email           | Adresse email de contact         | client  | VARCHAR | 255    | NOT NULL, UNIQUE | Format email à respecter |

- les données doivent être élémentaires
  - ne doivent pas être calculées
    - sauf si la valeur ne varie pas dans le temps
    - exemple : pas d'âge, on stocke une date de naissance, mais prix TTC ok
  - ne doivent pas être composées
    - plus simple de modifier une valeur élémentaire courte qu'une valeur composée longue
    - exemple : on ne stocke pas une adresse complète, mais un numéro de rue + le nom de la rue + ...
