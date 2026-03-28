# Index des fonctionnalités-type

Chaque fonctionnalité a son propre fichier avec une **définition**, une **liste de sous-features**, et un **questionnaire de cadrage** complet.

---

## auth/ — Authentification et gestion utilisateurs

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Inscription / Connexion | [inscription-connexion.md](auth/inscription-connexion.md) | App web, Mobile, SaaS, Outil interne |
| Mot de passe oublié | [mot-de-passe-oublie.md](auth/mot-de-passe-oublie.md) | App web, Mobile, SaaS |
| Profil utilisateur | [profil-utilisateur.md](auth/profil-utilisateur.md) | App web, Mobile, SaaS |
| Rôles et permissions | [roles-permissions.md](auth/roles-permissions.md) | App web, Dashboard, SaaS, Outil interne |
| Multi-tenant (organisations) | [multi-tenant.md](auth/multi-tenant.md) | SaaS |
| Authentification API | [auth-api.md](auth/auth-api.md) | API, Extension |
| Authentification biométrique | [biometrie.md](auth/biometrie.md) | Mobile |
| SSO / SAML | [sso.md](auth/sso.md) | SaaS, Outil interne |

## data/ — Données, recherche, formulaires

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Formulaires | [formulaires.md](data/formulaires.md) | Landing, Vitrine, App web, SaaS |
| Recherche et filtres | [recherche-filtres.md](data/recherche-filtres.md) | App web, Dashboard, SaaS, Outil interne |
| CRUD (Create, Read, Update, Delete) | [crud.md](data/crud.md) | App web, SaaS, Outil interne |
| Tableaux de données | [tableaux.md](data/tableaux.md) | Dashboard, Outil interne, SaaS |
| Export de données | [export-donnees.md](data/export-donnees.md) | Dashboard, App web, SaaS, Outil interne |
| Pagination | [pagination.md](data/pagination.md) | App web, API, SaaS |
| Validation des données | [validation.md](data/validation.md) | App web, API, SaaS |
| Workflow d'approbation | [workflow-approbation.md](data/workflow-approbation.md) | App web, SaaS, Outil interne |
| Mode offline | [mode-offline.md](data/mode-offline.md) | Mobile |
| Temps réel | [temps-reel.md](data/temps-reel.md) | Dashboard, App web, SaaS |
| Géolocalisation | [geolocalisation.md](data/geolocalisation.md) | Mobile |
| Cache | [cache.md](data/cache.md) | API, App web |

## content/ — Contenu, médias, documents

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Upload de fichiers | [upload-fichiers.md](content/upload-fichiers.md) | App web, Mobile, SaaS |
| Blog / actualités | [blog.md](content/blog.md) | Vitrine |
| FAQ | [faq.md](content/faq.md) | Landing, Vitrine, App web |
| Social proof | [social-proof.md](content/social-proof.md) | Landing, Vitrine |
| Génération de documents | [generation-documents.md](content/generation-documents.md) | App web, SaaS, Outil interne |
| Lecteur de médias | [lecteur-medias.md](content/lecteur-medias.md) | App web, Mobile, SaaS |

## communication/ — Notifications, emails, messagerie

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Notifications in-app | [notifications.md](communication/notifications.md) | App web, SaaS, Outil interne |
| Notifications push | [notifications-push.md](communication/notifications-push.md) | Mobile |
| Emails transactionnels | [emails-transactionnels.md](communication/emails-transactionnels.md) | App web, SaaS |
| Alertes et seuils | [alertes.md](communication/alertes.md) | Dashboard, Automatisation |
| Chat / messagerie | [chat.md](communication/chat.md) | App web, SaaS |
| Intégration réseaux sociaux | [social-media.md](communication/social-media.md) | Vitrine, Landing |

## payment/ — Paiement, facturation, abonnement

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Paiement en ligne | [paiement.md](payment/paiement.md) | App web, SaaS |
| Abonnement / plans | [abonnement.md](payment/abonnement.md) | SaaS |
| Facturation automatique | [facturation.md](payment/facturation.md) | SaaS |
| Limites par plan | [limites-plan.md](payment/limites-plan.md) | SaaS |

## admin/ — Administration, back-office

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Panel admin | [panel-admin.md](admin/panel-admin.md) | App web, SaaS |
| Modération de contenu | [moderation.md](admin/moderation.md) | App web, SaaS |
| Gestion des utilisateurs | [gestion-utilisateurs.md](admin/gestion-utilisateurs.md) | App web, SaaS, Outil interne |

## integration/ — APIs, webhooks, imports/exports

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Documentation API | [documentation-api.md](integration/documentation-api.md) | API |
| Versioning API | [versioning-api.md](integration/versioning-api.md) | API |
| Webhooks | [webhooks.md](integration/webhooks.md) | API, SaaS, Automatisation |
| CI/CD | [cicd.md](integration/cicd.md) | API, App web, SaaS |
| Tests automatisés | [tests-api.md](integration/tests-api.md) | API, App web, SaaS |
| Partage / embed | [partage-embed.md](integration/partage-embed.md) | Dashboard |
| Scalabilité | [scalabilite.md](integration/scalabilite.md) | SaaS, API |

## analytics/ — Statistiques, reporting, KPIs

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Tracking (GA4, GTM) | [tracking.md](analytics/tracking.md) | Landing, Vitrine, App web |
| KPIs et métriques | [kpis.md](analytics/kpis.md) | Dashboard, SaaS, Outil interne |
| Graphiques interactifs | [graphiques.md](analytics/graphiques.md) | Dashboard |
| Drill-down | [drill-down.md](analytics/drill-down.md) | Dashboard |
| Dashboard utilisateur | [dashboard-utilisateur.md](analytics/dashboard-utilisateur.md) | App web, SaaS |
| A/B testing | [ab-testing.md](analytics/ab-testing.md) | Landing |
| Monitoring | [monitoring.md](analytics/monitoring.md) | Automatisation, API |

## ux/ — UX transversale

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| Responsive design | [responsive.md](ux/responsive.md) | Tous |
| Navigation | [navigation.md](ux/navigation.md) | Vitrine, App web, SaaS |
| Navigation mobile | [navigation-mobile.md](ux/navigation-mobile.md) | Mobile |
| Onboarding | [onboarding.md](ux/onboarding.md) | App web, Mobile, SaaS |
| SEO | [seo.md](ux/seo.md) | Landing, Vitrine |
| Gestion d'erreurs | [gestion-erreurs.md](ux/gestion-erreurs.md) | Tous |
| Loading states | [loading-states.md](ux/loading-states.md) | App web, Mobile, SaaS |
| Internationalisation (i18n) | [i18n.md](ux/i18n.md) | Vitrine, App web, SaaS |
| Thème / mode sombre | [theme.md](ux/theme.md) | Dashboard, App web |
| Accessibilité | [accessibilite.md](ux/accessibilite.md) | Tous |
| Settings utilisateur | [settings.md](ux/settings.md) | App web, Mobile, SaaS, Extension |
| Deep linking | [deep-linking.md](ux/deep-linking.md) | Mobile |
| ASO (App Store Optimization) | [aso.md](ux/aso.md) | Mobile |
| Animations | [animations.md](ux/animations.md) | Landing, App web |
| CTA (Call to Action) | [cta.md](ux/cta.md) | Landing, Vitrine |

## security/ — Sécurité, conformité, RGPD

| Feature | Fichier | Pertinent pour |
|---------|---------|---------------|
| RGPD / Consentement | [rgpd.md](security/rgpd.md) | Tous |
| Mentions légales | [mentions-legales.md](security/mentions-legales.md) | Landing, Vitrine |
| Audit trail | [audit-trail.md](security/audit-trail.md) | App web, SaaS, Outil interne, API |
| Rate limiting | [rate-limiting.md](security/rate-limiting.md) | API, Automatisation |
| CORS | [cors.md](security/cors.md) | API |
| Secrets management | [secrets-management.md](security/secrets-management.md) | Automatisation, API |
| Backup et disaster recovery | [backup.md](security/backup.md) | SaaS |
| Crash reporting | [crash-reporting.md](security/crash-reporting.md) | Mobile |
| Permissions extension | [permissions-extension.md](security/permissions-extension.md) | Extension |
