# Secrets management

## Définition
Gestion sécurisée des clés API, tokens, mots de passe et autres secrets utilisés par l'application et les automatisations.

## Sous-features
- [ ] Variables d'environnement (.env)
- [ ] Vault (HashiCorp Vault, AWS Secrets Manager)
- [ ] Rotation automatique des secrets
- [ ] Séparation dev/staging/prod
- [ ] Pas de secrets dans le code source (git)
- [ ] Audit d'accès aux secrets

## Questionnaire de cadrage
1. Quels secrets sont nécessaires ? (clés API, tokens, credentials BDD, clés de chiffrement)
2. Où sont stockés les secrets ? (.env, vault, variables CI/CD, dashboard hébergeur)
3. Faut-il de la rotation automatique ?
4. Les secrets sont-ils différents par environnement ? (dev, staging, prod)
5. Qui a accès aux secrets de production ? (restreindre au minimum)
6. Y a-t-il un audit de qui accède aux secrets ?
