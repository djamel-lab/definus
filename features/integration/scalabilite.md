# Scalabilité

## Définition
Capacité de l'application à supporter une croissance du nombre d'utilisateurs et du volume de données.

## Questionnaire de cadrage
1. Combien d'utilisateurs simultanés au lancement ? À 6 mois ? À 2 ans ?
2. Quel volume de données ? (nombre de lignes, taille des fichiers)
3. L'architecture est-elle stateless (scalable horizontalement) ?
4. Faut-il de l'auto-scaling ? (ajuster les ressources automatiquement)
5. Quels sont les goulots d'étranglement potentiels ? (BDD, API, uploads)
6. Faut-il du CDN pour les assets ?
7. Faut-il du load balancing ?
8. Faut-il des queues pour les tâches lourdes ? (envoi d'emails en masse, génération de rapports)
