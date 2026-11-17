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
