# Panel admin

## Définition
Interface d'administration pour gérer l'application : utilisateurs, contenus, paramètres globaux.

## Sous-features
- [ ] Dashboard admin (KPIs globaux)
- [ ] Gestion des utilisateurs (lister, bloquer, supprimer)
- [ ] Gestion du contenu (CRUD sur les entités métier)
- [ ] Configuration globale (paramètres de l'app)
- [ ] Logs et audit trail
- [ ] Notifications admin
- [ ] Impersonation (se connecter en tant qu'un utilisateur)

## Questionnaire de cadrage
1. Quelles actions l'admin doit-il pouvoir faire ? Lister.
2. Faut-il un dashboard admin avec des KPIs spécifiques ?
3. L'admin doit-il pouvoir impersonner un utilisateur ? (voir l'app comme lui)
4. Faut-il des niveaux d'admin ? (super-admin, admin, moderator)
5. L'admin panel est-il une partie de l'app ou une app séparée ?
6. Quel outil ? (custom React, Django Admin, Retool, Appsmith)
