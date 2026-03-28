# Workflow d'approbation

## Définition
Processus en étapes où un élément passe par différents statuts avec validation humaine à chaque étape. Essentiel pour les outils réglementés et les processus métier structurés.

## Sous-features

- [ ] Définition des étapes du workflow
- [ ] Transition entre statuts (avec conditions)
- [ ] Attribution d'un approbateur par étape
- [ ] Notifications aux approbateurs
- [ ] Commentaires/notes à chaque étape
- [ ] Rejet avec motif obligatoire
- [ ] Retour en arrière (renvoyer à l'étape précédente)
- [ ] Escalade automatique (si pas de réponse en N jours)
- [ ] Historique complet du workflow (qui, quand, quoi)
- [ ] Délais / SLA par étape
- [ ] Workflow parallèle (plusieurs approbations simultanées)
- [ ] Signature électronique à certaines étapes

## Questionnaire de cadrage

1. Quels éléments passent par un workflow d'approbation ? (dossiers, projets, transactions, documents)
2. Quelles sont les étapes du workflow ? Dessiner le flux (ex: brouillon → soumis → en review → approuvé/rejeté).
3. Qui approuve à chaque étape ? (un rôle spécifique, le manager, un comité)
4. Faut-il que toutes les approbations soient séquentielles ou certaines peuvent être parallèles ?
5. Que se passe-t-il en cas de rejet ? (retour au début, retour à l'étape précédente, fin)
6. Le rejet nécessite-t-il un motif obligatoire ?
7. Y a-t-il des délais maximum par étape ? Que se passe-t-il si dépassé ? (escalade, notification)
8. Faut-il des notifications à chaque changement de statut ? À qui ?
9. Faut-il un historique complet avec audit trail ?
10. Faut-il une signature électronique à certaines étapes ?
11. Le workflow est-il fixe ou configurable par un admin ?
12. Y a-t-il des conditions automatiques ? (ex: montant > 100K → validation directeur obligatoire)

## Exemple Lina

Workflow dossier PSFP : Soumission porteur de projet → Analyse financière (équipe) → Validation Sharia Board → Approbation comité d'investissement → Publication campagne. Rejet possible à chaque étape avec motif.
