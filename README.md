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

## Expanded review protocol and remaining work

The [review process](TYPOGRAPHY_REVIEW_PROCESS.md#2-select-pages-and-inspect-responsive-typography) now defines future page selection, SPA states, substitutions for missing page types, bounded loading/access fallbacks, and representative viewports of 390 × 844, 768 × 1024, and 1440 × 900 CSS pixels. These are test conditions, not universal device breakpoints.

Keep per-page/per-width evidence, status, selection reasons, and limitations in repository documentation. Optional fluid-sizing notes should distinguish verified CSS declarations from observed computed values.

Before expanding the published studies:

- Re-review the existing eight only when separately authorized; preserve their dated desktop baseline.
- Agree on evidence storage and study-panel presentation for multiple pages and widths before changing the current schema.
- Apply the expanded protocol, verify newly encountered primary fonts, and document incomplete coverage.
- Evaluate review time and browser capabilities after the first expanded study.

The instructions are updated; expanded observations, responsive comparison UI, and new fluid-sizing sections have not been implemented.
