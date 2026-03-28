# Formulaires

## Définition
Interfaces de saisie de données par l'utilisateur. Du formulaire de contact simple au formulaire multi-étapes complexe avec validation en temps réel.

## Sous-features

- [ ] Champs texte (input, textarea)
- [ ] Champs numériques
- [ ] Sélecteurs (dropdown, radio, checkbox)
- [ ] Date picker / time picker
- [ ] Upload de fichiers dans le formulaire
- [ ] Champs conditionnels (afficher/masquer selon les réponses)
- [ ] Formulaire multi-étapes (wizard/stepper)
- [ ] Validation en temps réel (côté client)
- [ ] Validation côté serveur
- [ ] Messages d'erreur contextuels
- [ ] Auto-save (brouillon)
- [ ] Pré-remplissage intelligent
- [ ] Formulaire dynamique (champs générés depuis une config)
- [ ] Accessibilité (labels, aria, focus management)
- [ ] Anti-spam (honeypot, captcha)

## Questionnaire de cadrage

### Structure
1. Combien de formulaires différents dans l'application ? Lister chacun.
2. Pour chaque formulaire, combien de champs approximativement ?
3. Y a-t-il des formulaires multi-étapes ? Combien d'étapes ?
4. Certains champs sont-ils conditionnels (apparaissent selon d'autres réponses) ?

### Champs et validation
5. Quels types de champs sont nécessaires ? (texte, nombre, date, fichier, dropdown, etc.)
6. Quelles sont les règles de validation ? (obligatoire, format email, longueur min/max, regex)
7. La validation doit-elle être en temps réel ou à la soumission ?
8. Faut-il des messages d'erreur personnalisés par champ ?

### Comportement
9. Les données doivent-elles être sauvegardées en brouillon avant soumission ?
10. Certains champs doivent-ils être pré-remplis ? (données profil, données précédentes)
11. Que se passe-t-il après la soumission ? (message de confirmation, redirection, email)
12. Où vont les données ? (base de données, email, CRM, Google Sheets, webhook)

### Anti-spam et sécurité
13. Faut-il une protection anti-spam ? (captcha, honeypot)
14. Y a-t-il des données sensibles dans le formulaire ? (données financières, santé)
15. Faut-il chiffrer certaines données avant envoi ?
