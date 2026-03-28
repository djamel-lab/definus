# Versioning API

## Définition
Stratégie pour faire évoluer l'API sans casser les clients existants.

## Questionnaire de cadrage
1. Quelle stratégie de versioning ? (URL: /v1/, header: Accept-Version, query: ?version=1)
2. Combien de versions maintenir en parallèle ?
3. Quelle politique de dépréciation ? (durée avant suppression d'une ancienne version)
4. Comment communiquer les changements ? (changelog, email, header Sunset)
5. Faut-il un mécanisme de migration automatique ?
