# Loading states

## Définition
Feedback visuel pendant le chargement de données ou le traitement d'actions.

## Sous-features
- [ ] Spinner global (page loading)
- [ ] Skeleton loaders (placeholder de contenu)
- [ ] Barre de progression
- [ ] Bouton loading (désactivé + spinner pendant la soumission)
- [ ] Optimistic UI (afficher le résultat avant confirmation serveur)
- [ ] Pull to refresh (mobile)
- [ ] Loading overlay sur section

## Questionnaire de cadrage
1. Quel pattern de loading ? (spinner, skeleton, barre de progression)
2. Faut-il des skeleton loaders pour les listes et cartes ?
3. Les boutons d'action doivent-ils montrer un état loading ?
4. Faut-il de l'optimistic UI ? (l'action semble instantanée)
5. Sur mobile, faut-il du pull-to-refresh ?
6. Quel est le temps de chargement acceptable ? (< 1s idéal, < 3s acceptable)
