# Gestion d'erreurs

## Définition
Comment l'application communique les erreurs aux utilisateurs et aux développeurs.

## Sous-features
- [ ] Page 404 (not found) personnalisée
- [ ] Page 500 (erreur serveur) personnalisée
- [ ] Messages d'erreur user-friendly (pas de stack trace)
- [ ] Toast / notification d'erreur
- [ ] Retry automatique (pour les erreurs réseau)
- [ ] Error boundary (React)
- [ ] Logging des erreurs côté serveur
- [ ] Codes d'erreur API standardisés
- [ ] Fallback gracieux (afficher un état dégradé plutôt que rien)

## Questionnaire de cadrage
1. Faut-il des pages d'erreur custom ? (404, 500, 403, maintenance)
2. Comment afficher les erreurs utilisateur ? (toast, inline, modal, page)
3. Faut-il du retry automatique pour les erreurs réseau ?
4. Les erreurs API suivent-elles un format standard ? (code, message, details)
5. Faut-il un error boundary global ? (React : capturer les crashes de composants)
6. Faut-il un mode maintenance ?
7. Les erreurs sont-elles loguées ? (Sentry, console, fichier)
