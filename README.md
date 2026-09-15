# endorrfin.github.io

Landing page for **github.com/Endorrfin** — published at <https://endorrfin.github.io/>.

Single static `index.html`. No build step, no dependencies, no CDN, no trackers.

## Files

| File | Why |
|---|---|
| `index.html` | The whole page — inline CSS, inline SVG diagram |
| `.nojekyll` | Empty file. Tells GitHub Pages to skip Jekyll processing: faster deploys, and no risk of Jekyll mangling or hiding files |
| `README.md` | This file. Not served — `index.html` wins at the root |

## Publishing

The repository must be **public** (Pages from a private repo needs a paid plan) and named
**`endorrfin.github.io`** — all lowercase, because the username contains an uppercase letter.

Settings → Pages → Source: **Deploy from a branch** → Branch: **main** → Folder: **/ (root)** → Save.

First publish takes 1–3 minutes. After that every push to `main` republishes.

## This does not affect the guide sites

The guides are *project* sites, each published from its own repository and served at
`endorrfin.github.io/<repo>/`. This repository is the *user* site and only occupies the root `/`.
They coexist; none of the guide URLs change.

## Checks before and after pushing

- open `index.html` locally — every card link opens the right guide
- narrow the window to ~380 px — nothing overflows horizontally
- after publish, open <https://endorrfin.github.io/> in a private window (avoids the cached 404)
- click all 10 outbound links on the live page

## Updating

Adding a guide = one `<article class="card">` block copied and edited.
Keep the numbering (`01`, `02`, …) contiguous, and keep the strongest guide first —
the first three cards are the only ones most visitors read.

Soft limits worth knowing: 1 GB repo, 1 GB published site, 100 GB/month bandwidth,
10 builds/hour. This page is ~16 KB.
