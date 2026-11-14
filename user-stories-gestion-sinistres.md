# User Stories — Module de Gestion des Sinistres

Projet : klalin
Module : Gestion des Sinistres

---

## Épopée : Déclaration d'un sinistre

### US-01 — Déclarer un nouveau sinistre
**En tant qu'** assuré
**Je veux** déclarer un sinistre lié à ma police
**Afin de** initier une demande de règlement

**Critères d'acceptation**
- Le formulaire demande : police concernée, type de sinistre, description, date de l'incident
- Je peux télécharger des documents justificatifs (photos, rapports)
- Un numéro de dossier unique est généré à la soumission
- Une confirmation (écran + email) est envoyée après déclaration
- Je ne peux déclarer un sinistre que sur une police active dont je suis titulaire

---

## Épopée : Instruction du dossier

### US-02 — Vue d'ensemble des sinistres
**En tant que** gestionnaire de sinistres
**Je veux** consulter la liste des sinistres déclarés avec leur statut
**Afin de** prioriser mon travail d'instruction

**Critères d'acceptation**
- Filtrage par statut : en cours, réglé, refusé
- Tri par date de déclaration, par urgence, par montant estimé
- Recherche par numéro de dossier ou nom d'assuré

---

### US-03 — Consulter le détail d'un sinistre
**En tant que** gestionnaire de sinistres
**Je veux** voir l'historique complet des actions sur un dossier
**Afin de** comprendre où en est le traitement sans avoir à interroger un collègue

**Critères d'acceptation**
- L'historique affiche chronologiquement : réception, enquête, décisions, échanges
- Les documents fournis par l'assuré sont accessibles depuis cette page
- Je peux ajouter un commentaire interne visible par l'équipe

---

### US-04 — Mettre à jour le statut d'un sinistre
**En tant que** gestionnaire de sinistres
**Je veux** faire évoluer le statut d'un dossier (en cours → réglé/refusé)
**Afin de** refléter l'avancement réel du traitement

**Critères d'acceptation**
- Chaque changement de statut nécessite un commentaire explicatif
- Le client est notifié automatiquement lors d'un changement de statut
- Un refus doit obligatoirement être justifié avant validation

---

## Épopée : Règlement financier

### US-05 — Gérer le paiement d'un sinistre
**En tant que** gestionnaire de sinistres
**Je veux** déclencher ou suivre le paiement lié à un sinistre validé
**Afin de** indemniser l'assuré

**Critères d'acceptation**
- Je peux saisir le montant du règlement et déclencher le paiement
- Le statut du paiement (en attente, effectué) est visible sur le dossier
- Au-delà d'un certain montant, une validation par un administrateur est requise
- L'assuré reçoit une notification lorsque le paiement est effectué

---

## Épopée : Suivi côté client

### US-06 — Suivre l'avancement de mon sinistre
**En tant qu'** assuré
**Je veux** consulter le statut de mon sinistre déclaré
**Afin de** savoir où en est mon dossier sans avoir à appeler l'assurance

**Critères d'acceptation**
- Le statut affiché correspond en temps réel à celui du back-office
- Je vois les grandes étapes (reçu, en cours d'instruction, décision) sans le détail interne sensible
- Je peux consulter l'historique de tous mes sinistres passés

---

## Notes de priorisation suggérées

| Story | Priorité | Justification |
|---|---|---|
| US-01 | Haute | Point d'entrée du module, condition de tout le reste |
| US-02, US-03 | Haute | Indispensables pour l'instruction quotidienne |
| US-04 | Haute | Cœur du workflow métier |
| US-05 | Moyenne | Peut s'appuyer sur un processus manuel en V1 |
| US-06 | Moyenne | Valeur ajoutée client, non bloquant pour le back-office |
