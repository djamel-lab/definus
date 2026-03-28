# Temps réel

## Définition
Mise à jour automatique des données affichées sans rechargement de page. L'utilisateur voit les changements instantanément.

## Sous-features

- [ ] WebSocket / Server-Sent Events
- [ ] Polling (rafraîchissement périodique)
- [ ] Indicateur de mise à jour en cours
- [ ] Notification de nouvelles données
- [ ] Synchronisation multi-onglets
- [ ] Presence (voir qui est en ligne)
- [ ] Collaboration en temps réel (édition simultanée)

## Questionnaire de cadrage

1. Quelles données doivent être en temps réel ? (KPIs, notifications, statuts, messages)
2. Quel degré de temps réel ? (instantané via WebSocket, quasi temps réel via polling 5-30s)
3. Combien d'utilisateurs simultanés maximum ?
4. Faut-il de la présence (voir qui est connecté) ?
5. Faut-il de la collaboration en temps réel (plusieurs personnes éditent le même élément) ?
6. Quel provider ? (Supabase Realtime, Pusher, Ably, Socket.io custom)
7. Que se passe-t-il en cas de perte de connexion ? (reconnexion auto, message d'erreur)
