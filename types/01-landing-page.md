# 01 — Landing Page

## Définition

Page web unique conçue pour convertir un visiteur en lead ou en client. Objectif unique, message ciblé, CTA clair. Pas de navigation complexe.

## Caractéristiques

| Critère | Valeur |
|---------|--------|
| Complexité | ⭐ |
| Utilisateurs | Anonymes (trafic payant/organique) |
| Interactions | Lecture + formulaire |
| Données | Statiques + collecte leads |
| Hébergement | Statique (CDN, Cloudflare Pages, Netlify) |
| Cycle de vie | Court (campagne) ou permanent (produit) |
| Stack typique | HTML/CSS/JS ou React/Next.js |

## Fonctionnalités standard

| Feature | Priorité | Questionnaire |
|---------|----------|--------------|
| Hero section | Obligatoire | [→](../features/ux/onboarding.md) |
| CTA principal | Obligatoire | [→](../features/ux/cta.md) |
| Formulaire de capture | Obligatoire | [→](../features/data/formulaires.md) |
| Social proof (témoignages, logos) | Recommandé | [→](../features/content/social-proof.md) |
| FAQ accordéon | Recommandé | [→](../features/content/faq.md) |
| Compteurs animés | Optionnel | [→](../features/ux/animations.md) |
| A/B testing | Optionnel | [→](../features/analytics/ab-testing.md) |
| SEO on-page | Obligatoire | [→](../features/ux/seo.md) |
| Analytics / tracking | Obligatoire | [→](../features/analytics/tracking.md) |
| Responsive design | Obligatoire | [→](../features/ux/responsive.md) |
| Mentions légales | Obligatoire | [→](../features/security/mentions-legales.md) |
| Cookie banner | Obligatoire (RGPD) | [→](../features/security/rgpd.md) |

## Questionnaire de cadrage rapide

1. Quel est l'objectif unique de cette page ? (inscription, téléchargement, achat, prise de RDV)
2. Quelle est la source de trafic principale ? (SEA, SEO, réseaux sociaux, email)
3. Quelle est la cible ? (persona, niveau de conscience du problème)
4. Quel est le message principal en une phrase ?
5. Y a-t-il un formulaire ? Quels champs ?
6. Où vont les données collectées ? (CRM, email, Notion, Google Sheets)
7. Faut-il du tracking ? (GA4, Pixel Meta, GTM)
8. Y a-t-il des contraintes réglementaires ? (mentions AMF, PSFP, RGPD)
9. Budget et deadline ?
10. Existe-t-il une charte graphique à respecter ?

## Exemple Lina

Le site **lina-capital** (repo `djamel-lab/lina-capital`) est une landing page type avec hero, profils, processus, FAQ, formulaire de liste d'attente, et mentions PSFP.
