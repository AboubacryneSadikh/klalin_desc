# User Stories — Module de Tarification Dynamique

Projet : klalin
Module : Tarification Dynamique

---

## Épopée : Simulation

### US-01 — Simuler une prime d'assurance
**En tant qu'** agent commercial (ou client sur le portail public)
**Je veux** simuler une prime en fonction de critères de risque
**Afin de** fournir un devis rapide à un prospect

**Critères d'acceptation**
- Le formulaire demande les critères pertinents : âge, type de couverture, historique éventuel
- Le résultat s'affiche instantanément après saisie
- Le détail du calcul (facteurs ayant influencé le prix) est consultable

---

## Épopée : Configuration des règles

### US-02 — Consulter les critères de tarification
**En tant qu'** actuaire / responsable tarification
**Je veux** voir les critères de risque utilisés et leur pondération
**Afin de** comprendre comment les primes sont actuellement calculées

**Critères d'acceptation**
- Chaque critère (âge, zone géographique, type de bien, historique) est listé avec son poids dans le calcul

---

### US-03 — Ajuster les critères de tarification
**En tant qu'** actuaire / responsable tarification
**Je veux** modifier les règles et pondérations de tarification
**Afin de** adapter les primes à l'évolution du risque (ex. hausse des sinistres inondation)

**Critères d'acceptation**
- Toute modification nécessite une validation avant mise en production
- Les modifications sont historisées (qui, quand, quel critère)
- Les polices déjà existantes ne sont pas recalculées rétroactivement sans action explicite

---

## Épopée : Modèles de tarification

### US-04 — Gérer les modèles de tarification
**En tant qu'** administrateur/actuaire
**Je veux** consulter et définir des modèles de tarification avec règles et exceptions
**Afin de** structurer différentes grilles tarifaires selon les produits d'assurance

**Critères d'acceptation**
- Je peux créer un nouveau modèle basé sur un modèle existant (duplication)
- Je peux définir des règles d'exception (ex. tarif préférentiel pour un profil donné)
- Un modèle ne peut pas être supprimé s'il est activement utilisé par des polices en cours

---

## Épopée : Cohérence commerciale

### US-05 — Garantir la cohérence des devis entre agents
**En tant qu'** administrateur
**Je veux** que tous les agents utilisent le même modèle de tarification pour un profil donné
**Afin de** éviter les incohérences de prix entre deux clients aux profils similaires

**Critères d'acceptation**
- Le simulateur applique automatiquement le modèle en vigueur, sans possibilité de saisie manuelle du prix final par l'agent
- Toute dérogation tarifaire nécessite une validation explicite d'un superviseur

---

## Notes de priorisation suggérées

| Story | Priorité | Justification |
|---|---|---|
| US-01 | Haute | Usage quotidien par les agents, impact commercial direct |
| US-02 | Haute | Prérequis de transparence avant tout ajustement |
| US-03, US-04 | Moyenne | Structurant mais peut s'appuyer sur des valeurs par défaut en V1 |
| US-05 | Moyenne | Renforce la gouvernance une fois le module stabilisé |
