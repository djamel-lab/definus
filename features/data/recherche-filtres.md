# Recherche et filtres

## Définition
Permettre aux utilisateurs de trouver rapidement des données dans l'application via recherche textuelle et/ou filtres structurés.

## Sous-features

- [ ] Recherche textuelle (full-text search)
- [ ] Recherche instantanée (au fil de la frappe)
- [ ] Filtres par catégorie / statut / date
- [ ] Filtres combinés (AND/OR)
- [ ] Tri par colonne
- [ ] Sauvegarde de filtres favoris
- [ ] Recherche avancée (opérateurs, champs spécifiques)
- [ ] Suggestions / autocomplete
- [ ] Recherche globale (cross-entités)
- [ ] Historique de recherche
- [ ] Résultats paginés

## Questionnaire de cadrage

1. Sur quelles entités la recherche porte-t-elle ? (utilisateurs, projets, transactions, documents...)
2. La recherche est-elle textuelle (full-text) ou uniquement par filtres structurés ?
3. Faut-il de la recherche instantanée (résultats au fil de la frappe) ?
4. Quels filtres sont nécessaires ? Lister par entité : champ + type (dropdown, date range, slider, toggle)
5. Les filtres doivent-ils être combinables ? (ex: statut=actif ET date > 01/01/2026)
6. L'utilisateur doit-il pouvoir sauvegarder des filtres/vues favorites ?
7. Faut-il du tri ? Sur quelles colonnes ?
8. Quel est le volume de données à chercher ? (centaines, milliers, millions)
9. Faut-il de l'autocomplete/suggestions pendant la saisie ?
10. Faut-il une recherche globale (chercher à travers toutes les entités) ?
11. Quel moteur de recherche ? (SQL LIKE, PostgreSQL full-text, Elasticsearch, Algolia, Meilisearch)
