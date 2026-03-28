# Upload de fichiers

## Définition
Permettre aux utilisateurs de téléverser des fichiers (documents, images, vidéos) dans l'application.

## Sous-features

- [ ] Upload simple (clic ou drag-and-drop)
- [ ] Upload multiple
- [ ] Preview avant upload (images, PDF)
- [ ] Barre de progression
- [ ] Validation de type de fichier (extensions autorisées)
- [ ] Validation de taille maximale
- [ ] Compression d'images automatique
- [ ] Redimensionnement d'images
- [ ] Génération de thumbnails
- [ ] Upload direct vers cloud (S3, R2, Supabase Storage)
- [ ] Upload signé (presigned URLs)
- [ ] Scan antivirus
- [ ] Gestion des fichiers uploadés (lister, supprimer, remplacer)

## Questionnaire de cadrage

1. Quels types de fichiers sont acceptés ? (images, PDF, Word, Excel, vidéo, audio)
2. Quelle est la taille maximale par fichier ? Par upload total ?
3. Faut-il du drag-and-drop ?
4. Faut-il un upload multiple (plusieurs fichiers à la fois) ?
5. Faut-il une preview du fichier avant ou après upload ? (image, PDF)
6. Faut-il une barre de progression ?
7. Les images doivent-elles être compressées ou redimensionnées automatiquement ?
8. Où sont stockés les fichiers ? (Supabase Storage, S3, R2, serveur local)
9. Faut-il des presigned URLs pour l'upload direct vers le cloud ?
10. Faut-il un scan antivirus sur les fichiers uploadés ?
11. L'utilisateur peut-il gérer ses fichiers après upload ? (lister, supprimer, remplacer)
12. Les fichiers sont-ils publics ou privés ? (URL signée pour accès temporaire)
