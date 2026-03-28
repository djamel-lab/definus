# 05 — Application Mobile

## Définition

Application installée sur smartphone (iOS et/ou Android). Accès aux fonctionnalités natives du device (push notifications, caméra, GPS, biométrie). Peut être native, hybride ou PWA.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐⭐⭐ |
| Utilisateurs | Authentifiés (clients grand public ou B2B) |
| Interactions | Touch, gestes, notifications push, offline |
| Données | Synchronisées cloud + cache local |
| Hébergement | App Store + Google Play + API backend |
| Cycle de vie | Long terme, mises à jour régulières, review stores |
| Stack typique | React Native, Flutter, Swift/Kotlin natif |

## Sous-types

| Approche | Description | Quand choisir |
|----------|-------------|---------------|
| Native (Swift/Kotlin) | Code spécifique par OS | Performance critique, accès hardware avancé |
| Cross-platform (React Native, Flutter) | Code partagé iOS/Android | Budget limité, time-to-market rapide |
| PWA | App web installable | MVP, pas besoin de features natives avancées |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Inscription / Connexion | Obligatoire | [→](../features/auth/inscription-connexion.md) |
| Authentification biométrique | Recommandé | [→](../features/auth/biometrie.md) |
| Mot de passe oublié | Obligatoire | [→](../features/auth/mot-de-passe-oublie.md) |
| Profil utilisateur | Obligatoire | [→](../features/auth/profil-utilisateur.md) |
| Notifications push | Obligatoire | [→](../features/communication/notifications-push.md) |
| Navigation (tab bar, drawer) | Obligatoire | [→](../features/ux/navigation-mobile.md) |
| Mode offline | Recommandé | [→](../features/data/mode-offline.md) |
| Upload photo/document | Recommandé | [→](../features/content/upload-fichiers.md) |
| Géolocalisation | Optionnel | [→](../features/data/geolocalisation.md) |
| Deep linking | Recommandé | [→](../features/ux/deep-linking.md) |
| Onboarding (tutoriel) | Recommandé | [→](../features/ux/onboarding.md) |
| In-app updates | Recommandé | [→](../features/ux/mise-a-jour.md) |
| Analytics mobile | Obligatoire | [→](../features/analytics/tracking.md) |
| Crash reporting | Obligatoire | [→](../features/security/crash-reporting.md) |
| Accessibilité | Obligatoire | [→](../features/ux/accessibilite.md) |
| App Store / Play Store (ASO) | Obligatoire | [→](../features/ux/aso.md) |

## Questionnaire de cadrage rapide

1. iOS, Android ou les deux ?
2. Approche technique : native, cross-platform (React Native/Flutter), ou PWA ?
3. Quels sont les 3-5 écrans principaux ?
4. Quelles fonctionnalités natives sont nécessaires ? (caméra, GPS, biométrie, NFC, push)
5. L'app doit-elle fonctionner offline ? Si oui, quelles données en cache ?
6. Y a-t-il une app web existante dont l'app mobile est le compagnon ?
7. Quel est le volume d'utilisateurs cible ?
8. Y a-t-il des contraintes de performance (taille app, temps de chargement) ?
9. Qui gère la publication sur les stores ? (compte développeur existant ?)
10. Fréquence de mises à jour prévue ?
11. Y a-t-il des contraintes réglementaires spécifiques mobile ? (RGPD, données bancaires)
12. Budget pour les deux plateformes ou une seule d'abord ?

## Exemple Lina

Application investisseur Lina Capital : consultation du portfolio, suivi des projets investis, notifications sur les rendements, upload KYC, authentification biométrique.
