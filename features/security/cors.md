# CORS

## Définition
Cross-Origin Resource Sharing : contrôle quels domaines peuvent appeler l'API depuis un navigateur.

## Questionnaire de cadrage
1. Quels domaines front-end appellent l'API ? (lister tous les domaines autorisés)
2. Faut-il autoriser les credentials (cookies) cross-origin ?
3. Quels headers custom sont utilisés ?
4. Quelles méthodes HTTP autoriser ? (GET, POST, PUT, DELETE, PATCH)
5. Y a-t-il des environnements différents ? (dev: *, staging: domaine spécifique, prod: domaine spécifique)
