# Audit trail

## Définition
Journal d'événements qui enregistre qui a fait quoi et quand dans l'application. Essentiel pour la conformité et le debugging.

## Sous-features
- [ ] Log de toutes les actions utilisateur (création, modification, suppression)
- [ ] Log des connexions / déconnexions
- [ ] Log des changements de rôle/permission
- [ ] Horodatage précis (timestamp + timezone)
- [ ] Identité de l'auteur (user ID, IP, device)
- [ ] Avant/après (valeur avant et après modification)
- [ ] Recherche et filtres dans les logs
- [ ] Rétention configurable
- [ ] Export des logs
- [ ] Immutabilité (logs non modifiables)

## Questionnaire de cadrage
1. Quelles actions doivent être loguées ? (toutes, seulement les critiques)
2. Faut-il stocker le avant/après des modifications ?
3. Quelles métadonnées ? (IP, user agent, device, géolocalisation)
4. Combien de temps conserver les logs ? (30 jours, 1 an, 5 ans, illimité)
5. Qui peut consulter les logs ? (admin seulement, compliance, tout le monde sur ses propres actions)
6. Faut-il pouvoir exporter les logs ?
7. Les logs doivent-ils être immutables ? (contrainte réglementaire)
8. Quel stockage ? (même base, base séparée, service externe comme Datadog)
