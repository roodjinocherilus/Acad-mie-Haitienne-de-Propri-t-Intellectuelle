# Site AHPI

Page unique, HTML statique, sans build.

```
index.html          la page complète, styles et script inclus
assets/             logos SVG et favicon
CLAUDE.md           brief de reprise, à lire avant toute modification
```

## Lancer en local

```
python3 -m http.server 8000
```

Puis ouvrir `http://localhost:8000`. Ouvrir `index.html` par double-clic fonctionne aussi,
mais le chemin relatif du favicon ne se résout pas.

## Déployer

Le site est servi par GitHub Pages depuis la branche `main`, dossier racine, sous le
domaine `www.acahpi.com` déclaré dans le fichier `CNAME`. Un push sur `main` suffit à
publier ; aucune commande de construction, aucun répertoire de sortie.

## Modifier

Tout est dans `index.html`. Les couleurs et les polices passent par les variables CSS
déclarées dans `:root`. Le thème sombre est géré par `prefers-color-scheme` et par un
attribut `data-theme` sur l'élément racine.

Le formulaire de candidature est inerte : il valide et affiche un accusé de réception,
sans rien transmettre. Voir `CLAUDE.md` pour ce qu'il reste à brancher.
