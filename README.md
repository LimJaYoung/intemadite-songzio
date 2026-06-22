# SONGZIO Digital Galerie Noir

## Project URL

- Vercel production: https://vercel-songzio.vercel.app
- Vercel project: `limjayoungs-projects/vercel-songzio`

## Local Files

- Deploy folder: `F:\intermediate\vercel-songzio`
- Main HTML: `F:\intermediate\vercel-songzio\index.html`
- Original working HTML: `F:\intermediate\index.html`
- Reference note: `F:\intermediate\local\reperence.md`

## How To Open Locally

Open this file directly in a browser:

```text
F:\intermediate\vercel-songzio\index.html
```

Or run a local static server from the deploy folder:

```powershell
cd F:\intermediate\vercel-songzio
python -m http.server 8080 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:8080/index.html
```

## How To Deploy To Vercel

From the deploy folder:

```powershell
cd F:\intermediate\vercel-songzio
pnpm dlx vercel --prod --yes
```

If `pnpm` is not installed on another PC, install Node.js first, then use:

```powershell
npx vercel --prod --yes
```

You must be logged in to the Vercel account that owns:

```text
limjayoungs-projects/vercel-songzio
```

## Design Source Of Truth

This page is not a free-form redesign. It must follow the measured reference layout from:

```text
F:\intermediate\local\reperence.md
```

Keep these reference rules:

- Content width basis: `1920px`
- Container max: `1640px`
- Desktop grid: `12 columns / 20px gap`
- Mobile grid: `6 columns / 8px gap`
- Hero title: `100px / 90px / -6px`
- Mobile hero title: `50px / 44px / -3px`
- Body copy: `18px / 24px / -1.08px`
- Small CTA: `16px / 20px / -0.96px`
- Big CTA: `50px / 44px / -3px`
- Story padding: `112px 120px 120px`
- Gallery gap: `32px`
- No rounded CTA radius unless the reference is reverified
- Do not expose shopping CTA too early in the hero

## Page Structure

The current `index.html` follows this reference order:

1. Entry / black splash
2. Chapter menu
3. Intro
4. Tale Head
5. Lookbook
6. Product Overview
7. Story
8. Collection Gallery
9. Outro / contact

## Image Policy

Images are loaded from SONGZIO official sources. Do not replace them with stock images.

Current image types:

- Runway / look images
- Collection campaign images
- Full-width archive/gallery images

When changing images, preserve the reference ratios:

- Hero cover: `1920 / 1600`
- Mobile cover: `1080 / 1920`
- Portrait look: `1610 / 2148`
- Side portrait: `500 / 698`
- Outro/archive portrait: `934 / 1204`

## Editing Rule

Edit this file for deployment:

```text
F:\intermediate\vercel-songzio\index.html
```

If you edit the original working file instead:

```text
F:\intermediate\index.html
```

copy it back into the deploy folder before redeploying:

```powershell
Copy-Item -LiteralPath "F:\intermediate\index.html" -Destination "F:\intermediate\vercel-songzio\index.html" -Force
```

## Verification Checklist

Before redeploying, check:

- The page opens locally.
- SONGZIO images load.
- First viewport remains black/gallery-like.
- Top and bottom navigation remain fixed.
- Text does not overlap at 1920px desktop.
- Mobile keeps the large type readable.
- Layout still follows the reference values, not a new arbitrary layout.
