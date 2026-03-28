# Gestion des utilisateurs (admin)

## Définition
Interface admin pour gérer les comptes utilisateurs : lister, rechercher, modifier, bloquer, supprimer.

## Sous-features
- [ ] Liste des utilisateurs avec recherche/filtres
- [ ] Fiche utilisateur détaillée
- [ ] Modifier les informations d'un utilisateur
- [ ] Changer le rôle d'un utilisateur
- [ ] Bloquer / débloquer un compte
- [ ] Supprimer un compte (avec gestion RGPD)
- [ ] Réinitialiser le mot de passe
- [ ] Voir l'activité d'un utilisateur (audit trail)
- [ ] Export de la liste des utilisateurs
- [ ] Invitation de nouveaux utilisateurs

## Questionnaire de cadrage
1. Quelles informations l'admin voit-il sur chaque utilisateur ?
2. L'admin peut-il modifier les informations d'un utilisateur ?
3. Faut-il pouvoir bloquer un compte ? (soft block vs hard delete)
4. Faut-il pouvoir réinitialiser le mot de passe d'un utilisateur ?
5. Faut-il voir l'historique d'activité de chaque utilisateur ?
6. L'admin peut-il inviter de nouveaux utilisateurs ?
7. Faut-il exporter la liste des utilisateurs ?
8. Y a-t-il des contraintes RGPD sur la suppression ? (supprimer toutes les données associées)
