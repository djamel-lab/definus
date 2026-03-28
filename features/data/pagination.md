# Pagination

## Définition
Découpage de listes longues en pages pour optimiser la performance et l'expérience utilisateur.

## Sous-features

- [ ] Pagination classique (page 1, 2, 3...)
- [ ] Nombre de résultats par page configurable
- [ ] Infinite scroll
- [ ] Load more button
- [ ] Cursor-based pagination (API)
- [ ] Affichage du nombre total de résultats
- [ ] Navigation directe à une page

## Questionnaire de cadrage

1. Quel pattern de pagination ? (pages numérotées, infinite scroll, load more)
2. Combien d'éléments par page par défaut ? L'utilisateur peut-il changer ?
3. Faut-il afficher le nombre total de résultats ?
4. Côté API : offset-based ou cursor-based ?
5. Y a-t-il des listes avec un très grand volume ? (> 10 000 éléments)
6. La pagination doit-elle se combiner avec les filtres et le tri ?
