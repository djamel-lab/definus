# 04 — Dashboard / Reporting

## Définition

Interface de visualisation de données en temps réel ou quasi temps réel. Graphiques, KPIs, tableaux. L'utilisateur consulte et analyse mais ne crée pas de contenu. Peut être interne (équipe) ou externe (client).

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐⭐ |
| Utilisateurs | Authentifiés (managers, analystes, clients) |
| Interactions | Lecture, filtrage, drill-down, export |
| Données | Dynamiques, agrégées, volumineuses |
| Hébergement | Serveur ou outil no-code (Metabase, Grafana, Retool) |
| Cycle de vie | Long terme, données évolutives |
| Stack typique | React + Recharts/D3 + API, ou Metabase/Retool |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Authentification | Obligatoire | [→](../features/auth/inscription-connexion.md) |
| Rôles et permissions | Obligatoire | [→](../features/auth/roles-permissions.md) |
| KPIs en temps réel | Obligatoire | [→](../features/analytics/kpis.md) |
| Graphiques interactifs | Obligatoire | [→](../features/analytics/graphiques.md) |
| Tableaux de données | Obligatoire | [→](../features/data/tableaux.md) |
| Filtres et période | Obligatoire | [→](../features/data/recherche-filtres.md) |
| Export (PDF, CSV, Excel) | Recommandé | [→](../features/data/export-donnees.md) |
| Drill-down / navigation dans les données | Recommandé | [→](../features/analytics/drill-down.md) |
| Alertes et seuils | Optionnel | [→](../features/communication/alertes.md) |
| Rafraîchissement automatique | Recommandé | [→](../features/data/temps-reel.md) |
| Responsive / mobile | Recommandé | [→](../features/ux/responsive.md) |
| Mode sombre | Optionnel | [→](../features/ux/theme.md) |
| Partage / embed | Optionnel | [→](../features/integration/partage-embed.md) |

## Questionnaire de cadrage rapide

1. Qui consulte ce dashboard ? (interne, client, les deux)
2. Quels sont les 5-10 KPIs principaux à afficher ?
3. D'où viennent les données ? (base SQL, API, Google Sheets, fichiers)
4. À quelle fréquence les données sont-elles mises à jour ?
5. Faut-il du temps réel (WebSocket) ou du quasi temps réel (polling) ?
6. Quels types de graphiques ? (barres, lignes, camembert, cartes, jauges)
7. Les utilisateurs doivent-ils pouvoir filtrer par période, catégorie, etc. ?
8. Faut-il des alertes quand un KPI dépasse un seuil ?
9. Faut-il exporter les données ou les graphiques ? (PDF, CSV, Excel)
10. Y a-t-il un outil existant (Metabase, Grafana) ou faut-il du custom ?
11. Combien de vues/pages différentes dans le dashboard ?
12. Y a-t-il des données sensibles nécessitant une restriction d'accès ?

## Exemple Lina

Dashboard interne Lina Finance avec KPIs de collecte, nombre d'investisseurs actifs, taux de défaut, montants investis par période, statut des projets en cours.
