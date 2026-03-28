# Webhooks

## Définition
Callbacks HTTP envoyés automatiquement vers une URL externe quand un événement se produit dans l'application.

## Sous-features
- [ ] Configuration d'URL de webhook par événement
- [ ] Liste des événements disponibles
- [ ] Payload JSON signé (HMAC)
- [ ] Retry en cas d'échec (avec backoff exponentiel)
- [ ] Log des webhooks envoyés (succès/échec)
- [ ] Interface de test (renvoyer un webhook)
- [ ] Webhook secret pour vérification

## Questionnaire de cadrage
1. Quels événements déclenchent des webhooks ? (création, modification, paiement, etc.)
2. Quel format de payload ? (JSON)
3. Faut-il signer les payloads ? (HMAC SHA256)
4. Combien de retry en cas d'échec ? Quel intervalle ?
5. Faut-il un log des webhooks envoyés avec statut ?
6. L'utilisateur configure-t-il ses webhooks depuis l'interface ou via API ?
7. Faut-il un outil de test/debugging ? (renvoyer un webhook, voir le payload)
