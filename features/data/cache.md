# Cache

## Définition
Stockage temporaire de données fréquemment consultées pour réduire la latence et la charge serveur.

## Sous-features

- [ ] Cache HTTP (headers Cache-Control, ETag)
- [ ] Cache applicatif (Redis, Memcached)
- [ ] CDN pour assets statiques
- [ ] Cache côté client (Service Worker, React Query)
- [ ] Invalidation de cache (TTL, event-based)
- [ ] Cache de requêtes API

## Questionnaire de cadrage

1. Quelles données sont fréquemment consultées et rarement modifiées ? (candidats au cache)
2. Quel TTL (durée de vie) pour chaque type de donnée ?
3. Comment invalider le cache quand les données changent ?
4. Faut-il un cache côté serveur (Redis) ou côté client (React Query, SWR) ?
5. Les assets statiques sont-ils servis via CDN ?
6. Quelle stratégie de cache ? (cache-first, network-first, stale-while-revalidate)
