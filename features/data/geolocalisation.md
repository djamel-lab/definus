# Géolocalisation

## Définition
Utilisation de la position GPS de l'utilisateur pour afficher du contenu contextualisé, des cartes, ou des fonctionnalités basées sur la localisation.

## Sous-features

- [ ] Récupération position GPS
- [ ] Affichage carte (Google Maps, Mapbox, OpenStreetMap)
- [ ] Marqueurs sur carte
- [ ] Recherche par adresse (geocoding)
- [ ] Calcul de distance/itinéraire
- [ ] Geofencing (alertes quand l'utilisateur entre/sort d'une zone)
- [ ] Store locator (trouver le point le plus proche)

## Questionnaire de cadrage

1. Pourquoi avez-vous besoin de géolocalisation ? (afficher sur carte, trouver le plus proche, tracking)
2. Faut-il une carte interactive ? Quel provider ? (Google Maps, Mapbox, Leaflet)
3. Faut-il de la recherche par adresse (geocoding) ?
4. Faut-il calculer des distances ou des itinéraires ?
5. La localisation est-elle ponctuelle ou en continu (tracking) ?
6. Faut-il du geofencing ? (notifications quand l'utilisateur entre dans une zone)
7. Quelles autorisations demander ? (toujours, en utilisation, jamais)
