# Dossier vidéos

Déposez vos vidéos dans ce dossier avec un nom **indexé** :

- `video1.mp4`
- `video2.mp4`
- `video3.mp4`
- ...

Le site détecte automatiquement les fichiers présents et les affiche dans la section Portfolio.

## Formats supportés

Le lecteur HTML5 du site tente de charger, pour chaque index (`video1`, `video2`, etc.), les extensions suivantes :

- `.mp4` (recommandé)
- `.webm`
- `.mov`

> ✅ Recommandation forte : utilisez `videoX.mp4` en H.264 pour une compatibilité maximale navigateur.

## Conseils qualité/performance

- Format recommandé : `1080x1920` (9:16)
- Codec recommandé : H.264 (MP4)
- Taille conseillée : `< 100 MB` par vidéo (plus rapide à charger)
- Évitez les espaces et caractères spéciaux dans les noms de fichiers
- Préférez les extensions en minuscules (`.mp4`) pour éviter les confusions

## Dépannage rapide

Si une vidéo ne s'affiche pas ou ne se lit pas :

1. Vérifiez le nom exact (`video7.mp4`, pas `Video7.mp4` si vous voulez suivre la convention standard)
2. Vérifiez que le fichier est bien dans `/videos/`
3. Testez une ré-export en MP4/H.264
4. Ouvrez la console navigateur pour voir le message d'erreur de chargement
