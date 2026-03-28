# Notifications push

## Définition
Notifications envoyées sur le smartphone de l'utilisateur même quand l'application est fermée. Spécifique mobile.

## Sous-features
- [ ] Push notifications iOS (APNs)
- [ ] Push notifications Android (FCM)
- [ ] Rich push (image, boutons d'action)
- [ ] Deep link depuis la notification (ouvrir un écran spécifique)
- [ ] Segmentation (envoyer à un groupe d'utilisateurs)
- [ ] Scheduling (programmer l'envoi)
- [ ] Analytics push (taux d'ouverture, taux de clic)
- [ ] Gestion des permissions (demander au bon moment)
- [ ] Silent push (mise à jour en background)

## Questionnaire de cadrage
1. Quels événements déclenchent un push ? Lister chacun avec le message type.
2. Les push sont-ils automatiques (événement) ou manuels (campagne marketing) ?
3. Faut-il des rich push (image, boutons) ?
4. Faut-il du deep linking ? (clic sur la notif → écran spécifique)
5. Faut-il pouvoir segmenter les destinataires ?
6. Faut-il du scheduling (programmer l'envoi) ?
7. Quel provider ? (Firebase Cloud Messaging, OneSignal, Expo Push)
8. Faut-il des analytics sur les push ? (taux ouverture, conversion)
9. Quand demander la permission push ? (premier lancement, après une action clé)
