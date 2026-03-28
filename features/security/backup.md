# Backup et disaster recovery

## Définition
Stratégie de sauvegarde et de restauration en cas de perte de données ou de panne majeure.

## Sous-features
- [ ] Backup automatique de la base de données
- [ ] Backup des fichiers/médias
- [ ] Point-in-time recovery
- [ ] Backup cross-région
- [ ] Test de restauration périodique
- [ ] RTO (Recovery Time Objective)
- [ ] RPO (Recovery Point Objective)
- [ ] Runbook de disaster recovery

## Questionnaire de cadrage
1. Quelle fréquence de backup ? (continue, horaire, quotidien)
2. Quelle rétention ? (7 jours, 30 jours, 1 an)
3. Faut-il du point-in-time recovery ? (restaurer à une minute précise)
4. Faut-il un backup cross-région ? (si le datacenter brûle)
5. Quel RTO acceptable ? (combien de temps pour restaurer)
6. Quel RPO acceptable ? (combien de données peut-on perdre)
7. Les backups sont-ils chiffrés ?
8. Y a-t-il un runbook documenté et testé ?
