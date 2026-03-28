# Rate limiting

## Définition
Limiter le nombre de requêtes qu'un client peut faire sur une période donnée pour protéger l'API contre les abus.

## Sous-features
- [ ] Limite par IP
- [ ] Limite par token/API key
- [ ] Limite par endpoint
- [ ] Headers de rate limit (X-RateLimit-Remaining)
- [ ] Réponse 429 Too Many Requests
- [ ] Retry-After header
- [ ] Rate limit différent par plan (SaaS)

## Questionnaire de cadrage
1. Quelles limites par défaut ? (ex: 100 req/min, 1000 req/heure)
2. Les limites sont-elles par IP, par token, par utilisateur ?
3. Certains endpoints ont-ils des limites spécifiques ? (login, signup, paiement)
4. Le rate limit varie-t-il par plan tarifaire ?
5. Faut-il retourner les headers de rate limit dans les réponses ?
6. Quel backend ? (Redis, mémoire, Cloudflare built-in)
