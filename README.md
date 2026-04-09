# moto-trip

## Contexte de l’application : MotoTrip

Vous travaillez sur une application appelée MotoTrip, une plateforme dédiée à l’organisation de balades moto entre passionnés.

L’objectif de cette application est de permettre à des utilisateurs de créer et rejoindre des trajets (trips), tout en respectant certaines règles métier liées à la capacité, au statut premium et au déroulement des événements.

---

## Gestion des utilisateurs

Un utilisateur possède :
- un nom
- un statut premium (oui/non)
- un nombre de points

Les points sont attribués automatiquement lorsqu’un utilisateur participe à un trajet.

---

## Gestion des trajets (Trips)

Un trajet est défini par :
- un nom
- une capacité maximale de participants
- une restriction éventuelle aux utilisateurs premium
- un état (démarré ou non)
- une liste de participants

---

## Fonctionnalités principales

L’application permet de :

### 1. Créer des utilisateurs
- avec ou sans statut premium

### 2. Créer des trajets
- avec une capacité définie
- éventuellement réservés aux utilisateurs premium

### 3. Rejoindre un trajet
- un utilisateur peut rejoindre un trajet si :
  - le trajet n’est pas complet
  - le trajet n’a pas déjà commencé
  - les conditions premium sont respectées
- lorsqu’un utilisateur rejoint un trajet, il gagne des points

### 4. Démarrer un trajet
- un trajet peut être démarré uniquement s’il contient au moins un participant
- une fois démarré, aucun nouvel utilisateur ne peut rejoindre

### 5. Consulter les trajets
- récupérer la liste des trajets existants

---

## Règles métier importantes

- Un trajet ne peut pas dépasser sa capacité maximale
- Un utilisateur non premium ne peut pas rejoindre un trajet premium
- Un trajet démarré est verrouillé (plus de participants)
- Un trajet sans participant ne peut pas être démarré
- Une capacité de trajet invalide (≤ 0) doit être rejetée
- Un utilisateur ou un trajet inexistant doit générer une erreur

---

## Objectif de l’examen

Le code de l’application vous est fourni.

Votre objectif est de concevoir et implémenter une stratégie de test complète, couvrant :

- les tests unitaires
- les tests d’intégration (avec base H2)
- les tests API REST
- les tests end-to-end (E2E)

Vous ne devez pas modifier le code métier, uniquement écrire les tests.

---
