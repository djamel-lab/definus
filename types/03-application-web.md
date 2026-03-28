# 03 — Application Web

## Définition

Application interactive accessible via navigateur avec espace connecté. Les utilisateurs créent un compte, interagissent avec des données, exécutent des actions. C'est le cœur de la plupart des produits digitaux.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐⭐ |
| Utilisateurs | Authentifiés (clients, utilisateurs finaux) |
| Interactions | CRUD complet, workflows, temps réel |
| Données | Dynamiques, sensibles, relationnelles |
| Hébergement | Serveur (Vercel, AWS, Cloudflare Workers) |
| Cycle de vie | Produit long terme, itérations continues |
| Stack typique | React/Next.js + API + PostgreSQL/Supabase |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Inscription / Connexion | Obligatoire | [→](../features/auth/inscription-connexion.md) |
| Mot de passe oublié | Obligatoire | [→](../features/auth/mot-de-passe-oublie.md) |
| Profil utilisateur | Obligatoire | [→](../features/auth/profil-utilisateur.md) |
| Rôles et permissions | Recommandé | [→](../features/auth/roles-permissions.md) |
| Dashboard utilisateur | Recommandé | [→](../features/analytics/dashboard-utilisateur.md) |
| Recherche et filtres | Recommandé | [→](../features/data/recherche-filtres.md) |
| Formulaires complexes | Obligatoire | [→](../features/data/formulaires.md) |
| Upload de fichiers | Recommandé | [→](../features/content/upload-fichiers.md) |
| Notifications | Recommandé | [→](../features/communication/notifications.md) |
| Emails transactionnels | Obligatoire | [→](../features/communication/emails-transactionnels.md) |
| Export de données (PDF, CSV) | Recommandé | [→](../features/data/export-donnees.md) |
| Pagination / Infinite scroll | Recommandé | [→](../features/data/pagination.md) |
| Navigation et layout | Obligatoire | [→](../features/ux/navigation.md) |
| Responsive design | Obligatoire | [→](../features/ux/responsive.md) |
| Gestion d'erreurs | Obligatoire | [→](../features/ux/gestion-erreurs.md) |
| Loading states | Obligatoire | [→](../features/ux/loading-states.md) |
| RGPD / Consentement | Obligatoire | [→](../features/security/rgpd.md) |
| Logs et audit trail | Recommandé | [→](../features/security/audit-trail.md) |

## Questionnaire de cadrage rapide

1. Qui sont les utilisateurs ? Combien de rôles différents ?
2. Quels sont les 3-5 parcours utilisateur principaux ?
3. Quelles données sont manipulées ? Lesquelles sont sensibles ?
4. Y a-t-il des workflows avec validation (ex: soumission → review → approbation) ?
5. Faut-il du temps réel (notifications, mises à jour live) ?
6. Quelles intégrations externes (paiement, email, CRM, API tierces) ?
7. Quel volume d'utilisateurs est attendu au lancement ? À 12 mois ?
8. Y a-t-il des contraintes réglementaires (PSFP, PCI-DSS, RGPD) ?
9. Quel est le stack technique préféré ou imposé ?
10. Y a-t-il une maquette Figma ou un wireframe existant ?
11. Quel est le MVP (version minimale) vs la vision complète ?
12. Qui maintient l'application après le lancement ?

## Exemple Lina

L'espace investisseur Lina Capital serait une application web avec connexion, dashboard portfolio, suivi des projets, documents à télécharger, et notifications.
