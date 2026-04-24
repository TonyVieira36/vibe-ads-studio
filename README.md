# Vibe Ads Studio

Portfolio statique prêt pour GitHub Pages, configuré pour lire vos vidéos **MP4 locales** depuis le dossier `videos/`.

## Structure recommandée

```text
vibe-ads-studio/
├── index.html
├── README.md
├── .gitattributes
└── videos/
    ├── video1.mp4
    ├── video2.mp4
    ├── video3.mp4
    └── ...
```

## Ajouter vos vidéos MP4 (méthode simple)

1. Ouvrez le dossier `videos/` du repo.
2. Déposez vos fichiers `.mp4` (ex: `video1.mp4`, `video2.mp4`, `video3.mp4`).
3. Si besoin, renommez vos fichiers pour garder un nom clair et stable.
4. Vérifiez dans `index.html` (tableau `portfolioVideos`) que chaque `src` pointe vers le bon chemin, par exemple:

```js
{ type: "local", src: "videos/video1.mp4" }
```

## Convention de nommage conseillée

Utilisez des noms simples, sans espace, en minuscules:

- `video1.mp4`
- `video2.mp4`
- `ugc-demo-1.mp4`
- `product-review-2.mp4`

## Taille de fichiers GitHub (important)

- GitHub bloque les fichiers **> 100 MB**.
- Recommandation: gardez chaque vidéo **< 100 MB** (idéalement 20–80 MB pour un chargement plus rapide).
- Si vos fichiers sont trop lourds, compressez-les avant upload (H.264 + AAC, 1080p max).

## `.gitattributes`

Le repo inclut `.gitattributes` pour traiter les MP4 comme des fichiers binaires:

```gitattributes
videos/*.mp4 binary
```

## Modifier les slides du carrousel

Éditez `portfolioVideos` dans `index.html` (script en bas de page). Par défaut, les 8 slides pointent déjà vers:

- `videos/video1.mp4`
- `videos/video2.mp4`
- ...
- `videos/video8.mp4`

Si vous changez un nom de fichier, mettez à jour le `src` correspondant.

## Déploiement

Ce dépôt est conçu pour être publié via GitHub Pages (branche `main`, dossier `/root`).
