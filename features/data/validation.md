# Validation des données

## Définition
Ensemble de règles qui vérifient que les données saisies ou reçues sont correctes, complètes et cohérentes avant d'être stockées.

## Sous-features

- [ ] Validation côté client (frontend, temps réel)
- [ ] Validation côté serveur (API)
- [ ] Types de validation : obligatoire, format, longueur, plage, regex, unicité
- [ ] Messages d'erreur contextuels et clairs
- [ ] Validation cross-champs (ex: date fin > date début)
- [ ] Validation asynchrone (vérifier en base : email déjà utilisé ?)
- [ ] Sanitization (nettoyage des entrées : trim, escape HTML)

## Questionnaire de cadrage

1. Quels champs ont des règles de validation ? Lister champ + règle.
2. La validation doit-elle être en temps réel (au blur/keyup) ou à la soumission ?
3. Y a-t-il des validations cross-champs ? (ex: mot de passe et confirmation identiques)
4. Faut-il des validations asynchrones ? (vérifier l'unicité d'un email en base)
5. Comment afficher les erreurs ? (sous le champ, en toast, en bandeau)
6. Les messages d'erreur sont-ils génériques ou personnalisés par champ ?
7. Faut-il de la sanitization ? (trim espaces, échapper HTML, prévenir XSS)
8. Côté API, les erreurs de validation retournent-elles un format structuré ? (champ + message)
