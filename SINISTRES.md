# 🏢 Workflow de Gestion des Sinistres - SUNU Assurance

## 📖 Description
Ce document décrit le workflow complet de gestion des sinistres pour SUNU Assurance Côte d'Ivoire, organisé par espace utilisateur et phase de traitement.

## 🎯 Objectifs
- Digitaliser le processus sinistre de bout en bout
- Améliorer l'expérience client
- Optimiser les délais de traitement
- Réduire les coûts de gestion

## 👥 Espaces Utilisateurs

| Espace | Rôle | Accès | Utilisateurs |
|--------|------|-------|-------------|
| **👤 Espace Client** | Déclaration et suivi | Public/Authentifié | Assurés |
| **👨‍💼 Espace Agent** | Interface commerciale | Authentifié | Agents, Courtiers |
| **🏢 Espace Backoffice** | Traitement métier | Authentifié + RBAC | Gestionnaires, Experts |
| **🔧 Espace Expert** | Expertise technique | Authentifié | Experts externes |
| **🤖 Système Auto** | Automatisation | Technique | APIs, Services |

## 🔄 Processus Global

```mermaid
flowchart LR
    A[🚨 Déclaration] --> B[🔍 Évaluation]
    B --> C[💶 Décision]
    C --> D[📦 Clôture]
