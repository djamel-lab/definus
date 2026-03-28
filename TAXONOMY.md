# Taxonomie des types de logiciels

Cette taxonomie couvre tous les types de logiciels que Lina Finance est amenée à produire. Chaque type a sa fiche détaillée dans `/types/`.

---

## Vue d'ensemble

| # | Type | Complexité | Exemple Lina | Fiche |
|---|------|-----------|-------------|-------|
| 01 | Landing Page | ⭐ | lina-capital, pages campagne | [→](types/01-landing-page.md) |
| 02 | Site Vitrine | ⭐⭐ | linafinance.com | [→](types/02-site-vitrine.md) |
| 03 | Application Web | ⭐⭐⭐ | Espace investisseur, portail client | [→](types/03-application-web.md) |
| 04 | Dashboard / Reporting | ⭐⭐⭐ | Dashboard interne KPIs | [→](types/04-dashboard.md) |
| 05 | Application Mobile | ⭐⭐⭐⭐ | App investisseur iOS/Android | [→](types/05-application-mobile.md) |
| 06 | API / Backend | ⭐⭐⭐ | Hub API Lina | [→](types/06-api-backend.md) |
| 07 | Outil Interne | ⭐⭐ | CRM interne, outil compliance | [→](types/07-outil-interne.md) |
| 08 | Plateforme SaaS | ⭐⭐⭐⭐⭐ | Plateforme PSFP complète | [→](types/08-plateforme-saas.md) |
| 09 | Extension Navigateur | ⭐⭐ | Extension Chrome interne | [→](types/09-extension-navigateur.md) |
| 10 | Automatisation / Workflow | ⭐⭐ | Pipelines Zapier/n8n, scripts | [→](types/10-automatisation-workflow.md) |

---

## Arbre de décision rapide

```
Ton projet...
│
├─ Est une page unique de conversion ?
│  → 01 Landing Page
│
├─ Présente une activité sans interaction utilisateur ?
│  → 02 Site Vitrine
│
├─ A des utilisateurs qui se connectent et interagissent ?
│  ├─ Principalement consultation de données/graphiques ?
│  │  → 04 Dashboard
│  ├─ Interactions riches (CRUD, workflows, formulaires) ?
│  │  ├─ Usage interne uniquement ?
│  │  │  → 07 Outil Interne
│  │  ├─ Multi-tenant avec abonnement ?
│  │  │  → 08 Plateforme SaaS
│  │  └─ Usage client externe ?
│  │     → 03 Application Web
│  └─ Besoin d'accès mobile natif (push, offline, caméra) ?
│     → 05 Application Mobile
│
├─ Est un service sans interface (machine-to-machine) ?
│  → 06 API / Backend
│
├─ Est un plugin pour un logiciel existant ?
│  → 09 Extension Navigateur
│
└─ Automatise des tâches entre systèmes existants ?
   → 10 Automatisation / Workflow
```

---

## Combinaisons fréquentes

Certains projets combinent plusieurs types :

| Projet | Types combinés |
|--------|---------------|
| Plateforme PSFP Lina Capital | 08 SaaS + 06 API + 04 Dashboard + 05 Mobile |
| Site marketing + collecte leads | 02 Vitrine + 01 Landing Pages |
| Espace investisseur | 03 App Web + 06 API + 04 Dashboard |
| Outil compliance interne | 07 Interne + 04 Dashboard + 10 Automatisation |
| Funnel d'acquisition | 01 Landing Page + 10 Automatisation |

Quand un projet combine plusieurs types, il faut spécifier chaque composant séparément puis décrire les interfaces entre eux.

---

## Critères de catégorisation

Chaque type est caractérisé par :

- **Utilisateurs** : anonymes, authentifiés, internes, multi-tenant
- **Interactions** : lecture seule, CRUD, temps réel, transactionnel
- **Données** : statiques, dynamiques, sensibles, volumineuses
- **Hébergement** : statique (CDN), serveur, serverless, mobile stores
- **Cycle de vie** : one-shot, itératif, produit long terme
- **Conformité** : RGPD, PSFP, PCI-DSS, accessibilité RGAA
