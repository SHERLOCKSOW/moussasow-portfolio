# Portfolio — Moussa Sow

Portfolio professionnel statique (HTML/CSS/JS pur, aucune dépendance, aucun build requis).

## Lancer en local

Ouvrir simplement `index.html` dans un navigateur (double-clic), ou :

```bash
open index.html        # macOS
xdg-open index.html    # Linux
```

## Déploiement — GitHub Pages

1. Créer un repository GitHub public (ex: `moussasow-portfolio`)
2. Pousser ce projet :
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/SHERLOCKSOW/moussasow-portfolio.git
   git branch -M main
   git push -u origin main
   ```
3. Dans le repo GitHub : Settings → Pages → Source = branch `main`, dossier `/ (root)`
4. Custom domain : `moussasow.pro` (le fichier `CNAME` est déjà inclus dans ce projet)
5. Configurer les DNS chez Spaceship (A records vers GitHub Pages + CNAME pour www)
6. Cocher "Enforce HTTPS" une fois le DNS propagé

## Structure

```
moussasow-portfolio/
├── index.html      # Tout le site : HTML + CSS + JS + photo + badges + CV (encodés en base64)
├── CNAME           # Domaine custom pour GitHub Pages : moussasow.pro
├── .gitignore
└── README.md
```

## Mettre à jour le site après déploiement

```bash
# modifier index.html
git add .
git commit -m "Description du changement"
git push
```

Le site se met à jour automatiquement en 1-2 minutes, sans étape de build.

## Notes

- Aucun secret, token ou clé API n'est présent dans ce projet.
- Le formulaire de contact utilise FormSubmit.co (sow49986@gmail.com) — la première soumission nécessite de cliquer sur un email de confirmation pour l'activer.
- Aucune meta description / Open Graph / favicon n'est encore configuré — recommandé avant partage public large.
