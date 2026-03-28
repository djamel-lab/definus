# Cahier des charges — Skill "definus"

## 1. Positionnement

Cette skill permet à Claude de **générer des spécifications logicielles complètes** quand l'utilisateur veut spécifier un logiciel, une application, un dashboard ou tout autre type de soft, en suivant un **workflow d'interview structuré** basé sur une bibliothèque de fonctionnalités-type, pour que l'utilisateur obtienne un **SPECS.md prêt pour le développement** en 15-20 minutes.

## 2. Catégorie

**Catégorie 2** — Automatisation de workflow

Justification : la skill orchestre un processus multi-étapes (identification → sélection → cadrage → génération) qui implique des lectures de fichiers de référence (GitHub), des questions structurées, et la production d'un document final.

## 3. Cas d'usage

### Cas 1 — Spécifier une nouvelle application
- **Scénario** : "Je veux spécifier l'espace investisseur de Lina Capital"
- **Étapes** : Identification (App Web + Dashboard) → Sélection features → Questionnaire par blocs → Génération SPECS.md
- **Résultat** : SPECS.md complet avec modèle de données, pages, features détaillées, stack technique
- **Triggers** : "spécifier", "specs pour", "cahier des charges de", "je veux définir", "SPECS.md pour"

### Cas 2 — Spécifier un dashboard
- **Scénario** : "Je veux un dashboard pour suivre les KPIs de collecte Lina"
- **Étapes** : Identification (Dashboard) → Sélection KPIs et graphiques → Questionnaire data/filtres → Génération SPECS.md
- **Résultat** : SPECS.md avec KPIs listés, sources de données, types de graphiques, filtres
- **Triggers** : "dashboard pour", "tableau de bord", "reporting de"

### Cas 3 — Spécifier une landing page
- **Scénario** : "Je dois faire une landing page pour le nouveau produit"
- **Étapes** : Identification (Landing Page) → Questions rapides (CTA, tracking, formulaire) → Génération SPECS.md léger
- **Résultat** : SPECS.md simple avec sections, contenus, CTA, tracking, mentions légales
- **Triggers** : "landing page pour", "page de conversion"

### Anti-triggers
- "Le code de mon app" → lina-dev (développement, pas spécification)
- "Audite ma landing page" → lp-auditor (audit CRO, pas spécification)
- "Définis une nouvelle skill" → skill-definition (skill Claude, pas logiciel)
- "Apprends-moi à spécifier" → speed-learner (formation, pas production)

## 4. Complexité

| Axe | Score |
|-----|-------|
| Nombre d'étapes | Moyen (4-7) = 2 |
| Outils externes | Moyen (GitHub MCP) = 2 |
| Fichiers de référence | Complexe (60+ fichiers dans le repo) = 3 |
| Scripts exécutables | Simple (0) = 1 |
| Domaines couverts | Complexe (10 types de logiciel) = 3 |
| Points de décision | Moyen (type, features, stack) = 2 |
| **Total** | **13 / 18** |

**Décision** : Pas de découpage. Bien que le score soit élevé, la skill est un workflow linéaire (pas de branches indépendantes). La complexité vient de la bibliothèque de référence, pas du flux.

**Gestion de la complexité** : Progressive disclosure — les fichiers de référence sont chargés à la demande depuis GitHub, pas tous en même temps.

## 5. Architecture

### 5.1 Logigramme

```
[Utilisateur décrit son projet]
        │
        ▼
[Phase 1: Identifier le type]
   Lire TAXONOMY.md + arbre de décision
        │
        ▼
[Combinaison de types ?]──oui──▶ [Lister les composants]
        │ non                           │
        ▼                               ▼
[Phase 2: Charger la fiche du type]
   Lire types/XX-xxx.md
   Présenter les features standard
        │
        ▼
[Utilisateur valide les features]
        │
        ▼
[Phase 3: Questionnaire par blocs]
   Pour chaque feature retenue:
     Lire features/category/feature.md
     Poser les questions pertinentes
     Déduire quand possible
        │
        ▼
[Toutes les réponses collectées ?]
   │ non → Poser le bloc suivant
   │ oui ↓
        ▼
[Phase 4: Générer SPECS.md]
   Lire templates/SPECS-TEMPLATE.md
   Remplir chaque section
   Pousser sur GitHub si demandé
        │
        ▼
[Livraison du SPECS.md]
```

### 5.2 Structure de fichiers

```
definus/                        ← Skill Claude
├── SKILL.md                    ← Instructions principales
└── (références chargées depuis GitHub: djamel-lab/definus)
```

La skill elle-même est légère. Toute la bibliothèque de référence est dans le repo GitHub `djamel-lab/definus` et chargée à la demande via le MCP GitHub.

### 5.3 Progressive disclosure

- **Niveau 1** (frontmatter) : name + description — toujours chargé
- **Niveau 2** (SKILL.md body) : workflow en 4 phases, règles d'interview, template de questionnaire
- **Niveau 3** (GitHub à la demande) : TAXONOMY.md, types/XX.md, features/category/feature.md, templates/SPECS-TEMPLATE.md

### 5.4 Dépendances

- **MCP GitHub** : `github_read_file` pour charger les fichiers de référence depuis `djamel-lab/definus`
- **MCP GitHub** : `github_create_file` pour pousser le SPECS.md dans le repo du projet
- **Aucun package externe** requis

## 6. Spécifications

### 6.1 Frontmatter

```yaml
name: definus
description: >
  Génère des spécifications logicielles complètes (SPECS.md) pour tout type de
  logiciel : application web, mobile, dashboard, API, SaaS, landing page, outil
  interne, extension navigateur, automatisation. Déclenche ce skill dès que
  l'utilisateur mentionne "spécifier", "specs pour", "cahier des charges",
  "SPECS.md", "définir les features de", "je veux construire", "spécifications
  pour", ou toute intention de cadrer un logiciel avant de le développer. Aussi
  quand l'utilisateur dit "qu'est-ce qu'il me faut pour faire [type de soft]".
  Utilise une bibliothèque de 60+ fonctionnalités-type avec questionnaires de
  cadrage et produit un document structuré prêt pour le développement. Ne PAS
  déclencher pour du développement (utiliser lina-dev), de l'audit de landing
  page (utiliser lp-auditor), ou de la définition de skill (utiliser
  skill-definition).
```

### 6.2 Workflow détaillé

Voir WORKFLOW.md dans le repo definus.

### 6.3 Template de sortie

Voir templates/SPECS-TEMPLATE.md dans le repo definus.

### 6.4 Boucles de feedback

1. Après Phase 1 (identification) : "J'ai identifié que c'est un [TYPE]. C'est correct ?"
2. Après Phase 2 (features) : "Voici les features que je recommande. Tu veux ajouter/retirer quelque chose ?"
3. Après Phase 4 (génération) : "Voici le SPECS.md. Je le pousse sur GitHub ?"

### 6.5 Critères de succès

**Quantitatifs** :
- Le SPECS.md couvre au moins 80% des features standard du type identifié
- Le workflow prend moins de 20 minutes pour un projet standard
- Moins de 3 allers-retours de clarification par bloc

**Qualitatifs** :
- L'utilisateur n'a pas à réexpliquer le contexte
- Le SPECS.md est directement exploitable par lina-dev/Claude Code
- Les questions posées sont pertinentes (pas de questions hors sujet)

## 7. Checklist de validation

- [x] La description inclut QUOI + QUAND
- [x] Les trigger phrases couvrent les formulations variées
- [x] Les anti-triggers évitent le sur-déclenchement
- [x] Le nom est en kebab-case, ≤ 64 caractères
- [x] Pas de XML dans le frontmatter
- [x] Pas de "claude" ou "anthropic" dans le nom
- [x] SKILL.md estimé sous 500 lignes
- [x] Détails avancés dans des fichiers séparés (GitHub)
- [x] Pas d'information temporelle
- [x] Terminologie cohérente
- [x] Exemples concrets
- [x] Étapes claires et séquentielles
- [x] Points de décision explicites
- [x] Boucles de feedback pour les tâches critiques
- [x] Gestion d'erreur incluse (déduction, défauts)
- [x] Au moins 3 cas de test
- [x] Tests négatifs (anti-triggers)

## 8. Instructions pour skill-creator

```
Utilise le skill-creator pour construire la skill "definus" à partir
de ce cahier des charges. La skill doit :

1. Lire TAXONOMY.md depuis djamel-lab/definus via le MCP GitHub
2. Identifier le type de logiciel
3. Charger la fiche du type (types/XX-xxx.md)
4. Présenter les features et recueillir les choix
5. Pour chaque feature retenue, charger le questionnaire (features/category/xxx.md)
6. Poser les questions par blocs en déduisant quand possible
7. Générer le SPECS.md en utilisant templates/SPECS-TEMPLATE.md
8. Proposer de pousser sur GitHub

Le SKILL.md doit contenir le workflow complet mais PAS la bibliothèque
de features (elle est dans le repo GitHub et chargée à la demande).
```
