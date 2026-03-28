# Export de données

## Définition
Permettre aux utilisateurs de télécharger leurs données dans différents formats pour analyse externe, reporting ou archivage.

## Sous-features

- [ ] Export CSV
- [ ] Export Excel (.xlsx)
- [ ] Export PDF
- [ ] Export JSON
- [ ] Export de graphiques en image (PNG, SVG)
- [ ] Export personnalisé (choisir colonnes, filtres, période)
- [ ] Export planifié (automatique, récurrent)
- [ ] Export en masse (toutes les données)
- [ ] Historique des exports
- [ ] Génération asynchrone (pour gros volumes)

## Questionnaire de cadrage

1. Quelles données doivent être exportables ? (tableaux, graphiques, rapports complets)
2. Quels formats de sortie ? (CSV, Excel, PDF, JSON)
3. L'utilisateur peut-il personnaliser l'export ? (choisir colonnes, filtres, période)
4. Y a-t-il des gros volumes nécessitant un export asynchrone ? (générer en background, notifier quand prêt)
5. Faut-il des exports planifiés/automatiques ? (ex: rapport hebdo par email)
6. Faut-il un historique des exports téléchargés ?
7. Les exports contiennent-ils des données sensibles nécessitant un contrôle d'accès ?
8. Faut-il une mise en forme dans le PDF/Excel ? (en-tête, logo, pagination)
9. Y a-t-il des contraintes de taille ? (limite de lignes, poids du fichier)
10. Qui a le droit d'exporter ? (tous les utilisateurs, seulement les admins)
