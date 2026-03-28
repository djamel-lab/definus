# Alertes et seuils

## Définition
Notifications automatiques quand une métrique dépasse un seuil défini. Utilisé dans les dashboards et les automatisations.

## Sous-features
- [ ] Définition de seuils par KPI
- [ ] Alertes email
- [ ] Alertes Slack / Teams
- [ ] Alertes SMS (critique)
- [ ] Fréquence de vérification configurable
- [ ] Historique des alertes
- [ ] Escalade (si pas de réponse en N minutes → alerte niveau supérieur)
- [ ] Snooze / mute temporaire

## Questionnaire de cadrage
1. Quelles métriques déclenchent des alertes ? Lister avec les seuils.
2. Par quel canal ? (email, Slack, SMS, notification in-app)
3. Faut-il de l'escalade ? (si pas de réponse → alerte au niveau supérieur)
4. Qui reçoit quelle alerte ? (mapping rôle → type d'alerte)
5. Peut-on snooze / muter temporairement une alerte ?
6. À quelle fréquence vérifier les seuils ? (temps réel, toutes les 5 min, toutes les heures)
7. Faut-il un historique des alertes déclenchées ?
