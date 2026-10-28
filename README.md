# Website Studies

Eight independent typography case studies with homepage screenshots, measured CSS samples, and practical learning exercises.

Published with GitHub Pages from `main` using `.github/workflows/deploy-pages.yml`. Root source files are copied into a static deployment artifact. Open `index.html` through a static server for local preview, for example `python3 -m http.server 8000`. No dependencies or build step are required.

## Files

- `data.js`: study records.
- `app.js`: card filters and native study dialogs.
- `style.css`: responsive gallery and header.
- `assets/`: homepage reference captures.
- `TYPOGRAPHY_REVIEW_PROCESS.md`: repeatable review and publication workflow.

Learning framework: https://github.com/Pythonidaer/typography-learning. Studies are independent observations, not official brand guidelines.

Deployment: the Pages workflow runs for changes on `main` and can also be started manually from Actions.

## Observation baseline

The first eight studies are homepage observations recorded on October 27, 2026 (America/New_York). The browser used a 1363 × 936 CSS-pixel viewport; typography tables describe that single desktop snapshot. This was the available browser viewport, not a chosen design breakpoint, a device standard, or evidence that the source websites target 1363px.

Existing source-website typography measurements do not establish mobile or tablet behavior. Later checks of this gallery’s own mobile layout are separate from responsive audits of the websites being studied. Keep observation metadata in repository documentation rather than the public page introduction or study-panel status text.

## To do: broader and responsive typography reviews

- Define a small, repeatable page sample per website: homepage, one content-heavy page, and one relevant product, service, or listing page when available. Select by typography roles rather than inspecting every page.
- Agree on consistent representative viewport widths, for example 390px (mobile), 768px (tablet), and 1440px (desktop). Treat these as test widths, not universal device breakpoints.
- Check a small amount of resizing or the declared CSS around visible layout/type changes. Capture an extra width only when it reveals a meaningful transition; do not audit every possible screen width.
- Record per-page and per-width font family, size, weight, line height, tracking, text width, and wrapping. Distinguish fixed values, fluid scaling, and breakpoint changes only when supported by evidence.
- Decide how responsive comparisons should appear in study panels and how to store their evidence before extending the current study schema. Retain the original desktop snapshot as a dated baseline.
- Review time cost and browser capabilities, then update TYPOGRAPHY_REVIEW_PROCESS.md with an approved workflow. Representative browser widths do not replace real-device checks or a full accessibility audit.

These are follow-up tasks, not completed observations or newly implemented responsive studies.
