# Definus — Générateur intelligent de spécifications logicielles

**Definus** est une bibliothèque structurée qui permet de produire des spécifications complètes pour n'importe quel type de logiciel en quelques minutes.

## Principe

Au lieu de partir d'une page blanche, Definus fonctionne comme un **constructeur de specs par assemblage** :

1. **Choisir le type de logiciel** → la taxonomie propose les catégories pertinentes
2. **Sélectionner les fonctionnalités** → la bibliothèque propose les features standards
3. **Répondre aux questionnaires** → chaque feature a un questionnaire de cadrage précis
4. **Générer le SPECS.md** → le workflow assemble tout en document cohérent

## Structure du repo

```
definus/
├── README.md                          ← Ce fichier
├── TAXONOMY.md                        ← Taxonomie complète des types de logiciels
├── WORKFLOW.md                        ← Processus de génération des specs
├── CAHIER-DES-CHARGES-SKILL.md        ← CDC de la skill Claude "Definus"
│
├── types/                             ← Fiches détaillées par type de logiciel
│   ├── 01-landing-page.md
│   ├── 02-site-vitrine.md
│   ├── 03-application-web.md
│   ├── 04-dashboard.md
│   ├── 05-application-mobile.md
│   ├── 06-api-backend.md
│   ├── 07-outil-interne.md
│   ├── 08-plateforme-saas.md
│   ├── 09-extension-navigateur.md
│   └── 10-automatisation-workflow.md
│
├── features/                          ← Bibliothèque de fonctionnalités-type
│   ├── 00-INDEX.md
│   ├── auth/
│   ├── data/
│   ├── content/
│   ├── communication/
│   ├── payment/
│   ├── admin/
│   ├── integration/
│   ├── analytics/
│   ├── ux/
│   └── security/
│
└── templates/
    └── SPECS-TEMPLATE.md
```

## Usage avec Claude

```
"Je veux spécifier [type de logiciel] pour [contexte]"
```

Claude charge Definus, pose les bonnes questions basées sur les questionnaires, et génère un SPECS.md complet prêt pour le développement.

## Écosystème Lina Finance

- **lina-codex** → Base de connaissances stratégique
- **definus** → Spécifications logicielles (ce repo)
- **lina-dev** → Skill de développement Claude Code
