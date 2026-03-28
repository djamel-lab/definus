# Mode offline

## Définition
Permettre à l'application mobile de fonctionner sans connexion internet, avec synchronisation des données quand la connexion revient.

## Sous-features

- [ ] Cache des données consultées
- [ ] Création de données en offline (queue locale)
- [ ] Synchronisation automatique au retour en ligne
- [ ] Gestion des conflits (modification simultanée online/offline)
- [ ] Indicateur de mode offline
- [ ] Stockage local (SQLite, AsyncStorage, MMKV)

## Questionnaire de cadrage

1. Quelles fonctionnalités doivent marcher offline ? (lecture seule, création, modification)
2. Quelles données doivent être disponibles en cache offline ?
3. Combien de données stocker localement ? (dernières 50 entrées, tout)
4. Comment gérer les conflits si la même donnée a été modifiée online et offline ?
5. Faut-il un indicateur visuel quand l'utilisateur est offline ?
6. La synchronisation au retour en ligne est-elle automatique ou manuelle ?
7. Quel stockage local ? (SQLite, AsyncStorage, WatermelonDB)
