# Workflow Definus — Génération intelligente de spécifications

## Principe

Definus transforme une idée vague en spécifications complètes en **4 phases** de 5-15 minutes chacune. Chaque phase pose des questions ciblées basées sur la bibliothèque de fonctionnalités.

---

## Phase 1 — Identification (2 min)

**Objectif** : Comprendre ce qu'on construit.

1. L'utilisateur décrit son projet en langage naturel
2. Claude identifie le type de logiciel via l'arbre de décision (TAXONOMY.md)
3. Si le projet combine plusieurs types, Claude les liste et propose de les spécifier séparément
4. Validation avec l'utilisateur

**Output** : Type(s) identifié(s) + contexte métier

---

## Phase 2 — Sélection des fonctionnalités (5 min)

**Objectif** : Constituer le panier de features.

1. Claude charge la fiche du type identifié (types/XX-xxx.md)
2. Il présente la liste des fonctionnalités standard avec leur priorité (Obligatoire, Recommandé, Optionnel)
3. L'utilisateur valide, ajoute ou retire des features
4. Pour les features Optionnelles, Claude demande si elles sont pertinentes
5. Si une feature custom n'est pas dans la bibliothèque, Claude la note pour la spécifier from scratch

**Output** : Liste des features retenues avec priorité

---

## Phase 3 — Cadrage détaillé (10-20 min)

**Objectif** : Répondre aux questionnaires de chaque feature.

1. Claude regroupe les questions par thème pour éviter les doublons :
   - **Bloc Utilisateurs** : auth, rôles, profils (questions mutualisées)
   - **Bloc Données** : entités, CRUD, validation, recherche
   - **Bloc UX** : navigation, responsive, loading, erreurs
   - **Bloc Communication** : notifications, emails
   - **Bloc Sécurité** : RGPD, audit, mentions légales
   - **Bloc Technique** : stack, hébergement, CI/CD
   - **Bloc Business** : paiement, facturation (si applicable)

2. Pour chaque bloc, Claude pose les questions pertinentes (issues des questionnaires des features sélectionnées)
3. Claude ne pose PAS les questions évidentes (ex: si c'est une landing page, pas de questions sur l'authentification)
4. Les réponses alimentent directement les specs

**Technique d'interview intelligente** :
- Poser max 3-5 questions par message
- Proposer des réponses par défaut quand possible (ex: "JWT avec refresh token, c'est ok ?")
- Déduire les réponses des réponses précédentes (ex: si PSFP → RGPD obligatoire, pas besoin de demander)
- Reformuler pour valider avant de passer au bloc suivant

**Output** : Réponses complètes à tous les questionnaires pertinents

---

## Phase 4 — Génération du SPECS.md (3 min)

**Objectif** : Assembler un document de spécifications complet et structuré.

1. Claude utilise le template (templates/SPECS-TEMPLATE.md)
2. Il remplit chaque section avec les réponses collectées
3. Il ajoute les détails techniques inférés (stack, architecture, modèle de données)
4. Il produit le fichier SPECS.md final

**Output** : SPECS.md complet, prêt pour le développement

---

## Règles d'intelligence

### Déduction automatique
Claude déduit certaines réponses sans demander :

| Si... | Alors... |
|-------|---------|
| Type = Landing Page | Pas d'auth, pas de BDD, statique |
| Contexte = PSFP/finance | RGPD obligatoire, audit trail, KYC |
| Stack = Next.js + Supabase | Auth Supabase, PostgreSQL, Row Level Security |
| Mobile = React Native | Push via FCM, navigation React Navigation |
| Budget = MVP | Features Obligatoires uniquement, pas d'Optionnelles |

### Priorisation des questions
1. Questions de cadrage global en premier (qui, quoi, pourquoi)
2. Questions métier ensuite (entités, workflows)
3. Questions techniques en dernier (stack, hébergement)
4. Ne jamais demander un détail technique si le cadrage métier n'est pas clair

### Gestion de l'incertitude
Si l'utilisateur ne sait pas :
- Proposer le pattern le plus courant comme défaut
- Marquer la décision comme "à confirmer" dans les specs
- Ne pas bloquer le workflow pour une question secondaire

---

## Intégration avec l'écosystème Lina

### Avec lina-dev
Le SPECS.md généré par Definus est directement consommable par la skill lina-dev pour lancer le développement avec Claude Code :
```
Definus (specs) → lina-dev (CLAUDE.md + code) → GitHub → Déploiement
```

### Avec lina-codex
Les décisions architecturales majeures prises pendant le cadrage peuvent être enregistrées dans le Lina Codex si elles ont une valeur stratégique.

### Avec skill-creator
Si le projet spécifié est une skill Claude, Definus peut générer un cahier des charges compatible avec skill-creator.
