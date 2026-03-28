# 08 — Plateforme SaaS

## Définition

Produit logiciel complet accessible en ligne, multi-tenant (plusieurs clients/organisations), avec système d'abonnement. Combine app web, API, dashboard, et souvent app mobile. C'est le type le plus complexe.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐⭐⭐⭐ |
| Utilisateurs | Multi-tenant, rôles multiples par organisation |
| Interactions | CRUD, workflows, temps réel, transactions financières |
| Données | Multi-tenant, volumineuses, sensibles |
| Hébergement | Cloud scalable (AWS, GCP, Vercel + Supabase) |
| Cycle de vie | Produit long terme, roadmap feature |
| Stack typique | Next.js + Supabase/PostgreSQL + Stripe + Vercel |

## Fonctionnalités standard

### Couche utilisateur
| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Inscription / Connexion | Obligatoire | [→](../features/auth/inscription-connexion.md) |
| Multi-tenant (organisations) | Obligatoire | [→](../features/auth/multi-tenant.md) |
| Rôles et permissions granulaires | Obligatoire | [→](../features/auth/roles-permissions.md) |
| Onboarding guidé | Obligatoire | [→](../features/ux/onboarding.md) |
| Profil et préférences | Obligatoire | [→](../features/auth/profil-utilisateur.md) |

### Couche métier
| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| CRUD entités principales | Obligatoire | [→](../features/data/crud.md) |
| Workflows complexes | Obligatoire | [→](../features/data/workflow-approbation.md) |
| Recherche et filtres avancés | Obligatoire | [→](../features/data/recherche-filtres.md) |
| Dashboard et reporting | Obligatoire | [→](../features/analytics/kpis.md) |
| Notifications multi-canal | Obligatoire | [→](../features/communication/notifications.md) |

### Couche paiement
| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Abonnement / pricing plans | Obligatoire | [→](../features/payment/abonnement.md) |
| Paiement en ligne | Obligatoire | [→](../features/payment/paiement.md) |
| Facturation automatique | Obligatoire | [→](../features/payment/facturation.md) |
| Gestion des limites par plan | Recommandé | [→](../features/payment/limites-plan.md) |

### Couche infrastructure
| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| API publique | Recommandé | [→](../features/integration/documentation-api.md) |
| Webhooks | Recommandé | [→](../features/integration/webhooks.md) |
| SSO / SAML | Optionnel | [→](../features/auth/sso.md) |
| Audit trail | Obligatoire | [→](../features/security/audit-trail.md) |
| Backup et disaster recovery | Obligatoire | [→](../features/security/backup.md) |
| Scalabilité | Obligatoire | [→](../features/integration/scalabilite.md) |

## Questionnaire de cadrage rapide

1. Quel problème le SaaS résout-il ? Pour qui ?
2. Quel est le modèle économique ? (freemium, abonnement, usage-based, commission)
3. Combien de plans tarifaires ? Quelles fonctionnalités par plan ?
4. L'architecture est-elle multi-tenant ? (une base par client ou base partagée)
5. Quels sont les 5 écrans les plus importants du produit ?
6. Y a-t-il des transactions financières ? (paiements, virements, commissions)
7. Faut-il une API publique pour les intégrations tierces ?
8. Quel volume d'utilisateurs simultanés faut-il supporter ?
9. Quels sont les SLA attendus ? (uptime 99.9%, temps de réponse)
10. Y a-t-il des contraintes réglementaires ? (PSFP, PCI-DSS, RGPD, SOC2)
11. Quelle est la roadmap MVP → V1 → V2 ?
12. Qui compose l'équipe technique ?

## Exemple Lina

La plateforme PSFP Lina Capital dans sa version complète : espace investisseur + espace porteur de projet + back-office interne + API partenaires + dashboard reporting AMF.
