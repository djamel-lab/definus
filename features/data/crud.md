# CRUD (Create, Read, Update, Delete)

## Définition
Opérations de base sur les données : créer, lire, modifier et supprimer des enregistrements. Chaque entité métier de l'application a généralement un CRUD complet.

## Sous-features

- [ ] Création d'enregistrement (formulaire)
- [ ] Liste / vue des enregistrements
- [ ] Vue détail d'un enregistrement
- [ ] Modification d'un enregistrement
- [ ] Suppression (soft delete ou hard delete)
- [ ] Suppression en masse (bulk delete)
- [ ] Duplication d'un enregistrement
- [ ] Import en masse (CSV, Excel)
- [ ] Historique des modifications (versioning)
- [ ] Corbeille / restauration

## Questionnaire de cadrage

1. Quelles sont les entités métier principales ? Lister chacune (ex: Projet, Investisseur, Transaction, Document).
2. Pour chaque entité, quels sont les champs/attributs ? Lister avec le type (texte, nombre, date, relation, fichier).
3. Qui peut créer, lire, modifier, supprimer chaque entité ? (matrice rôle × action)
4. La suppression est-elle définitive (hard delete) ou réversible (soft delete / corbeille) ?
5. Faut-il un historique des modifications ? (qui a changé quoi, quand)
6. Faut-il pouvoir dupliquer un enregistrement ?
7. Faut-il un import en masse ? (CSV, Excel) Si oui, quel format ?
8. Y a-t-il des relations entre entités ? (un Projet a N Transactions, un Investisseur a N Projets)
9. Y a-t-il des champs calculés automatiquement ? (totaux, pourcentages, statuts)
10. Les enregistrements ont-ils des statuts / étapes ? (brouillon → actif → archivé)
