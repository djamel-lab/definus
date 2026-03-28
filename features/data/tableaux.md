# Tableaux de données

## Définition
Composant d'affichage de données tabulaires avec tri, filtres, pagination. Le composant le plus utilisé dans les dashboards et outils internes.

## Sous-features

- [ ] Affichage colonnes configurables
- [ ] Tri par colonne (asc/desc)
- [ ] Filtres par colonne
- [ ] Pagination (ou infinite scroll)
- [ ] Sélection de lignes (checkbox)
- [ ] Actions en masse sur la sélection
- [ ] Actions par ligne (edit, delete, view)
- [ ] Colonnes redimensionnables
- [ ] Colonnes masquables
- [ ] Export (CSV, Excel, PDF)
- [ ] Résumé / totaux en bas de tableau
- [ ] Lignes expansibles (détail inline)
- [ ] Cellules éditables inline
- [ ] Freeze première colonne / header

## Questionnaire de cadrage

1. Quels tableaux sont nécessaires dans l'application ? Lister chacun avec ses colonnes.
2. Quel volume de données par tableau ? (dizaines, centaines, milliers, millions)
3. Faut-il du tri ? Sur quelles colonnes ?
4. Faut-il des filtres intégrés au tableau ? Lesquels ?
5. Comment paginer ? (pagination classique, infinite scroll, load more)
6. Faut-il pouvoir sélectionner des lignes et faire des actions en masse ? (supprimer, exporter, changer statut)
7. Quelles actions par ligne ? (voir détail, modifier, supprimer, dupliquer)
8. L'utilisateur peut-il personnaliser les colonnes affichées ?
9. Faut-il des cellules éditables directement dans le tableau ?
10. Faut-il exporter le contenu du tableau ? (CSV, Excel, PDF)
11. Faut-il des totaux / résumés en bas de colonnes ?
12. Y a-t-il des lignes expansibles pour voir un détail sans quitter le tableau ?
