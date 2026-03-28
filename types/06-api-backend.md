# 06 — API / Backend

## Définition

Service sans interface utilisateur qui expose des endpoints pour que d'autres applications (web, mobile, partenaires) puissent lire et écrire des données. C'est la colonne vertébrale technique d'un système.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐⭐ |
| Utilisateurs | Machines (apps, scripts, partenaires) |
| Interactions | Requêtes HTTP, WebSocket, webhooks |
| Données | CRUD, transformations, agrégations |
| Hébergement | Serveur (Node.js, Python), serverless (Cloudflare Workers, AWS Lambda) |
| Cycle de vie | Long terme, versioning, backward compatibility |
| Stack typique | Node.js/Express, Python/FastAPI, Cloudflare Workers |

## Sous-types

| Type | Description | Quand choisir |
|------|-------------|---------------|
| REST API | Endpoints ressource-based, HTTP verbs | Standard, la plupart des cas |
| GraphQL | Requêtes flexibles, un seul endpoint | Frontends multiples, données complexes |
| WebSocket | Connexion persistante bidirectionnelle | Temps réel (chat, notifications live) |
| Webhook | Callbacks HTTP sur événements | Intégrations event-driven |
| gRPC | Protocol Buffers, haute performance | Microservices internes |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Authentification API (JWT, OAuth) | Obligatoire | [→](../features/auth/auth-api.md) |
| Rate limiting | Obligatoire | [→](../features/security/rate-limiting.md) |
| Validation des entrées | Obligatoire | [→](../features/data/validation.md) |
| Gestion d'erreurs standardisée | Obligatoire | [→](../features/ux/gestion-erreurs.md) |
| Documentation API (OpenAPI/Swagger) | Obligatoire | [→](../features/integration/documentation-api.md) |
| Versioning | Recommandé | [→](../features/integration/versioning-api.md) |
| Pagination | Obligatoire | [→](../features/data/pagination.md) |
| Logging et monitoring | Obligatoire | [→](../features/security/audit-trail.md) |
| CORS | Obligatoire | [→](../features/security/cors.md) |
| Webhooks sortants | Optionnel | [→](../features/integration/webhooks.md) |
| File upload/download | Optionnel | [→](../features/content/upload-fichiers.md) |
| Cache (Redis, CDN) | Recommandé | [→](../features/data/cache.md) |
| Tests automatisés | Obligatoire | [→](../features/integration/tests-api.md) |
| CI/CD | Obligatoire | [→](../features/integration/cicd.md) |

## Questionnaire de cadrage rapide

1. Quel type d'API ? (REST, GraphQL, WebSocket, webhook)
2. Qui consomme cette API ? (frontend interne, app mobile, partenaires externes)
3. Quelles sont les ressources/entités principales ? (users, projects, transactions...)
4. Quels sont les endpoints critiques ? Lister les 5-10 principaux.
5. Quel mécanisme d'authentification ? (JWT, API key, OAuth2)
6. Faut-il du rate limiting ? Quelles limites ?
7. Y a-t-il des données sensibles nécessitant du chiffrement ?
8. Quel volume de requêtes attendu ? (requêtes/seconde)
9. Faut-il une documentation Swagger/OpenAPI ?
10. Quelles bases de données ? (PostgreSQL, MongoDB, Redis)
11. Faut-il du versioning d'API ? (v1, v2)
12. Quel environnement de déploiement ? (Cloudflare Workers, AWS, VPS)
13. Y a-t-il des contraintes de latence ? (SLA)
14. Faut-il des webhooks pour notifier d'autres systèmes ?

## Exemple Lina

Hub API Lina : authentification centralisée, gestion des investisseurs, projets, transactions, calcul des rendements. Consommé par l'app web, l'app mobile et les partenaires.
