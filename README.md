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

N'importe quel hébergement statique convient. Déposer le dossier tel quel, aucune
commande de construction, aucun répertoire de sortie.

Après le déploiement, remplacer `REMPLACER.ht` dans les balises `canonical` et Open Graph
par le domaine réel.

## Modifier

Tout est dans `index.html`. Les couleurs et les polices passent par les variables CSS
déclarées dans `:root`. Le thème sombre est géré par `prefers-color-scheme` et par un
attribut `data-theme` sur l'élément racine.

Le formulaire de candidature est inerte : il valide et affiche un accusé de réception,
sans rien transmettre. Voir `CLAUDE.md` pour ce qu'il reste à brancher.
