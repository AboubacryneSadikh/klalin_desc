# User Stories — Portail Administrateur

Projet : klalin
Module : Portail Administrateur

---

## Épopée : Tableau de bord

### US-01 — Vue d'ensemble de l'activité
**En tant qu'** administrateur
**Je veux** voir un tableau de bord avec les statistiques globales
**Afin de** évaluer rapidement l'état de l'activité (polices, sinistres, paiements)

**Critères d'acceptation**
- Le tableau affiche : nombre de polices actives, sinistres en cours, volume de paiements
- Les chiffres sont mis à jour en temps réel ou quasi temps réel

---

## Épopée : Gestion des utilisateurs

### US-02 — Lister et gérer les utilisateurs
**En tant qu'** administrateur
**Je veux** consulter la liste des utilisateurs (clients, agents)
**Afin de** gérer les accès à la plateforme

**Critères d'acceptation**
- Je peux filtrer par type d'utilisateur et par statut de compte
- Je peux modifier ou désactiver un compte
- Toute suppression de compte demande une confirmation explicite

---

### US-03 — Consulter le détail d'un utilisateur
**En tant qu'** administrateur
**Je veux** voir les polices, sinistres, paiements et informations personnelles liés à un utilisateur
**Afin de** avoir une vision complète en cas de litige ou de demande spécifique

**Critères d'acceptation**
- Toutes les données affichées sont limitées à ce qui est nécessaire (principe de minimisation des données)
- L'accès à cette page est journalisé (traçabilité RGPD)

---

## Épopée : Supervision des polices et sinistres

### US-04 — Superviser l'ensemble des polices
**En tant qu'** administrateur
**Je veux** avoir une vue globale et des droits de création/modification/suppression sur toutes les polices
**Afin de** intervenir en cas de besoin, au-delà des droits d'un agent standard

**Critères d'acceptation**
- Les actions administratives sont distinguées des actions d'un agent standard dans les journaux d'audit

---

### US-05 — Superviser l'ensemble des sinistres
**En tant qu'** administrateur
**Je veux** filtrer, modifier le statut et commenter n'importe quel sinistre
**Afin de** débloquer des dossiers complexes ou litigieux

**Critères d'acceptation**
- Je peux réassigner un sinistre à un autre gestionnaire
- Les changements que j'effectue apparaissent dans l'historique du dossier avec mon identité

---

## Épopée : Reporting

### US-06 — Consulter des rapports et statistiques
**En tant que** manager/superviseur métier
**Je veux** accéder à des rapports sur les sinistres, primes et tendances
**Afin de** prendre des décisions stratégiques (ajustement tarifaire, allocation de ressources)

**Critères d'acceptation**
- Je peux filtrer les rapports par période, type de police, région
- Les rapports sont exportables (PDF ou Excel)

---

## Épopée : Configuration système

### US-07 — Paramétrer l'application
**En tant qu'** administrateur système
**Je veux** configurer les options globales (taxes, rôles, notifications)
**Afin de** adapter la plateforme aux règles métier de l'entreprise

**Critères d'acceptation**
- Toute modification de paramètre global nécessite les droits d'administrateur
- Un historique des changements de configuration est conservé

---

### US-08 — Gérer les notifications
**En tant qu'** administrateur
**Je veux** configurer et envoyer des notifications aux clients et administrateurs
**Afin de** communiquer efficacement (ex. alerte suite à un sinistre climatique de masse)

**Critères d'acceptation**
- Je peux cibler une notification par segment (tous les clients, une région, un type de police)
- Je peux prévisualiser le message avant envoi
- Un envoi groupé est confirmé avant déclenchement définitif

---

## Notes de priorisation suggérées

| Story | Priorité | Justification |
|---|---|---|
| US-01, US-02 | Haute | Fondation opérationnelle du portail |
| US-04, US-05 | Haute | Supervision indispensable dès le lancement |
| US-03, US-07 | Moyenne | Nécessaires mais moins fréquentes au quotidien |
| US-06, US-08 | Moyenne | Valeur stratégique, non bloquant en V1 |
