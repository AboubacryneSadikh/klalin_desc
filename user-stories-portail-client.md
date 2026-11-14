# User Stories — Portail Client

Projet : klalin
Module : Portail Client

---

## Épopée : Authentification et accueil

### US-01 — Connexion au portail
**En tant qu'** assuré
**Je veux** me connecter avec mon email et mon mot de passe
**Afin de** accéder à mon espace personnel en toute sécurité

**Critères d'acceptation**
- Un message d'erreur générique s'affiche en cas d'identifiants incorrects (sans préciser lequel est faux)
- Une option "mot de passe oublié" est disponible
- Après plusieurs échecs, un mécanisme de protection (délai, captcha) se déclenche

---

### US-02 — Vue d'ensemble personnelle
**En tant qu'** assuré
**Je veux** voir en un coup d'œil mes polices, sinistres et paiements
**Afin de** avoir une vision claire de ma situation sans naviguer dans plusieurs menus

**Critères d'acceptation**
- Le tableau de bord affiche le nombre de polices actives, sinistres en cours, prochain paiement
- Des raccourcis mènent directement aux actions fréquentes (déclarer un sinistre, voir mes documents)

---

## Épopée : Gestion de mes polices

### US-03 — Consulter le détail de ma police
**En tant qu'** assuré
**Je veux** consulter les informations complètes de ma police
**Afin de** connaître précisément ma couverture et mes échéances

**Critères d'acceptation**
- Les informations contractuelles, paiements effectués et à venir sont visibles
- Je ne peux consulter que mes propres polices

---

## Épopée : Sinistres

### US-04 — Déclarer un sinistre depuis mon espace
**En tant qu'** assuré
**Je veux** déclarer un sinistre directement depuis mon portail
**Afin de** ne pas dépendre des horaires d'ouverture d'une agence

**Critères d'acceptation**
- Le formulaire est accessible 24h/24
- Je reçois une confirmation immédiate avec un numéro de suivi

---

### US-05 — Consulter l'historique de mes sinistres
**En tant qu'** assuré
**Je veux** voir la liste de mes sinistres passés et leur statut de traitement
**Afin de** garder une trace de mes démarches

**Critères d'acceptation**
- Chaque ligne affiche : date, type, statut, montant réglé le cas échéant
- Je peux ouvrir le détail de chaque sinistre pour voir les actions entreprises

---

## Épopée : Documents et paiements

### US-06 — Accéder à mes documents
**En tant qu'** assuré
**Je veux** consulter et télécharger mes contrats, attestations et courriers
**Afin de** disposer de mes justificatifs sans solliciter un conseiller

**Critères d'acceptation**
- Les documents sont classés par type et par date
- Chaque document est téléchargeable au format PDF

---

### US-07 — Suivre mes paiements
**En tant qu'** assuré
**Je veux** voir mes paiements effectués et à venir
**Afin de** anticiper mes échéances et éviter tout retard

**Critères d'acceptation**
- La date et le montant du prochain paiement sont clairement affichés
- L'historique des paiements passés indique leur statut (payé, en retard)

---

## Épopée : Profil

### US-08 — Modifier mes informations personnelles
**En tant qu'** assuré
**Je veux** mettre à jour mon adresse, mon email et mon téléphone
**Afin de** garder mes coordonnées à jour auprès de l'assurance

**Critères d'acceptation**
- Toute modification déclenche une confirmation par email
- Un changement d'adresse peut déclencher un recalcul de prime, avec information claire au client

---

## Notes de priorisation suggérées

| Story | Priorité | Justification |
|---|---|---|
| US-01, US-02 | Haute | Fondation de tout le portail |
| US-03, US-04, US-05 | Haute | Cœur de la valeur pour le client |
| US-06, US-07 | Moyenne | Confort, réduit la charge du support |
| US-08 | Moyenne | Important mais peut suivre la V1 |
