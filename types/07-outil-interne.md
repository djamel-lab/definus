# 07 — Outil Interne

## Définition

Application web destinée exclusivement à l'équipe interne. Back-office, CRM maison, outil de gestion, outil compliance. Pas besoin d'être beau, doit être efficace.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐ |
| Utilisateurs | Internes (équipe, 2-50 personnes) |
| Interactions | CRUD, workflows d'approbation, recherche |
| Données | Opérationnelles, parfois sensibles |
| Hébergement | Interne ou outil no-code (Retool, Appsmith, Notion) |
| Cycle de vie | Moyen terme, évolue avec les process |
| Stack typique | Retool, Appsmith, React + Supabase, Google Apps Script |

## Sous-types

| Type | Description | Exemple |
|------|-------------|---------|
| Back-office / Admin | Gestion des données métier | Admin Lina (projets, investisseurs) |
| CRM interne | Suivi des relations clients/prospects | Pipeline commercial |
| Outil compliance | Workflows réglementaires | Vérification KYC, contrôle PSFP |
| Outil RH | Gestion équipe interne | Congés, évaluations |
| Outil support | Gestion tickets/demandes | Support investisseurs |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Authentification (SSO si possible) | Obligatoire | [→](../features/auth/inscription-connexion.md) |
| Rôles et permissions | Obligatoire | [→](../features/auth/roles-permissions.md) |
| CRUD sur les entités métier | Obligatoire | [→](../features/data/crud.md) |
| Recherche et filtres avancés | Obligatoire | [→](../features/data/recherche-filtres.md) |
| Tableaux de données avec tri/filtre | Obligatoire | [→](../features/data/tableaux.md) |
| Workflow d'approbation | Recommandé | [→](../features/data/workflow-approbation.md) |
| Import/export données | Recommandé | [→](../features/data/export-donnees.md) |
| Audit trail | Obligatoire | [→](../features/security/audit-trail.md) |
| Notifications internes | Recommandé | [→](../features/communication/notifications.md) |
| Dashboard KPIs | Optionnel | [→](../features/analytics/kpis.md) |

## Questionnaire de cadrage rapide

1. Qui utilise cet outil ? Combien de personnes ? Quels rôles ?
2. Quel process métier cet outil digitalise-t-il ?
3. Quelles sont les entités principales ? (clients, dossiers, projets, tickets...)
4. Y a-t-il des workflows de validation ? (soumission → review → approbation)
5. Faut-il un audit trail (qui a fait quoi, quand) ?
6. L'outil doit-il s'intégrer à des systèmes existants ? (CRM, email, Notion, Slack)
7. Faut-il importer des données existantes ? (Excel, CSV, autre outil)
8. Approche : code custom ou outil no-code (Retool, Appsmith) ?
9. Y a-t-il des contraintes de sécurité particulières ? (données sensibles, RGPD)
10. Qui maintient l'outil ? (développeur interne, prestataire)

## Exemple Lina

Outil compliance interne pour le suivi des dossiers PSFP : soumission du dossier → vérification KYC → validation Sharia Board → approbation comité d'investissement. Avec audit trail complet.
