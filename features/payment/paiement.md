# Paiement en ligne

## Définition
Permettre aux utilisateurs de payer directement dans l'application par carte bancaire, virement ou autre moyen de paiement.

## Sous-features
- [ ] Paiement par carte bancaire
- [ ] Paiement par virement SEPA
- [ ] Prélèvement automatique
- [ ] Apple Pay / Google Pay
- [ ] 3D Secure
- [ ] Page de paiement (checkout)
- [ ] Paiement en plusieurs fois
- [ ] Remboursement
- [ ] Reçu automatique
- [ ] Gestion des échecs de paiement
- [ ] Webhook de confirmation de paiement

## Questionnaire de cadrage
1. Quels moyens de paiement ? (carte, virement SEPA, prélèvement, Apple/Google Pay)
2. Faut-il du paiement récurrent (abonnement) ou ponctuel ?
3. Faut-il du paiement en plusieurs fois ?
4. Quel PSP (Payment Service Provider) ? (Stripe, Mangopay, Lemonway, Adyen)
5. Faut-il du 3D Secure ?
6. Comment gérer les échecs ? (retry automatique, notification, suspension)
7. Faut-il des remboursements ? (automatiques, manuels, partiels)
8. Faut-il un reçu/confirmation automatique ?
9. Y a-t-il des contraintes réglementaires ? (PCI-DSS, finance islamique)
10. Faut-il un compte séquestre / escrow ? (pour les plateformes de crowdfunding)
11. Dans quelle devise ? (EUR, USD, multi-devise)
12. Quel flux : redirect vers page Stripe ou paiement intégré ?
