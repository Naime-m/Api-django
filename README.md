# api-django-rest

Ce projet vise à créer une API pour gérer des produits, mettre en place un système d'authentification et permettre la gestion des utilisateurs avec différentes autorisations.

## CRUD sur les produits

Dans cette partie, l'API offre les fonctionnalités suivantes pour la gestion des produits :

- **GET /products** : Récupère la liste des produits.
  - Accessible à tous.

- **GET /products/{id}** : Récupère les détails d'un produit spécifique.
  - Accessible à tous.

- **POST /products** : Crée un produit.
  - Accessible uniquement à l'administrateur.

- **UPDATE /products/{id}** : Modifie un produit existant.
  - Accessible uniquement à l'administrateur.

- **DELETE /products/{id}** : Supprime un produit.
  - Accessible uniquement à l'administrateur.

## Authentification

Cette partie concerne la gestion de l'authentification des utilisateurs avec les requêtes suivantes :

- **POST /login** : Permet de s'authentifier et renvoie un token JWT.
  - Accessible à tous.
  - Le token JWT contient l'identifiant de l'utilisateur connecté.
  - Le token JWT a une durée de vie spécifiée.

## CRUD sur les utilisateurs

Cette section permet la gestion des utilisateurs avec les fonctionnalités suivantes :

- **GET /users** : Récupère la liste des utilisateurs.
  - Accessible à l'administrateur.

- **GET /users/{id}** : Récupère les détails d'un utilisateur spécifique.
  - Accessible à l'administrateur ou à l'utilisateur lui-même.

- **POST /users** : Crée un utilisateur.
  - Accessible à tous.
  - Si un utilisateur crée son compte, il n'a pas le choix du rôle.

- **UPDATE /users/{id}** : Modifie un utilisateur.
  - Accessible à l'administrateur ou à l'utilisateur lui-même.

- **DELETE /users/{id}** : Supprime un utilisateur.
  - Accessible à l'administrateur ou à l'utilisateur lui-même.
