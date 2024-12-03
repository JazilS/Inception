# Inception - 42cursus

## Description
Le projet **Inception** est conçu pour vous permettre d'approfondir vos connaissances sur **Docker** en virtualisant plusieurs images Docker et en les orchestrant avec **docker-compose**. Vous allez créer une mini-infrastructure composée de différents services, dont NGINX, WordPress avec php-fpm et MariaDB, tout en respectant des consignes strictes de sécurité et de bonnes pratiques Docker.

---

## Objectifs du projet

Le but de ce projet est de configurer et de déployer une architecture de services conteneurisés. Les services suivants devront être configurés dans des containers Docker :

1. **NGINX** : Un container Docker contenant NGINX avec **TLSv1.2** ou **TLSv1.3**.
2. **WordPress + php-fpm** : Un container Docker contenant **WordPress** et **php-fpm**, sans NGINX.
3. **MariaDB** : Un container Docker contenant **MariaDB**, sans NGINX.
4. **Volumes Docker** :
   - Un volume pour la base de données WordPress.
   - Un volume pour les fichiers de votre site WordPress.
5. **Réseau Docker** : Un réseau personnalisé pour interconnecter tous les containers.

---

## Prérequis

- Utilisation obligatoire de **docker-compose** pour gérer les services.
- Chaque service doit être dans un container dédié.
- Utilisation des bonnes pratiques Docker, comme la gestion des **variables d'environnement** et **Docker secrets**.
- Configuration d'un fichier `.env` pour stocker les variables sensibles.
- Le projet doit être réalisé dans une **machine virtuelle**.

---

## Fonctionnalités principales

- **NGINX en tant que point d'entrée sécurisé** : Le container NGINX doit être configuré pour n’accepter que les connexions via TLSv1.2 ou TLSv1.3 sur le port 443.
- **Configuration des utilisateurs WordPress** : L’admin WordPress ne doit pas avoir un nom d'utilisateur comportant "admin" ou "Admin".
- **Pas de mots de passe dans les Dockerfiles** : Toutes les informations sensibles doivent être stockées dans des fichiers `.env` et **Docker secrets**.

---
