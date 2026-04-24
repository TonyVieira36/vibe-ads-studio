# Vibe Ads Studio

Portfolio statique prêt pour GitHub Pages.

## Modifier les vidéos du carrousel

Ouvrez `index.html` puis éditez le tableau `portfolioVideos` dans le script en bas de page.

Formats supportés :

- `type: "youtube"` + URL YouTube
- `type: "vimeo"` + URL Vimeo
- `type: "file"` + chemin local (ex: `./videos/demo.mp4`)
- `type: "empty"` pour un emplacement vide

Exemple :

```js
{
  title: "UGC Démo",
  category: "UGC",
  description: "Mon premier cas client.",
  type: "youtube",
  src: "https://www.youtube.com/watch?v=XXXXXXXXXXX"
}
```

## Déploiement

Ce dépôt est conçu pour être publié via GitHub Pages (branche `main`, dossier `/root`).
