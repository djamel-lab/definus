# Crash reporting

## Définition
Détection et rapport automatique des crashes et erreurs sur mobile.

## Sous-features
- [ ] Crash reporting automatique (Sentry, Firebase Crashlytics)
- [ ] Stack trace avec contexte
- [ ] Breadcrumbs (actions avant le crash)
- [ ] Regroupement par type d'erreur
- [ ] Alertes en cas de spike d'erreurs
- [ ] Informations device (modèle, OS, version app)

## Questionnaire de cadrage
1. Quel outil ? (Sentry, Firebase Crashlytics, Bugsnag)
2. Faut-il des alertes en temps réel ? Par quel canal ?
3. Faut-il du source map upload pour des stack traces lisibles ?
4. Qui reçoit les rapports de crash ?
5. Y a-t-il un SLA sur le temps de correction des crashs critiques ?
