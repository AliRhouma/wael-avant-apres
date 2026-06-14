# Wael Design System — Avant / Après

A static showcase page comparing original scanned school documents ("Avant") with
their rebuilt **WaelDocuments** theme versions ("Après"). One of the "Après" panes
embeds a live, scrollable A4 document via an `<iframe>`.

## Structure

```
.
├── index.html              # the showcase / comparison page
└── docs/
    └── devoir_synthese_1.html   # embedded document (loaded in card 01's "Après" pane)
```

All fonts and MathJax are loaded from CDNs, so there are no build steps and no
local dependencies.

## Run locally

It's pure static HTML — just open `index.html` in a browser, **or** serve the
folder (recommended, so the iframe loads without `file://` restrictions):

```bash
# any of these from the project root
npx serve .
# or
python -m http.server 8000
```

Then visit http://localhost:8000 (or the port shown).

## Deploy to Vercel

This is a zero-config static site.

1. Push to GitHub (see below).
2. Go to https://vercel.com/new, import the repo.
3. Framework preset: **Other** · Build command: *(none)* · Output directory: `./`
4. Deploy. Every push to `main` redeploys automatically.

## Add the remaining images

Cards 02–04 (and the "Avant" pane of card 01) use `<img src="">` placeholders.
Drop image URLs/paths into those `src=""` attributes. Put local images in an
`assets/` folder and reference them as `assets/your-image.png`.
