# Ascension Industries — Pants of Ascension

This repository contains a small fantasy-parody site for a DnD campaign: the official "Thank you for purchasing the Pants of Ascension!" page. It includes quick-start usage, customization tips, and lore for your players.

Site map:

- `index.html` — Thank you / quick tips
- `howto.html` — Quick start and usage rules for the DM
- `customize.html` — Tailoring, runes, and flavor options
- `lore.html` — Origin story and FAQ

Quick steps to publish:

1. Create a repository on GitHub (or push this local repo to an existing one).
2. In the repository Settings → Pages, choose the branch (e.g., `main`) and the folder (`/ (root)`) to publish.
3. Save — GitHub Pages will deploy the site and provide a URL.

Useful commands (run in repository root):

```powershell
git init
git add .
git commit -m "Add Pants of Ascension site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

Notes:

- An empty `.nojekyll` file is included to prevent GitHub Pages from ignoring files and folders that start with an underscore.
- Add a `CNAME` file with your custom domain if you want to use one.
- If you prefer Jekyll features, remove `.nojekyll` and add `_config.yml`.

Optional background image:

You can add a stock background image to give the site a more polished, marketing feel while keeping the DnD vibe. Place a background image at `assets/bg.jpg` and the CSS will pick it up. Use a CC0 / public-domain image or provide proper attribution.

Example (free, CC0-style sources):
- https://unsplash.com (check license per image)
- https://pixabay.com

To add an image:

```powershell
# from repository root
curl -L -o assets/bg.jpg "<image-url>"
git add assets/bg.jpg
git commit -m "Add marketing background"
git push
```


