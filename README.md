## Description du projet

Ce projet a pour objectif de démontrer un workflow DevOps simple en utilisant **Git, Docker, Docker Compose et l'intégration continue (CI/CD)**.

L'application est un **site web statique simple** servi à l'aide d'un conteneur **Nginx**.

## Technologies utilisées

* **Git** : gestion de version du projet
* **Docker** : conteneurisation de l'application
* **Docker Compose** : exécution de l'application localement avec les conteneurs
* **GitHub Actions** : mise en place du pipeline d'intégration continue

## Structure du projet

devops-final-project
│
├── website/
│   └── index.html
│
├── Dockerfile
├── docker-compose.yml
├── README.md
└── .github/workflows/ci.yml

## Lancer le projet en local

Pour lancer le projet localement, il faut avoir **Docker installé** sur la machine.

Exécuter la commande suivante :

docker compose up --build

Ensuite ouvrir le navigateur et accéder à :

http://localhost:8080

Le site web sera alors accessible depuis le conteneur Docker.

## Configuration Docker

Le projet utilise un **conteneur Nginx** pour servir le site web statique.

Le **Dockerfile** permet de :

* utiliser l'image Nginx
* copier les fichiers du site dans le conteneur
* exposer le port 80

Le fichier **docker-compose.yml** permet de construire l'image et de lancer le conteneur en redirigeant le port **8080** de la machine locale vers le port **80** du conteneur.

## Pipeline CI

Un pipeline d'intégration continue est configuré avec **GitHub Actions**.

Ce pipeline est déclenché automatiquement à chaque **push sur la branche main**.

Les étapes du pipeline sont :

1. Récupération du code du dépôt
2. Build de l'image Docker
3. Exécution de tests simulés
4. Simulation d'une étape de déploiement

## Difficultés rencontrées

Aucunes.

## Auteur

Projet réalisé dans le cadre du TP final DevOps.
