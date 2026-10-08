# gatshub.github.io

Site personnel de Cyril L. — statique, écrit à la main, sans dépendance.
Servi par GitHub Pages à l'adresse <https://gatshub.github.io/>.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | Accueil : édito, aperçu des projets, lien vers la Sablaise |
| `projets.html` | Portefeuille de projets (hex-tui, sudoku-tui, sudoku-mignon) |
| `sablaise.html` | Étude de cas « Le Panier de la Sablaise » |
| `404.html` | Page d'erreur, à la charte, avec retour à l'accueil |
| `assets/style.css` | Feuille de style unique (palette + typographie système) |
| `.nojekyll` | Demande à GitHub Pages de servir les fichiers tels quels |

## Comment publier

Le dépôt s'appelle `<compte>.github.io` : **tout ce qui est poussé sur la branche
`main` devient le site**. Il n'y a ni build ni étape de déploiement.

```sh
# 1. prévisualiser en local
python3 -m http.server 8080        # puis http://localhost:8080/

# 2. publier
git add -A
git commit -m "…"
git push origin main
```

Le site est en ligne une minute plus tard environ. L'état de la publication se lit
dans `Settings → Pages` du dépôt, ou via `gh api repos/Gatshub/gatshub.github.io/pages`.

## Conventions

- **Aucune dépendance** : pas de framework, pas de police téléchargée, pas de CDN,
  pas de JavaScript, pas de traceur.
- **Polices système** uniquement (serif pour les titres, sans pour le corps,
  monospace pour les étiquettes).
- Deux règles de la palette, apprises à l'usage : l'ocre `#8C6A3F` porte les liens,
  mais **jamais** de teinte claire pour du texte qui doit être lu — le contraste
  prime sur l'effet.
- Le fichier `.nojekyll` est **nécessaire** : sans lui, Pages traiterait le dépôt
  comme un site Jekyll et transformerait le HTML écrit à la main.
