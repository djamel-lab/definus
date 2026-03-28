# Inscription / Connexion

## Définition
Permettre aux utilisateurs de créer un compte et de se connecter pour accéder à un espace protégé. C'est la porte d'entrée de toute application authentifiée.

## Sous-features

- [ ] Inscription par email + mot de passe
- [ ] Inscription par numéro de téléphone + OTP
- [ ] Connexion sociale (Google, Apple, Facebook)
- [ ] Magic link (connexion sans mot de passe par email)
- [ ] Double authentification (2FA / MFA)
- [ ] Vérification d'email
- [ ] Vérification de téléphone (SMS OTP)
- [ ] KYC (vérification d'identité pour plateformes régulées)
- [ ] Captcha / anti-bot
- [ ] Remember me (session persistante)
- [ ] Déconnexion
- [ ] Gestion de sessions multiples (voir/révoquer)
- [ ] Blocage de compte après N tentatives
- [ ] Conditions générales à accepter

## Questionnaire de cadrage

### Méthode d'inscription
1. Comment l'utilisateur crée-t-il un compte ? (email, téléphone, social login, invitation uniquement)
2. Quels champs sont requis à l'inscription ? (nom, prénom, email, téléphone, entreprise...)
3. L'inscription est-elle ouverte à tous ou sur invitation/liste d'attente ?
4. Faut-il une validation d'email avant d'accéder à l'app ?
5. Faut-il un processus KYC (vérification d'identité) ? Si oui, quels documents ?

### Méthode de connexion
6. Comment l'utilisateur se connecte-t-il ? (email + mdp, magic link, social, biométrie)
7. Faut-il de la double authentification (2FA) ? Pour tous ou seulement les admins ?
8. Faut-il une option "rester connecté" ?
9. Après combien de temps d'inactivité la session expire-t-elle ?
10. Faut-il pouvoir voir et révoquer les sessions actives ?

### Sécurité
11. Quelle politique de mot de passe ? (longueur, complexité)
12. Faut-il bloquer le compte après N tentatives échouées ?
13. Faut-il un captcha ? Si oui, à partir de quand ?
14. Y a-t-il des contraintes réglementaires sur l'inscription ? (PSFP, KYC, âge minimum)

### Technique
15. Quel provider d'authentification ? (Supabase Auth, Firebase Auth, Auth0, custom)
16. Quel format de token ? (JWT, session cookie)
17. Faut-il du SSO pour les clients entreprise ?

## Patterns courants

| Contexte | Pattern recommandé |
|----------|-------------------|
| App grand public | Email + social login + magic link |
| App B2B / SaaS | Email + mot de passe + 2FA optionnel + SSO |
| Plateforme régulée (PSFP) | Email + mot de passe + 2FA obligatoire + KYC |
| Outil interne | SSO entreprise ou email + mot de passe |
| Landing page (liste d'attente) | Email seul, pas de compte |
