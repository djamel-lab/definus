# Notifications in-app

## Définition
Système de notifications au sein de l'application pour informer les utilisateurs d'événements importants.

## Sous-features
- [ ] Centre de notifications (cloche avec badge)
- [ ] Notifications en temps réel
- [ ] Notifications lues / non lues
- [ ] Marquer tout comme lu
- [ ] Types de notifications (info, warning, success, action requise)
- [ ] Actions directes depuis la notification (approuver, voir, supprimer)
- [ ] Préférences de notification par type
- [ ] Historique des notifications
- [ ] Notification toast (popup temporaire)

## Questionnaire de cadrage
1. Quels événements déclenchent une notification ? Lister chacun.
2. Les notifications sont-elles en temps réel ou chargées au rafraîchissement ?
3. Faut-il un centre de notifications (page/panneau avec historique) ?
4. Faut-il des toasts (popups temporaires) en plus du centre de notifications ?
5. L'utilisateur peut-il configurer ses préférences ? (activer/désactiver par type)
6. Certaines notifications nécessitent-elles une action ? (approuver, refuser)
7. Combien de temps garder les notifications en historique ?
8. Faut-il aussi envoyer par email en parallèle ?
9. Quel provider temps réel ? (Supabase Realtime, Pusher, polling)
