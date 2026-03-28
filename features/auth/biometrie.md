# Authentification biométrique

## Définition
Connexion via empreinte digitale (Touch ID / fingerprint) ou reconnaissance faciale (Face ID) sur mobile.

## Sous-features

- [ ] Face ID / Face Unlock
- [ ] Touch ID / Fingerprint
- [ ] Fallback vers PIN / mot de passe
- [ ] Activation optionnelle par l'utilisateur
- [ ] Biométrie pour actions sensibles (paiement, signature)

## Questionnaire de cadrage

1. La biométrie remplace-t-elle le mot de passe ou est-elle un complément ?
2. Faut-il un fallback (PIN, mot de passe) si la biométrie échoue ?
3. L'activation de la biométrie est-elle obligatoire ou optionnelle ?
4. La biométrie est-elle utilisée uniquement pour la connexion ou aussi pour des actions sensibles ? (validation de paiement, signature de document)
5. Quels appareils minimum supporter ? (iOS 14+, Android 10+)
