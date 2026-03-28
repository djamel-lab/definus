# SPECS.md — [Nom du projet]

> Spécifications générées par Definus le [DATE]

## 1. Vue d'ensemble

### 1.1 Description
[Description en 2-3 phrases du projet, son objectif et son contexte]

### 1.2 Type de logiciel
[Type Definus : Landing Page / App Web / Dashboard / etc.]

### 1.3 Utilisateurs cibles
[Qui utilise ce logiciel, personas, volume estimé]

### 1.4 Objectifs business
[Pourquoi ce logiciel existe, quels KPIs il sert]

---

## 2. Stack technique

| Composant | Technologie | Justification |
|-----------|-------------|---------------|
| Frontend | [React/Next.js/HTML...] | [Pourquoi] |
| Backend | [API/Supabase/Workers...] | [Pourquoi] |
| Base de données | [PostgreSQL/MongoDB...] | [Pourquoi] |
| Auth | [Supabase Auth/Auth0...] | [Pourquoi] |
| Hébergement | [Vercel/Cloudflare/AWS...] | [Pourquoi] |
| Email | [Resend/SendGrid...] | [Pourquoi] |
| Paiement | [Stripe/Mangopay...] | [Si applicable] |
| Monitoring | [Sentry/...] | [Si applicable] |

---

## 3. Modèle de données

### 3.1 Entités principales

[Pour chaque entité :]

#### [Nom de l'entité]
| Champ | Type | Obligatoire | Description |
|-------|------|-------------|-------------|
| id | uuid | oui | Identifiant unique |
| ... | ... | ... | ... |

### 3.2 Relations
[Diagramme ou description des relations entre entités]

---

## 4. Pages et navigation

### 4.1 Arborescence des pages
```
/                          → Page d'accueil
/login                     → Connexion
/register                  → Inscription
/dashboard                 → Dashboard utilisateur
/...                       → ...
```

### 4.2 Navigation
[Description du système de navigation : header, sidebar, footer]

---

## 5. Fonctionnalités détaillées

[Pour chaque fonctionnalité retenue :]

### 5.X [Nom de la fonctionnalité]

**Priorité** : Obligatoire / Recommandé / Optionnel

**Description** : [Ce que fait cette fonctionnalité]

**Règles métier** :
- [Règle 1]
- [Règle 2]

**Parcours utilisateur** :
1. [Étape 1]
2. [Étape 2]
3. [Étape 3]

**Critères d'acceptation** :
- [ ] [Critère 1]
- [ ] [Critère 2]

---

## 6. Design et UX

### 6.1 Charte graphique
| Élément | Valeur |
|---------|--------|
| Police | [IBM Plex Sans / Inter / ...] |
| Couleur primaire | [#hex] |
| Couleur secondaire | [#hex] |
| Couleur accent | [#hex] |
| Border radius | [8px / ...] |

### 6.2 Responsive
[Breakpoints et comportement par taille d'écran]

### 6.3 Maquettes
[Lien Figma ou description des écrans clés]

---

## 7. Sécurité et conformité

### 7.1 Authentification
[Méthode d'auth, politique de mot de passe, 2FA]

### 7.2 RGPD
[Données collectées, base légale, droits utilisateurs]

### 7.3 Réglementation spécifique
[PSFP, PCI-DSS, etc. si applicable]

### 7.4 Audit trail
[Quelles actions sont loguées, rétention]

---

## 8. Intégrations externes

| Service | Usage | API/SDK |
|---------|-------|---------|
| [Service 1] | [Ce qu'il fait] | [Lien doc] |
| ... | ... | ... |

---

## 9. Infrastructure et déploiement

### 9.1 Environnements
| Environnement | URL | Usage |
|--------------|-----|-------|
| Dev | localhost | Développement local |
| Staging | staging.xxx.com | Tests |
| Production | xxx.com | Live |

### 9.2 CI/CD
[Pipeline de déploiement]

### 9.3 Monitoring
[Outils et alertes]

---

## 10. Roadmap

### MVP (v1)
- [ ] [Feature 1]
- [ ] [Feature 2]
- [ ] [Feature 3]

### V2 (post-lancement)
- [ ] [Feature 4]
- [ ] [Feature 5]

### V3 (vision)
- [ ] [Feature 6]

---

## 11. Questions ouvertes

[Décisions encore à prendre, à confirmer avec l'équipe]

| Question | Options | Décision | Date |
|----------|---------|----------|------|
| [Question 1] | [A ou B] | À confirmer | — |
| ... | ... | ... | ... |
