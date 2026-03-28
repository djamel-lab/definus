# Emails transactionnels

## Définition
Emails automatiques envoyés en réponse à une action utilisateur ou un événement système. Pas du marketing, mais des emails fonctionnels.

## Sous-features
- [ ] Email de bienvenue / confirmation d'inscription
- [ ] Email de vérification d'adresse
- [ ] Email de réinitialisation de mot de passe
- [ ] Email de confirmation d'action (paiement, soumission, modification)
- [ ] Email de notification (nouveau message, changement de statut)
- [ ] Email de rappel (action en attente, échéance)
- [ ] Email récapitulatif périodique (digest hebdo)
- [ ] Templates HTML responsive
- [ ] Variables dynamiques (nom, montant, date, lien)
- [ ] Tracking (ouverture, clic)
- [ ] Gestion des bounces et désinscription

## Questionnaire de cadrage
1. Quels emails transactionnels sont nécessaires ? Lister chacun avec le déclencheur.
2. Faut-il des templates HTML ou du texte simple ?
3. Qui est l'expéditeur ? (noreply@domain, support@domain, personne)
4. Quelles variables dynamiques par email ? (nom, montant, lien, date)
5. Faut-il du tracking ? (ouverture, clic)
6. Quel provider d'envoi ? (Resend, SendGrid, Postmark, SES, Brevo)
7. Faut-il un lien de désinscription ?
8. Faut-il un récapitulatif périodique ? (digest quotidien/hebdo)
9. Y a-t-il des contraintes de deliverability ? (SPF, DKIM, DMARC configurés)
10. Dans quelle(s) langue(s) ?
