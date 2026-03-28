# 09 — Extension Navigateur

## Définition

Plugin installé dans Chrome, Firefox ou Safari qui ajoute des fonctionnalités au navigateur ou modifie le comportement de pages web existantes. Souvent un outil de productivité ou un connecteur.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐ |
| Utilisateurs | Utilisateurs du navigateur ciblé |
| Interactions | Popup, sidebar, injection dans pages |
| Données | Locales (storage) + API distante optionnelle |
| Hébergement | Chrome Web Store / Firefox Add-ons |
| Cycle de vie | Moyen terme, mises à jour via le store |
| Stack typique | HTML/CSS/JS, Manifest V3 (Chrome) |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Popup interface | Obligatoire | — |
| Content script (injection dans pages) | Optionnel | — |
| Background service worker | Recommandé | — |
| Storage local | Obligatoire | — |
| Authentification (si connecté à un service) | Optionnel | [→](../features/auth/auth-api.md) |
| Communication avec API backend | Optionnel | [→](../features/integration/documentation-api.md) |
| Raccourcis clavier | Recommandé | — |
| Badge / icône dynamique | Optionnel | — |
| Options / settings page | Recommandé | [→](../features/ux/settings.md) |
| Permissions minimales | Obligatoire | [→](../features/security/permissions-extension.md) |

## Questionnaire de cadrage rapide

1. Quel navigateur cibler ? (Chrome d'abord, puis Firefox/Safari ?)
2. Que fait l'extension en une phrase ?
3. L'extension a-t-elle une popup, une sidebar, ou injecte-t-elle du contenu dans des pages ?
4. Quelles pages web sont ciblées ? (toutes, un domaine spécifique)
5. L'extension communique-t-elle avec un serveur backend ?
6. Quelles données sont stockées localement ?
7. Quelles permissions sont nécessaires ? (tabs, activeTab, storage, cookies)
8. Y a-t-il une authentification utilisateur ?
9. Faut-il des raccourcis clavier ?
10. Quel est le processus de publication sur le store ?

## Exemple Lina

Extension Chrome interne "Claudus" pour interfacer Claude avec le navigateur et exécuter des tâches autonomes sur des pages web.
