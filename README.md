# pitchpilot-site

Marketing site for the **PitchPilot** Chrome extension.

- Landing page, pricing, and feature overview: `index.html`
- Legal: `privacy.html`, `terms.html`, `refund.html`

Hosted via GitHub Pages from the `main` branch.

## Editing

All pages are static HTML with inline CSS. Edit, commit, push — Pages
redeploys automatically within a minute or two.

## Links to keep updated

If the Chrome Web Store listing URL changes, update the three
occurrences in `index.html`:

```
https://chromewebstore.google.com/detail/pitchpilot/mjclkechmmbnlagclaphacbkkccaaoao
```

If the LemonSqueezy checkout URL changes, update the two
occurrences (hero + pricing).

## Media

Images and the demo video live in `assets/` (web-optimized). Raw source
files go in `media/`, which is git-ignored — re-export from there with
`cwebp` / `ffmpeg` when screenshots change.

## Black Friday 2026 (temporary — revert after the sale)

Sale: 20% off Pro with LemonSqueezy discount code `BF20` ($19 → $15.20).

- **Auto-expiry:** the promo hides itself on Dec 1, 2026 00:00 PT
  (`Date.parse(...)` in the `<head>` of `index.html`) and the page falls back
  to regular pricing. Change that date to extend or end the sale early.
- **What's temporary:** everything between `<!-- BLACK FRIDAY -->` and
  `<!-- /BLACK FRIDAY -->` in `index.html`, the `bf-off` classes on the
  regular-price elements, and the whole `assets/bf/` folder.
- **Clean revert:** the promo is a single commit — "Add Black Friday 2026
  promo" — so `git revert <that commit>` removes it (the git tag
  `black-friday-2026` points at it). The reel and Free/Pro cards added
  alongside it are permanent and stay.

## Backlog

- [ ] **Google Search Console** (optional, skipped for now). Add a URL-prefix
  property for `https://yuvallasristudio.github.io/pitchpilot-site/`, verify
  with the HTML file method (put Google's `google….html` file in the repo
  root, not `assets/`, and keep it there), submit `sitemap.xml`, then use URL
  Inspection > Request indexing on the homepage. Search data only starts from
  the day the property is added.
