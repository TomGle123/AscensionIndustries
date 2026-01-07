# Copilot / Developer Instructions

This file summarizes the repository's HTML structure, CSS hooks, and common tasks to help future contributors (or Copilot-style agents) modify the site safely.

High-level structure
- `index.html` — Landing / "Thank you" page. Contains the primary hero, features grid, and quick tips.
- `howto.html` — Usage instructions for players/DMs.
- `customize.html` — Tailoring, rune and customization notes.
- `lore.html` — Origin story, FAQ, and care tips.
- `assets/styles.css` — Central stylesheet. Contains corporate + fantasy theming, hero full-bleed helpers, title/tab bar, and button styles.
- `assets/logo.svg` — Small SVG logo used in the header.
- `.nojekyll` — Prevent Jekyll processing on GitHub Pages.

Header / navigation
- Each page uses the same header pattern:
  - `<header class="site-header">` containing a `.container`.
  - Left area: `<div class="brand">` with the logo and two text lines: `.title` and `.tagline`.
  - Right/left tabs: `<div class="titlebar"><div class="tabs">` containing `<a>` links. Active tab has class `active`.

Hero
- The hero block uses `section.hero` and pages that should be full-bleed use `section.hero.hero-fullbleed` with an inner `.container` to center content.
- To enable the parchment background, add `assets/parchment.jpg`. The CSS uses the `@supports` check to apply it when present.

CSS hooks and conventions
- `.hero-fullbleed` — makes the hero span the viewport width. Keep hero content inside an inner `.container`.
- `.titlebar .tabs a` — the tab elements; add `active` to indicate the current page.
- `.btn`, `.cta`, `.btn-back` — standardized button styles.
- `.features` — grid of feature cards.

Adding pages
- Follow the same header pattern in new pages for consistent navigation.
- Add any hero content inside `section.hero.hero-fullbleed` followed by other sections inside the page `.container`.

Assets and images
- Place images in `assets/` and reference them relative to the HTML files (e.g., `assets/parchment.jpg` or `assets/logo.svg`).
- Keep images reasonably sized (hero backgrounds: 1600px+ width recommended).

Common tasks
- Change active tab: add `class="active"` to the corresponding `<a>` in `.tabs`.
- Update tagline length: if you want different truncation, modify `.tagline` max-width in `assets/styles.css`.
- Add a new section under the main `.container` for more information; use the existing `.features` card pattern for consistency.

Developer notes
- The layout uses CSS flexbox and a small amount of layout math to make the hero full-bleed while keeping content centered.
- On small screens the header stacks (brand on top, tabs beneath) — this behavior is controlled by the final `@media (max-width:800px)` block.
- Avoid changing the hero HTML structure unless you also update `.hero-fullbleed > .container` rules.

If you'd like, I can also add:
- A small build step or an automated GitHub Action that validates HTML/CSS or deploys to `gh-pages`.
- An example `assets/parchment.jpg` (I can fetch a public-domain texture and add it).
