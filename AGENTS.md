# Black in Business Interactives

## Project overview

This repository is a static, front-end-only GitHub Pages site for One Million Black Women: Black in Business. The root `index.html` is the branded module directory. Each learning module is a self-contained HTML file with its own styles and scripts.

There is no package manager, build step, framework, or server-side component.

## Current status (2026-09-08)

- Default branch: `main`
- Public repository: `https://github.com/sternlsl/bib-interactives`
- GitHub Pages site: `https://sternlsl.github.io/bib-interactives/`
- Ownership was transferred from `HughMackey-LSL` to the `sternlsl` GitHub organization on 2026-09-08.
- The local `origin` points to `https://github.com/sternlsl/bib-interactives.git`.
- GitHub reports the organization-owned Pages deployment as built from the root of `main`.

Recent milestones:

- `d2d7256` - Created the branded module index and initialized GitHub Pages.
- `15d11c8` - Made the landing page more compact and added Inter.

## Repository contents

- `index.html` - Editable landing page and module directory.
- `.nojekyll` - Ensures GitHub Pages serves the static files directly.
- `README.md` - Short repository overview.
- `1 - coffee cart financial statements simulator.html`
- `2 - ms yeo design studio simulator.html`
- `3 - projecting P&L.html`
- `4 - working capital management.html`

## Preserve the learning modules

The four numbered HTML modules are approved, self-contained deliverables. Do not edit, rename, move, reformat, or regenerate them unless the user explicitly requests a module-level change. Landing-page work should normally be confined to `index.html` and repository documentation.

Known SHA-256 checksums:

```text
cb4e3157b23f6132d48984c012babb18064e1a64451810c80b5475caab092b8a  1 - coffee cart financial statements simulator.html
2f82be70c8d1420e3bb1e761148908567bfa80d5bf0ec38c9765a2cf31067bea  2 - ms yeo design studio simulator.html
6d5cd235b5c1630c4898c1402e5ace35417ea8da44bed2e86d6ff79b95f97077  3 - projecting P&L.html
43dc91f8d9c4dbdd7d518c2739d7436c0af68a7a4db54b6b842b7977e242efc5  4 - working capital management.html
```

Recheck these hashes after any landing-page or repository-maintenance work.

## Landing-page design

The visual direction comes from the 2021 One Million Black Women brand guidelines; the source PDF is reference material and is not committed to this repository.

- Brand colors: white `#FFFFFF`, off-white `#F8F8F5`, sky blue `#9BEEEB`, magenta `#98004D`, coral `#FA6059`, emerald `#004E29`, Naples yellow `#FFB133`, and black `#000000`.
- Use black or white typography on brand-color surfaces; do not introduce gradients.
- Body and interface copy use Inter from Google Fonts, with Arial/Helvetica fallbacks.
- Primary display headlines and module numbers use League Gothic from Google Fonts, with Arial Narrow/condensed fallbacks. Longer module titles use Inter 800 in sentence case, following the secondary-headline hierarchy.
- The desktop module directory is a four-across grid. Narrow tablets use two columns. Mobile uses compact single-column rows with two-line descriptions to limit scrolling.
- Keep the page accessible: semantic headings, full-card links, visible keyboard focus, readable type, reduced-motion support, and the skip link should remain intact.

## Local preview and validation

Serve the repository root with a basic static server, for example:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Before publishing:

1. Confirm `index.html` loads successfully and all four module links resolve.
2. Run `git diff --check`.
3. Recalculate the four module checksums and compare them with the values above.
4. Confirm the Google Fonts stylesheet for Inter and League Gothic remains reachable, while retaining the local font fallbacks.

## Publishing

GitHub Pages publishes directly from the repository root on the `main` branch using the legacy branch-based Pages build. No generated output or deployment workflow is required. Push only validated source files, then wait for the Pages status to report `built` before treating the update as live.
