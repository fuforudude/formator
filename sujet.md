# Sujet — Application de gestion d’activité pédagogique

## Contexte

Le projet consiste à développer une application permettant à un intervenant/formateur indépendant de centraliser la gestion de son activité pédagogique et administrative avec plusieurs écoles.

L’objectif principal est de simplifier :
- l’organisation des cours,
- la gestion des prestations,
- la facturation,
- la centralisation documentaire,
- le suivi administratif.

Le sujet met l’accent sur :
- l’analyse du besoin,
- la priorisation,
- la cohérence fonctionnelle,
- l’organisation du projet,
- la qualité de l’architecture.

Le projet ne doit PAS être un ERP complet.

---

# Problématique

Actuellement, les informations sont réparties entre plusieurs outils :
- Outlook
- Teams
- Notion
- fichiers locaux
- NAS Synology
- plateformes des écoles
- documents administratifs

Cela entraîne :
- perte de temps,
- double saisie,
- manque de visibilité,
- oublis de facturation,
- difficulté de suivi.

L’application doit permettre de centraliser les informations importantes dans une interface unique.

---

# Objectifs principaux

L’application doit permettre :
- de gérer les écoles,
- d’organiser les cours,
- de suivre les prestations réalisées,
- de gérer les factures,
- de centraliser les documents,
- d’avoir une vision claire de l’activité.

---

# Fonctionnalités retenues pour le MVP

## Gestion des écoles
- création d’école
- modification d’école
- suppression d’école
- fiche école détaillée
- contacts administratifs
- notes internes

## Gestion des cours
- création de cours
- modification de cours
- suppression de cours
- association à une école
- planning/calendrier
- durée et horaires

## Gestion des prestations
- suivi des heures réalisées
- statut des prestations :
  - prévu
  - réalisé
  - facturé
  - payé

## Facturation
- génération de factures
- export PDF
- suivi des paiements
- visualisation des prestations non facturées

## Gestion documentaire
- upload de documents
- stockage local
- association des documents :
  - écoles
  - cours
  - factures

## Dashboard
- cours à venir
- factures impayées
- statistiques simples

---

# Fonctionnalités volontairement exclues

Les fonctionnalités suivantes ne sont PAS intégrées afin de conserver un périmètre réaliste :

- gestion avancée des étudiants
- système de notes
- suivi pédagogique détaillé
- gestion des absences
- synchronisation complexe avec plateformes externes
- temps réel
- multi-utilisateurs avancé
- notifications complexes

---

# Architecture technique

## Frontend
- React
- TypeScript
- TailwindCSS

## Backend
- NestJS
- API REST
- JWT Authentication

## Base de données
- PostgreSQL

## Infrastructure
- Docker
- docker-compose

---

# Architecture applicative

Architecture monolithique modulaire :
- frontend React séparé
- backend NestJS séparé
- communication REST API

Le projet doit privilégier :
- simplicité,
- maintenabilité,
- modularité,
- rapidité de développement.

---

# Contraintes

- un seul utilisateur administrateur
- application web responsive
- stockage local des fichiers
- architecture claire et propre
- MVP réaliste
- code maintenable

---

# Livrables attendus

- application fonctionnelle
- backend API REST
- frontend React
- base PostgreSQL
- environnement Docker
- documentation minimale
- démonstration du projet

---

# Philosophie du projet

Le projet doit démontrer :
- une bonne compréhension du besoin,
- une capacité de priorisation,
- une architecture cohérente,
- une implémentation réaliste,
- une bonne organisation technique.

L’objectif n’est pas de développer une solution exhaustive mais une solution cohérente et défendable.