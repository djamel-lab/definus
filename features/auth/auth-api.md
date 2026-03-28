# Authentification API

## Définition
Mécanisme pour authentifier les requêtes machine-to-machine vers une API. Pas d'interface utilisateur, uniquement des tokens/clés.

## Sous-features

- [ ] API Keys (clés statiques)
- [ ] JWT (JSON Web Tokens)
- [ ] OAuth2 (authorization code, client credentials)
- [ ] Bearer token
- [ ] HMAC signature
- [ ] Refresh tokens
- [ ] Scopes / permissions par token
- [ ] Rotation des clés
- [ ] Révocation de tokens
- [ ] IP whitelisting

## Questionnaire de cadrage

1. Qui consomme l'API ? (frontend interne, app mobile, partenaires externes, scripts)
2. Quel mécanisme d'authentification ? (API key, JWT, OAuth2)
3. Les tokens ont-ils une durée de vie ? Combien de temps ?
4. Faut-il des refresh tokens pour renouveler sans re-authentifier ?
5. Les tokens ont-ils des scopes (permissions limitées) ?
6. Faut-il permettre la révocation de tokens ?
7. Faut-il de l'IP whitelisting pour les partenaires ?
8. Comment les clés API sont-elles distribuées ? (dashboard, email, API)
9. Faut-il du rate limiting par clé/token ?
10. Y a-t-il des niveaux d'accès différents ? (read-only, read-write, admin)
