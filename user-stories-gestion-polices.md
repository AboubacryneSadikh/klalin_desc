# User Stories — Module de Gestion des Polices d'Assurance

Projet : klalin
Module : Gestion des Polices d'Assurance

---

## Épopée : Consultation des polices

### US-01 — Vue d'ensemble des polices
**En tant qu' agent/gestionnaire de contrats
**Je veux consulter la liste de toutes les polices d'assurance existantes
**Afin de avoir une vue globale de mon portefeuille de contrats

**Critères d'acceptation**
- La liste affiche au minimum : numéro de police, client, type de police, statut, date d'échéance
- Je peux filtrer par type de police, statut et client
- Je peux trier chaque colonne (ordre croissant/décroissant)
- Je peux rechercher une police par mot-clé (nom client, numéro de police)
- La liste est paginée au-delà de 50 résultats

---

### US-02 — Détail d'une police
**En tant qu' agent/gestionnaire de contrats
**Je veux consulter le détail complet d'une police spécifique
**Afin de disposer de toutes les informations nécessaires pour répondre à une demande client

**Critères d'acceptation**
- La page affiche : informations client, type de police, montant assuré, durée, conditions de couverture
- L'historique des paiements associés à la police est visible
- Je peux naviguer directement vers les sinistres liés à cette police, s'il en existe
- Un message clair s'affiche si la police n'existe pas ou a été supprimée

---

## Épopée : Création et modification

### US-03 — Création d'une nouvelle police
**En tant qu' agent commercial
**Je veux créer une nouvelle police d'assurance pour un client
**Afin de finaliser une souscription

**Critères d'acceptation**
- Le formulaire demande : informations client, type de police, couverture, montant assuré, durée
- Les champs obligatoires sont validés avant soumission (impossible de créer une police incomplète)
- Un message de confirmation s'affiche après création réussie
- La nouvelle police apparaît immédiatement dans la liste des polices
- En cas d'erreur serveur, l'agent reçoit un message explicite et ses saisies ne sont pas perdues

---

### US-04 — Modification d'une police existante
**En tant qu' agent/gestionnaire de contrats
**Je veux modifier les informations d'une police existante
**Afin de refléter un changement (renouvellement, ajustement de couverture, mise à jour client)

**Critères d'acceptation**
- Le formulaire est pré-rempli avec les données actuelles de la police
- Je peux modifier les termes de la police (couverture, montant, durée)
- Les modifications sont historisées (traçabilité de qui a modifié quoi et quand)
- Une confirmation est demandée avant l'enregistrement des changements
- Le client concerné voit la mise à jour reflétée sur son portail

---

## Épopée : Suppression

### US-05 — Suppression d'une police
**En tant qu' administrateur
**Je veux supprimer une police d'assurance
**Afin de retirer un contrat qui n'est plus valide (erreur de saisie, annulation, fraude)

**Critères d'acceptation**
- Une confirmation explicite est demandée avant suppression, avec avertissement sur l'irréversibilité
- Si la police a des sinistres actifs liés, un avertissement supplémentaire s'affiche
- Seuls les utilisateurs avec les droits appropriés (administrateur/gestionnaire habilité) peuvent supprimer une police
- Une trace de l'action est conservée (qui, quand, quelle police) à des fins d'audit

---

## Épopée : Accès restreint et sécurité

### US-06 — Contrôle des droits d'accès
**En tant qu' administrateur système
**Je veux que seuls les utilisateurs autorisés puissent créer, modifier ou supprimer une police
**Afin de garantir l'intégrité des données contractuelles

**Critères d'acceptation**
- Un client ne peut consulter que ses propres polices, jamais celles des autres
- Un agent ne peut pas supprimer une police sans droit d'administration
- Toute tentative d'accès non autorisé est journalisée
- Un message d'erreur clair (403) s'affiche en cas d'accès refusé

---

## Notes de priorisation suggérées

| Story | Priorité | Justification |
|---|---|---|
| US-01, US-02 | Haute | Fonctions de consultation, base de tout le module |
| US-03 | Haute | Sans création, aucune police ne peut exister |
| US-04 | Moyenne | Nécessaire mais peut suivre la V1 |
| US-05 | Moyenne | Action sensible, à sécuriser avant mise en prod |
| US-06 | Haute | Transverse à tout le module, condition de sécurité |
