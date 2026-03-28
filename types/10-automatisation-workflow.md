# 10 — Automatisation / Workflow

## Définition

Scripts, pipelines ou scénarios qui automatisent des tâches répétitives entre plusieurs systèmes. Pas d'interface utilisateur complexe. Tourne en arrière-plan.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐⭐ |
| Utilisateurs | Aucun direct (machine-to-machine) |
| Interactions | Déclencheurs → actions → résultats |
| Données | Transitent entre systèmes |
| Hébergement | n8n, Zapier, Make, cron jobs, Cloudflare Workers |
| Cycle de vie | Long terme, maintenance ponctuelle |
| Stack typique | n8n, Zapier, Python scripts, GitHub Actions |

## Sous-types

| Type | Description | Exemple |
|------|-------------|---------|
| ETL / Data pipeline | Extraction, transformation, chargement de données | Sync CRM → base de données |
| Notification automation | Envoi automatique d'alertes/emails | Email de bienvenue après inscription |
| Scheduled tasks | Tâches planifiées (cron) | Rapport hebdomadaire automatique |
| Integration bridge | Pont entre deux systèmes | Webhook Stripe → mise à jour Notion |
| Scraping / monitoring | Surveillance de sites ou APIs | Veille concurrentielle automatique |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Déclencheur (trigger) | Obligatoire | — |
| Actions séquentielles | Obligatoire | — |
| Gestion d'erreurs et retry | Obligatoire | [→](../features/ux/gestion-erreurs.md) |
| Logging | Obligatoire | [→](../features/security/audit-trail.md) |
| Alertes en cas d'échec | Obligatoire | [→](../features/communication/alertes.md) |
| Variables / secrets management | Obligatoire | [→](../features/security/secrets-management.md) |
| Conditions / branches | Recommandé | — |
| Rate limiting respect | Recommandé | [→](../features/security/rate-limiting.md) |
| Idempotence | Recommandé | — |
| Monitoring / dashboard d'exécution | Optionnel | [→](../features/analytics/monitoring.md) |

## Questionnaire de cadrage rapide

1. Quel process doit être automatisé ? Décrire le flux manuellement.
2. Quels systèmes sont impliqués ? (Notion, Slack, email, CRM, API...)
3. Quel est le déclencheur ? (webhook, cron, événement, action manuelle)
4. À quelle fréquence le workflow s'exécute-t-il ?
5. Quel volume de données traité par exécution ?
6. Que se passe-t-il en cas d'erreur ? (retry, alerte, skip)
7. Faut-il un log de chaque exécution ?
8. Y a-t-il des secrets/clés API à gérer ?
9. Quel outil de workflow ? (n8n, Zapier, Make, script custom)
10. Qui monitore et maintient le workflow ?

## Exemple Lina

Workflow n8n : quand un investisseur s'inscrit sur la landing page → créer un contact dans le CRM → envoyer un email de bienvenue → notifier l'équipe sur Slack → ajouter au segment Mailchimp.
