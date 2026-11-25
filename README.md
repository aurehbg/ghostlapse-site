# Booflip website

The public pages for the App Store: a home page, the privacy policy and the terms of use.
Plain HTML and CSS, no build step. Styled with the app's tokens (see `../DESIGN.md`) and its bundled Bricolage Grotesque font.

```
index.html          Home, links to both pages
privacy/index.html  Privacy policy (mirrors ../PRIVACY.md; change both together)
terms/index.html    Terms of use
style.css           Shared styles
fonts/, ghost.png   Copied from Ghostlapse/Resources/Fonts and the GhostMark asset
```

## Publishing on GitHub Pages

The app repo is private, so the site is published from a separate public repo, `booflip-site`:

1. Copy the contents of this folder (including `.nojekyll`) to the root of that repo and push to `main`.
2. In that repo: **Settings → Pages → Build and deployment → Deploy from a branch**, branch `main`, folder `/ (root)`.
3. The pages are then at `https://aurehbg.github.io/booflip-site/privacy/` and `…/terms/`.

Put those two URLs in App Store Connect (Privacy Policy URL, and the EULA / Terms of Use link in the app description) and on the paywall.

## Keeping it current

- When the policy changes, update the "Last updated" date on the page.

To preview locally: `python3 -m http.server -d site 8000`, then open http://localhost:8000.
