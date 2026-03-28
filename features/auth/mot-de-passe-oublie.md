# Mot de passe oublié

## Définition
Permettre à un utilisateur qui a oublié son mot de passe de le réinitialiser de manière sécurisée.

## Sous-features

- [ ] Demande de réinitialisation par email
- [ ] Demande de réinitialisation par SMS
- [ ] Lien de réinitialisation avec token temporaire
- [ ] Page de création du nouveau mot de passe
- [ ] Expiration du lien (durée configurable)
- [ ] Invalidation des anciennes sessions après changement
- [ ] Notification de changement de mot de passe
- [ ] Protection anti-abus (rate limiting sur les demandes)

## Questionnaire de cadrage

1. Par quel canal l'utilisateur reçoit-il le lien de réinitialisation ? (email, SMS, les deux)
2. Combien de temps le lien de réinitialisation est-il valide ? (15 min, 1h, 24h)
3. Faut-il invalider toutes les sessions existantes après un changement de mot de passe ?
4. Faut-il envoyer une notification (email/SMS) confirmant le changement ?
5. Faut-il limiter le nombre de demandes de réinitialisation ? (ex: max 3/heure)
6. L'utilisateur doit-il fournir des informations supplémentaires pour prouver son identité ?
7. Y a-t-il une politique spéciale pour les comptes admin ? (process de réinitialisation renforcé)
