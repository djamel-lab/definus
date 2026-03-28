# CI/CD

## Définition
Intégration continue et déploiement continu : automatiser le build, les tests et le déploiement.

## Sous-features
- [ ] Build automatique à chaque push
- [ ] Tests automatiques (unit, integration, e2e)
- [ ] Linting / formatting check
- [ ] Type checking
- [ ] Preview deployments (par branche / PR)
- [ ] Déploiement automatique en production
- [ ] Rollback
- [ ] Notifications de build (Slack, email)
- [ ] Environment variables par environnement

## Questionnaire de cadrage
1. Quel outil CI/CD ? (GitHub Actions, GitLab CI, Vercel auto-deploy)
2. Quels tests automatiques ? (unit, integration, e2e, lint, typecheck)
3. Faut-il des preview deployments par PR ?
4. Le déploiement en production est-il automatique ou manuel ?
5. Faut-il un mécanisme de rollback ?
6. Combien d'environnements ? (dev, staging, prod)
7. Faut-il des notifications de build ? (Slack, email)
