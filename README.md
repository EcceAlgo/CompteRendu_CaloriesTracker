# CompteRendu_CaloriesTracker

# Introduction

## Presentation du projet
## Objectifs du projet
## Contexte et justification

# Analyse des besoins

## Identification des besoins des utilisateurs

Une enquête approfondie auprès des utilisateurs potentiels a permis de définir les principaux besoins et attentes des utilisateurs pour l'application "Calories Tracker" :

Suivi précis des calories : Les utilisateurs souhaitent une interface conviviale et précise pour enregistrer leur consommation alimentaire quotidienne et suivre leur apport calorique.

Calcul automatique des valeurs nutritionnelles : Les utilisateurs attendent une fonctionnalité qui calcule automatiquement les valeurs nutritionnelles des aliments enregistrés, y compris les calories, les protéines, les glucides, les lipides, etc.

Personnalisation des objectifs de santé : Les utilisateurs désirent la possibilité de définir et de suivre des objectifs de santé personnalisés, tels que les objectifs caloriques quotidiens et les ratios de macronutriments.

Visualisation des données et des tendances : Les utilisateurs recherchent des graphiques interactifs et des tableaux de bord pour visualiser leurs données de consommation alimentaire, ainsi que des tendances et des analyses pour suivre leur progression.

Gestion des utilisateurs et des profils : Les utilisateurs attendent une fonctionnalité de gestion des profils qui leur permet de créer, de modifier et de supprimer des profils utilisateurs, avec la possibilité de personnaliser leurs préférences individuelles.

## Analyse des fonctionnalités requises

Sur la base des besoins identifiés, voici la liste des fonctionnalités requises pour l'application "Calories Tracker" :

Interface utilisateur intuitive pour l'enregistrement des repas et des collations, avec validation en temps réel et suggestions d'aliments.

Calcul automatique des valeurs nutritionnelles des aliments enregistrés, avec présentation claire des informations nutritionnelles.

Fonctionnalité de personnalisation des objectifs de santé pour chaque utilisateur, avec suivi de la progression et des recommandations personnalisées.

Visualisation des données de consommation alimentaire à l'aide de graphiques interactifs et de tableaux de bord, permettant aux utilisateurs d'analyser leurs habitudes alimentaires et leur progression vers leurs objectifs.

Gestion des profils utilisateurs, y compris la création, la modification et la suppression de profils individuels, ainsi que la gestion des préférences et des paramètres.

## Étude de faisabilité technique

Une étude de faisabilité technique a été réalisée pour évaluer la viabilité de la mise en œuvre des fonctionnalités requises dans le cadre du projet, en utilisant NestJS avec TypeScript pour le backend et React.js avec TypeScript pour le frontend. Les principaux aspects techniques comprennent :

### Intégration entre NestJS et React.js:

Évaluation des meilleures pratiques pour l'intégration entre le backend et le frontend, en utilisant des API RESTful ou des méthodes de communication en temps réel comme WebSocket.

### Choix des bibliothèques et des outils :

Sélection des bibliothèques et des outils appropriés pour le développement frontend avec React.js et TypeScript, en mettant l'accent sur la productivité, la performance et la maintenabilité du code.

### Sécurité et confidentialité des données : 

Identification des mesures de sécurité nécessaires pour protéger les données sensibles des utilisateurs, y compris le chiffrement des données et la gestion sécurisée des identifiants d'authentification.

Sur la base de cette étude de faisabilité, il a été conclu que l'utilisation de NestJS avec TypeScript pour le backend et de React.js avec TypeScript pour le frontend est une approche solide et réalisable pour le développement de l'application "Calories Tracker".

# Analyse des risques

# Planification 

# Stratégie de Sécurisation de l'Application CaloriesTracker

La partie sécurité de notre application CaloriesTracker est listé sur 3 axes primordiaux de protection.

Cette application a pour but de venir en aide à toutes les personnes souhaitant atteindre leurs objectifs physiques.

## Les 3 Grands Axes

Les trois grands axes sur lesquels nous allons nous concentrer aujourd’hui sont :
- La protection des données personnelles.
- L’identification.
- La protection de la partie client.

## La Mise en Place

### La Protection des Données Personnelles

- Utiliser le principe de Moindre Privilège (pour limiter les vols ainsi que la destruction de données).
- HTTPS (pour sécuriser les échanges de données).
- CSP (permet de sécuriser les échanges avec l’API).

### La Sécurité Liée aux Mots de Passe

- Interdire l’accès après trop de tentatives échouées (8) de mots de passe pour contrer les attaques en ligne.
- Hacher le mot de passe ainsi que rajouter un salage pour contrer les attaques hors ligne.
- Utiliser des caractères spéciaux dans les mots de passe pour contrer les attaques par dictionnaire.
- Utiliser un canal sécurisé comme un flux encapsulé pour un protocole TLS pour contrer les attaques par l'homme du milieu.
- Complexité et longueur minimale requises.
- Notifications d’activités suspectes.

### La Sécurité Liée à l’Expérience Utilisateur

- Défense en profondeur.
- Réduction de la surface d’attaques.
- HSTS (pour limiter les risques d’attaque ‘man in the middle‘).
- SOP
- CORS
- Utilisation de la balise HTML `<template>` contre les vulnérabilités XSS.
- Dissocier clairement la composition des pages web (HTML, CSS, JAVASCRIPT).
- Utiliser le X-XSS protection 
- Utiliser XMLHttpRequest (pour encoder)
- Choisir une API selon sa méthode HTTP
- Audit.

## Éléments Supplémentaires pour une Stratégie de Sécurisation

- Mettre en place une politique de gestion des identités et des accès (IAM).
- Effectuer régulièrement des tests de pénétration et des audits de sécurité.
- Mettre en place un système de surveillance et d'alerte en cas d'activité suspecte.
- Former le personnel sur les meilleures pratiques de sécurité et la sensibilisation aux menaces.
- Maintenir une veille technologique constante pour rester à jour sur les nouvelles vulnérabilités et les meilleures pratiques de sécurité.

### Gestion des Vulnérabilités

- Mettre en place un processus de gestion des vulnérabilités pour identifier, évaluer et traiter les failles de sécurité dès leur découverte.
- Assurer la veille sur les bases de données de vulnérabilités et les alertes de sécurité pour rester informé des menaces émergentes.

### Gestion des Logs

- Mettre en place un système de journalisation (logs) pour enregistrer les événements de l'application, afin de faciliter la détection et l'investigation des incidents de sécurité.
- Définir une politique de rétention des logs pour garantir la disponibilité des données nécessaires à l'analyse des incidents.

### Protection contre les Attaques par Déni de Service (DDoS)

- Mettre en place des mesures de protection contre les attaques par déni de service (DDoS), telles que la limitation des requêtes par IP, la mise en cache des ressources, ou l'utilisation de services de protection DDoS tiers.

### Gestion des Sessions Utilisateurs

- Implémenter des mécanismes de gestion des sessions utilisateurs, tels que l'expiration automatique des sessions après une période d'inactivité, et la ré-authentification périodique.

### Chiffrement des Données Sensibles

- Appliquer le chiffrement des données sensibles au repos et en transit, en utilisant des algorithmes cryptographiques robustes et des protocoles sécurisés.

### Sécurisation des Déploiements et des Environnements

- Mettre en œuvre des pratiques de sécurisation des déploiements et des environnements, telles que la segmentation réseau, la gestion des configurations sécurisées, et la supervision des activités système.


# Conception

## Architecture générale de l'application
## Conception de l'interface utilisateur (UI)
## Modèle de données et structure de la base de données
## Choix technologiques et justification

# Implementation

## Développement du BackEnd
## Développement du FrontEnd
## Intégration avec la base de données PostgreSQL
## Fonctionnalités clés implémentées

# Tests

## Stratégie de tests adoptées
## Résultats des test et couverture du code
## Actions correctives suite aux tests

# Déploiement et maintenance

## Processus de déploiement de l'application
## Gestion des mises à jour et de la maintenance continue
## Suivi des performances et optimisations réalisées


# Conclusion

## Récapitulatif des réalisations du projet
## Enseignements tirés et recommandations pour des futurs projets similaires

# Annexes

## Diagrammes de classe et de sequence
## Captures d'écran de l'application
## Code source
