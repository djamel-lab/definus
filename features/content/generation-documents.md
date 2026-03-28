# Génération de documents

## Définition
Produire automatiquement des documents formatés (PDF, Word, Excel) à partir des données de l'application. Rapports, factures, contrats, attestations.

## Sous-features

- [ ] Génération de PDF
- [ ] Génération de Word (.docx)
- [ ] Génération d'Excel (.xlsx)
- [ ] Templates de documents personnalisables
- [ ] Variables dynamiques dans les templates
- [ ] En-tête / pied de page avec logo
- [ ] Signature électronique intégrée
- [ ] QR code / code-barres dans le document
- [ ] Génération en masse (batch)
- [ ] Historique des documents générés
- [ ] Envoi automatique par email après génération

## Questionnaire de cadrage

1. Quels types de documents doivent être générés ? (facture, contrat, rapport, attestation, relevé)
2. Quel format de sortie ? (PDF, Word, Excel, les trois)
3. Y a-t-il un modèle/template existant à reproduire ?
4. Quelles données dynamiques sont injectées ? (nom, montant, date, tableaux)
5. Faut-il un en-tête/pied de page avec le logo de l'entreprise ?
6. Faut-il une signature électronique ?
7. Faut-il un QR code ou code-barres ? Quel contenu encode-t-il ?
8. Faut-il générer en masse ? (ex: toutes les factures du mois)
9. Le document doit-il être envoyé automatiquement par email ?
10. Faut-il stocker un historique des documents générés ?
11. Qui peut générer quels documents ? (permissions par rôle)
12. Y a-t-il des contraintes légales sur le format ? (facture, reporting AMF)
