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

- The eight-site desktop re-review was authorized and completed on October 28; the original baseline is preserved. Complete target-width checks when browser resizing is available.
- Page-grouped role tables and evidence notes are implemented; extend them with measured viewport samples when available.
- Apply the expanded protocol, verify newly encountered primary fonts, and document incomplete coverage.
- Evaluate review time and browser capabilities after the first expanded study.

The site now includes multi-page/section desktop observations. Mobile/tablet rendered measurements and a public CSS implementation section remain pending.

## To do: card font-availability labels

Explore the labels below the card divider (for example “All free · Google Fonts”) before changing their design. Clarify their context and visitor goals: what decision do they support, and how do they relate to filter buttons and detailed licensing sources? Review hierarchy relative to company name, font names, summary, and study action; assess plain text versus pills, wording, theme, palette, and accessible color contrast. Do not rely on color alone or make static labels look interactive without a purpose. Start with the smallest useful variable (such as wording, weight, spacing, or color), compare the result, and change one variable at a time before considering a broader redesign. This is a future exploration; the current labels remain unchanged.

Card company headings link to the source website in a new tab with the Material Icons `open_in_new` SVG (Google Material Design Icons, Apache-2.0; https://github.com/google/material-design-icons). Keep the visible icon, screen-reader new-tab notice, underline, hover treatment, and keyboard focus indicator. The study button remains a separate action; do not restore the duplicate bottom URL.

## Typography-guide direction and re-review gate

The [review process](TYPOGRAPHY_REVIEW_PROCESS.md) defines the next review as a reconstructed typography guide for adapting observed approaches to new websites. Keep Role as the text-function label, use CSS property terminology consistently, and name the analysis section Visual Hierarchy. Scan selected pages broadly and document distinct typography encountered, including footer treatments when relevant. The central Type style guide should use traceable role rows, separate font size and line height, and link later commentary to those rows.

The study panels now use: Website purpose summary; Fonts and roles; Type style guide; Visual Hierarchy; Spacing and line length; Reading conditions. Detailed font licensing follows the main analysis; general methodology is shared rather than repeated in each purpose summary. Preserve actual licensing evidence and existing filters. Consider an optional evidence-based type scale interpretation without forcing a modular ratio.

Future presentation tasks include a shared methodology page linked from the footer and a concise CSS implementation notes section for verified fluid sizing, clamp(), and breakpoints. Color analysis remains outside the current review scope.

The user authorized re-review of all eight studies. The records and renderer now implement this structure. The responsive portion remains partial because the available browser does not expose viewport resizing.

## October 28 re-review evidence

See [REVIEW_NOTES_2026-10-28.md](REVIEW_NOTES_2026-10-28.md) for page selection, substitutions, measured roles, CSS evidence, and remaining coverage. The 174 role samples are grouped by page or section at the actual 1363 × 936 CSS-pixel browser viewport. The requested 390 × 844, 768 × 1024, and 1440 × 900 conditions were not rendered. Do not present CSS predictions as measured mobile values.

[baseline-2026-10-27.json](baseline-2026-10-27.json) preserves the original eight records. Public images remain those original dated captures; the expanded tables describe the new review. `data.js` adds `review.pages[].roles[]` with stable IDs, role names, font stacks and computed properties. `app.js` renders each group and resolves commentary references to rows inside the dialog.

New primary-font findings include Tiempos on Mercury’s article, Hagrid Heavy on Verbatim, and PP Mori on CHEW. Font availability records were rechecked; the all-Google/all-free result remains Drivetrain, CarGurus, Bart Stefanski, and Code Metal. Mixed paid and unknown classifications remain explicit.
