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

## Comment personnaliser les titres et descriptions

Le fichier à modifier est : **`/videos/metadata.json`**

Vous n'avez **pas besoin de toucher au code HTML/JS**.

### Étapes ultra-simples (directement sur GitHub)

1. Ouvrez votre repo GitHub.
2. Allez dans le dossier **`videos`**.
3. Cliquez sur le fichier **`metadata.json`**.
4. Cliquez sur le bouton **✏️ Edit this file**.
5. Modifiez seulement les textes `title` et `description`.
6. Cliquez sur **Commit changes...**.
7. Attendez le déploiement : vos nouveaux textes apparaissent dans le portfolio.

### Captures d'écran textuelles (repères visuels)

- **Écran 1 (liste de fichiers)** : `videos/` → vous voyez `video1.mp4`, `video2.mp4`, `metadata.json`
- **Écran 2 (fichier ouvert)** : `metadata.json` affiché avec les blocs `video1`, `video2`, etc.
- **Écran 3 (édition)** : bouton ✏️ en haut à droite du fichier
- **Écran 4 (commit)** : zone "Commit changes" en bas avec message de commit

### Exemple concret à copier

```json
{
  "__instructions": {
    "note": "Modifiez seulement title et description"
  },
  "video1": {
    "title": "Mon nouveau titre",
    "description": "Ma description courte et claire"
  }
}
```

### Exemples de bons titres et descriptions

- **Cosmétique**
  - Titre : `Routine glow — Sérum Vitamine C`
  - Description : `Avant/après en 15 secondes avec focus texture et éclat du teint.`
- **Food**
  - Titre : `Burger Signature en 3 étapes`
  - Description : `Hook visuel rapide + dressage final pour déclencher l'envie.`
- **SaaS**
  - Titre : `Automatiser ses relances clients`
  - Description : `Démo orientée résultat avec CTA vers l'essai gratuit.`
- **Fitness**
  - Titre : `HIIT 20 min à la maison`
  - Description : `Routine courte, dynamique et facile à reproduire.`

## Mini-guide JSON (très important)

Le JSON est strict. Respectez ces règles :

1. **Guillemets obligatoires** autour des clés et textes.
2. **Virgules** entre les blocs, sauf après le dernier.
3. **Accolades** `{}` pour ouvrir/fermer chaque objet.
4. Gardez les clés comme `video1`, `video2`, etc. selon vos fichiers.

Exemple valide :

```json
"video3": {
  "title": "Titre ici",
  "description": "Description ici"
}
```

Exemple invalide (erreur JSON) :

```json
"video3": {
  "title": "Titre ici"
  "description": "Description ici"
}
```

👉 Il manque une virgule après `"Titre ici"`.

## Dépannage rapide

Si une vidéo ne s'affiche pas ou ne se lit pas :

1. Vérifiez le nom exact (`video7.mp4`, pas `Video7.mp4` si vous voulez suivre la convention standard)
2. Vérifiez que le fichier est bien dans `/videos/`
3. Testez une ré-export en MP4/H.264
4. Ouvrez la console navigateur pour voir le message d'erreur de chargement
5. Vérifiez que `metadata.json` est valide (guillemets, virgules, accolades)
