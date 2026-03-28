# Rôles et permissions

## Définition
Système qui contrôle ce que chaque utilisateur peut voir et faire dans l'application en fonction de son rôle. Essentiel pour les apps multi-utilisateurs.

## Sous-features

- [ ] Définition des rôles (admin, manager, user, viewer...)
- [ ] Matrice de permissions par rôle
- [ ] Permissions granulaires (CRUD par ressource)
- [ ] Héritage de rôles (un admin hérite des permissions manager)
- [ ] Rôles custom (créer ses propres rôles)
- [ ] Attribution de rôles par un admin
- [ ] Affichage conditionnel UI selon le rôle
- [ ] Protection API par rôle (middleware)
- [ ] Audit des changements de rôle

## Questionnaire de cadrage

1. Combien de rôles différents ? Lister chaque rôle et sa description.
2. Pour chaque rôle, quelles actions sont autorisées ? (voir, créer, modifier, supprimer, approuver)
3. Les permissions sont-elles par type de ressource ou globales ?
4. Les rôles sont-ils fixes ou un admin peut-il créer des rôles custom ?
5. Y a-t-il un super-admin avec accès total ?
6. Un utilisateur peut-il avoir plusieurs rôles ?
7. Les rôles sont-ils liés à une organisation (multi-tenant) ou globaux ?
8. Faut-il un audit trail des changements de permissions ?
9. Certaines actions nécessitent-elles une validation (ex: un admin doit approuver) ?
10. Comment les rôles sont-ils attribués ? (auto à l'inscription, invitation, promotion manuelle)

## Patterns courants

| Modèle | Description | Quand utiliser |
|--------|-------------|---------------|
| RBAC simple | Rôles fixes (admin, user, viewer) | Petites apps, outils internes |
| RBAC hiérarchique | Rôles avec héritage | Apps moyennes, SaaS |
| ABAC | Permissions basées sur attributs | Apps complexes, compliance |
| Permissions par objet | Droit par ressource individuelle | Collaboration docs, dossiers |
