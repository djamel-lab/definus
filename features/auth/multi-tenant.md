# Multi-tenant (Organisations)

## Définition
Architecture où plusieurs organisations/clients partagent la même application mais ont des données isolées. Chaque organisation a ses propres utilisateurs, données et configuration.

## Sous-features

- [ ] Création d'organisation
- [ ] Invitation de membres à une organisation
- [ ] Rôles par organisation (owner, admin, member)
- [ ] Switch entre organisations
- [ ] Isolation des données par organisation
- [ ] Paramètres spécifiques par organisation (logo, couleurs, nom)
- [ ] Facturation par organisation
- [ ] Sous-domaine ou URL personnalisé par organisation

## Questionnaire de cadrage

1. Comment appelle-t-on une organisation chez vous ? (workspace, team, company, cabinet)
2. Un utilisateur peut-il appartenir à plusieurs organisations ?
3. Comment une organisation est-elle créée ? (auto-inscription, invitation, validation manuelle)
4. Quels rôles existent au sein d'une organisation ? (owner, admin, member, viewer)
5. Faut-il une isolation stricte des données ? (un membre ne voit jamais les données d'une autre org)
6. Chaque organisation peut-elle personnaliser l'interface ? (logo, couleurs, nom de domaine)
7. La facturation est-elle par organisation ou par utilisateur ?
8. Faut-il un super-admin plateforme qui voit toutes les organisations ?
9. Architecture technique : base de données partagée (row-level security) ou séparée par org ?
10. Y a-t-il des limites par organisation ? (nombre d'utilisateurs, stockage, features)
