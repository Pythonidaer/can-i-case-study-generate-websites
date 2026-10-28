# Website typography review process

Version 3 · October 28, 2026

## Purpose

Review user-supplied websites one at a time, measure representative typography in a live browser, explain the choices using Type Study concepts, and append a screenshot-backed card to this gallery. These are independent observational studies, not official brand style guides.

Repeat this method and evidence standard. Websites, fonts, and animations can change; identical measurements or screenshots cannot be guaranteed on another date or device.

## Project and files

Repository: https://github.com/Pythonidaer/can-i-case-study-generate-websites

Learning reference: https://github.com/Pythonidaer/typography-learning

Publish this repository’s root source through the GitHub Pages workflow on `main`. The learning reference is separate and should not be edited as part of maintaining this gallery.

| File | Purpose |
| --- | --- |
| `index.html` | Header, filters, gallery, methodology, dialog shell |
| `style.css` | Responsive layout and text styles |
| `data.js` | All case-study records |
| `app.js` | Cards, filtering, and study dialogs |
| `assets/` | Homepage reference screenshots |
| `TYPOGRAPHY_REVIEW_PROCESS.md` | This downloadable workflow |

## 1. Review the current source and learning framework

Read the current README, this process, and source files before editing. Follow AGENTS.md if one exists; do not assume this repository contains one. Inspect the current `main` branch and preserve existing studies and unrelated work. Never rebuild the record list from a stale copy.

If the Type Study framework is not already available, read its README, design instructions, vocabulary page, Choosing Type article, and roadmap notes through GitHub. The framework follows purpose, audience, inspiration, font roles, sizing and spacing, and a documented type guide.

Use plain beginner-friendly language. Distinguish legibility (recognizing characters) from readability (reading passages comfortably).

## 2. Select pages and inspect responsive typography

### Preserve the existing baseline

The current eight records are homepage observations from October 27, 2026 at 1363 × 936 CSS pixels. Preserve their measurements, screenshots, and availability evidence until a separate re-review is authorized. This expanded procedure defines future work; it does not mean the eight studies have already been reviewed across pages or widths.

Use the same Type Study concepts, representative text roles, evidence rules, font checks, and concise original analysis as those records. Record differences in scope explicitly rather than implying that older and newer studies have identical coverage.

### Select by page purpose, with documented substitutions

Start at the supplied URL and record its final URL after redirects. Use the site's navigation and visible internal links to choose a small sample:

| Preferred sample | Selection rule | Fallback |
| --- | --- | --- |
| Homepage | Main entry page and primary hierarchy | Supplied landing page if no separate homepage is available |
| Content-heavy page | Article, documentation, case study, about page, or comparable sustained reading | Long-form section or expanded content state on the same page |
| Product, service, or listing page | A representative offering, detail page, directory, portfolio, or results list | Another materially different template, such as pricing, work detail, or an event page |

Choose representative typography, not arbitrary URLs. Avoid three nearly identical templates. Usually inspect up to three distinct pages or meaningful states per site. A smaller site may need only one or two; mark absent page types as not applicable. Explain each substitution briefly. Add another template only when it reveals an important missing text role, and record the reason rather than expanding without limit.

A single-page application can supply distinct routes or states without a full document load. Navigate through visible controls, wait for the route and useful content to settle, and record the URL plus the state, section, or tab used. Several sections on one scrolling page remain one page; do not present them as independent templates. Record routes that cannot be opened directly or states that cannot be reproduced reliably.

### Loading and access fallback

1. Retrieve the supplied URL for context, then inspect it in an approved live browser. Search snippets and extracted text do not establish rendered typography.
2. Read the visible structure. Dismiss optional cookie overlays when possible. Do not submit forms, subscribe, purchase, or access account-only content without authorization.
3. Wait for useful content and fonts to settle; scroll to trigger ordinary lazy loading. If blank or mid-animation, inspect again and allow one bounded retry or reload. Do not repeatedly retry a failing page.
4. If a direct route fails, try reaching the same public content through the site's visible navigation. If it remains inaccessible, choose a comparable accessible public page and document the substitution.
5. For a challenge, login wall, persistent timeout, or error, record the actual symptom, affected URL/state, date, and what could be inspected. Do not bypass access controls or bot challenges. A 502 or timeout does not establish a robots.txt block.
6. Mark each sample complete, partial, blocked, or not applicable. Preserve supported observations and clearly identify missing roles or widths. If no useful rendered content is accessible, leave the study incomplete; do not fabricate measurements or publish an apparently complete card.

### Consistent viewport sample

Use 390 × 844, 768 × 1024, and 1440 × 900 CSS pixels as representative mobile, tablet, and desktop browser viewports for future expanded reviews. These are repeatable test conditions, not claims about device models or the site's CSS breakpoints.

For each selected page or state, inspect the same representative text roles at all three widths, when available. Record actual inner viewport dimensions, browser/zoom conditions, date and timezone, and missing samples. If the browser cannot set a requested viewport, record the actual dimensions and the limitation; do not label a desktop capture as mobile evidence.

At each width, check loaded fonts, heading wrapping, paragraph width, navigation/actions, overflow, and relevant changes of hierarchy. Record family, size, weight, line height, tracking, and text box width for corresponding roles. Note when a role disappears or is replaced rather than comparing unrelated elements.

Use a brief resize check or relevant CSS inspection to investigate meaningful changes. Add one diagnostic width only when needed to explain a transition; do not exhaustively scan every pixel. Separate this source-site review from testing the gallery itself. Browser samples do not replace real-device testing or establish accessibility conformance.

### Evidence notes and future presentation

Keep a compact per-site evidence table in repository Markdown: page purpose, final URL/state, selection or substitution reason, review status, observation date, actual viewport, sampled roles, and screenshot reference. Group measurements by page and width so every claim can be traced to a sample. Record changed fonts and repeat the availability check for any newly discovered primary family.

The current card schema holds one desktop measurement table. Before publishing expanded comparisons, agree on a storage and presentation extension that preserves the original dated snapshot. Do not overwrite it with mixed-width measurements or place authoring notes in public interface copy. Until that extension is implemented, retain expanded evidence in documentation and state coverage accurately.

Fluid-sizing notes are optional supporting evidence, not a required new public section. If relevant CSS is available, record the property, authored declaration (for example clamp(), min(), max(), viewport units, or media query), selector/role, source location, and observed computed values at the test widths. Describe an exact formula only when the declaration is verified. If only computed values are available, say “size changes across these samples; mechanism unverified.” Do not infer fluid scaling, variable-font axes, or a breakpoint from a screenshot or a few values alone.

## 3. Measure representative text roles

Use browser developer tools or the approved browser’s read-only DOM evaluation capability. Sample the hero title, section title, paragraph, navigation, action, and caption or statistic when present.

The following page-scope JavaScript illustrates the discovery sampler. Run it only through the browser interface available in the current environment:

```javascript
(() => ({
  url: location.href,
  viewport: { width: innerWidth, height: innerHeight },
  rows: [...document.querySelectorAll('h1,h2,h3,p,a,button,small,time')]
    .filter(el => {
      const s = getComputedStyle(el);
      return el.getBoundingClientRect().width > 0 &&
        s.display !== 'none' && s.visibility !== 'hidden' &&
        el.textContent.trim();
    })
    .slice(0, 35)
    .map(el => {
      const s = getComputedStyle(el);
      return {
        tag: el.tagName,
        text: el.textContent.trim().replace(/\s+/g, ' ').slice(0, 95),
        font: s.fontFamily,
        size: s.fontSize,
        weight: s.fontWeight,
        line: s.lineHeight,
        tracking: s.letterSpacing,
        style: s.fontStyle,
        transform: s.textTransform,
        color: s.color,
        width: Math.round(el.getBoundingClientRect().width)
      };
    })
}))()
```

This is a discovery sample, not an audit. It can include clipped, offscreen, screen-reader-only, duplicate, or collapsed text. Match selected rows to visible content and reject irrelevant nodes. The first 35 matches may miss paragraphs, so inspect specific visible elements when necessary. Text can also live in divs and spans.

Inspect nested spans when a heading visibly changes weight, color, font, or style. Read both the parent and its descendants. Bart Stefanski’s introduction demonstrated why: its parent reported weight 700, while some phrases were weight 400.

Record font stack, size, weight, line height, tracking, text transform, alignment, and box width. Keep raw precision in notes, but round measurement tables for readability. Retain only necessary source excerpts; numeric evidence should not reproduce long marketing passages.

### Evidence rules

- A computed font-family stack is not proof of which font file rendered every glyph.
- CSS family names may be aliases. Do not infer the commercial font identity or license from an alias.
- A CSS weight of 400 can look heavy in a display family. Weight values are not equivalent visual mass across families.
- Intermediate weights do not prove which variable axes exist.
- Line-height ratio equals line height divided by font size. Tracking in em equals letter spacing divided by font size.
- Element width is a box measurement, not a character-count measure.
- A few sampled sizes do not establish a complete modular scale or responsive formula.
- A screenshot does not establish contrast ratios or accessibility conformance.
- Label inferred purpose, audience, personality, and effects as interpretations.

## 4. Capture the reference screenshot

Capture a viewport image, inspect it, and save the inspected bytes as `assets/<study-id>-type.jpg`. Check that the file is nonempty and shows the correct page. Avoid cookie dialogs, blank loading screens, and unfinished fades.

The initial CarGurus capture was blank and was replaced after content loaded. Jerry Seinfeld’s first view was mid-fade and was captured again after settling. Dynamic imagery, clocks, and animation mean later captures may differ.

Use screenshots of the actual website rather than downloading and redistributing its font binaries. Do not claim font licensing has been checked unless it has.

## 5. Write the study record

Write original analysis using the same fields as existing records:

```javascript
{
  id: 'unique-lowercase-id',
  name: 'Website name',
  url: 'https://verified-homepage.example/',
  fonts: 'Observed family names or explicitly labeled aliases',
  tags: ['Two families', 'Useful category'],
  summary: 'A concise description of the typography approach.',
  purpose: 'Reader task and audience, with inference labeled.',
  pairing: 'Which family handles which role and what the contrast does.',
  rows: [
    ['Hero title', '56 / 67.2', '500', '−1.12px']
  ],
  hierarchy: 'Reading order, scale, weight, case, and emphasis.',
  spacing: 'Widths, line-height ratios, tracking, and alignment.',
  reading: 'Reading conditions and specific untested concerns.',
  lesson: 'One transferable typography principle.',
  exercise: 'One practical comparison to try.',
  fallback: 'Observed fallback stack or an explicit unknown.'
}
```

Size and line height in `rows` are CSS pixels. Each row has four cells: role, size/line height, weight, tracking. Include five or six representative roles rather than every DOM element.

The dialog presents six numbered sections: purpose and audience; font roles and pairing; sampled styles; hierarchy; spacing and line length; reading conditions. It then shows a lesson, exercise, screenshot, and Type Study reference.

Keep the card summary short and details inside the dialog. These are desktop snapshots, not official design tokens or full responsive specifications. If later studies use different dates or viewports, add per-study metadata and update the renderer instead of retaining inaccurate shared labels.

### Filter meanings

| Filter | Meaning |
| --- | --- |
| Single family | One sampled family across primary roles |
| Display and text | Related display/text treatments or variants |
| Two families | Distinct sampled CSS families assigned roles |
| Sans and mono | Proportional sans-serif paired with monospace |

These are useful study categories, not an authoritative typeface taxonomy or complete font inventory.

## 6. Integrate the card

Append records to `data.js`; preserve all previous records. Add the matching screenshot. Do not reintroduce a visible collection count. Keep tag strings consistent with filters.

Preserve the Website Studies wordmark, Studies and Method anchors, and Review process Markdown download. The header uses the standardized Typography Learning nonmodal dropdown at 1080px and below. A 44px icon-only trigger opens an opaque full-width menu; Escape, link activation, outside click, and focus leaving the header close it. Larger screens keep inline links. The Ws monogram is typographic branding, not an action icon. Do not add emoji or substitute text-glyph icons.

Keep relative URLs working under the GitHub Pages repository subpath. The grid has four columns on desktop, two below 1100px, and one below 600px. Preserve native modal dialogs, explicit dismissal, and visible keyboard focus.

## 7. Validate

1. Run `node --check app.js` and `node --check data.js`.
2. Check unique IDs, expected count, required fields, four cells per measurement row, and nonempty image files.
3. Serve the root with an ordinary static server and open it through the approved browser preview.
4. Inspect the header, grid, and reference images. Open new dialogs and confirm the corresponding title, measurements, analysis, and screenshot.
5. Exercise filters, Show all, Close study, Escape, and the section links. Verify counts against the data.
6. Test narrow layout, text enlargement, focus, and overflow when supported. If unavailable, report the limit rather than treating CSS breakpoints as mobile visual verification.
7. Save a final screenshot of the updated page. Report the checks actually performed.

## 8. Publish to GitHub Pages

The site is buildless: no dependencies or framework build are required. Keep deployable files at the repository root and retain `.nojekyll`.

Commit verified changes to `main` only when authorized. Base updates on the inspected current head and avoid force pushes. The deployment workflow is `.github/workflows/deploy-pages.yml`. It runs on pushes to main or manual dispatch, checks JavaScript, copies only public site files into a static artifact, and deploys with the official GitHub Pages actions. GitHub Pages must have GitHub Actions selected as its publishing source. Preserve any existing custom domain and access settings.

Verify the new commit and check the deployed page separately. A commit to main alone is not proof that Pages publication succeeded. Check the rendered page and relative CSS, JavaScript, image, and Markdown URLs under the repository subpath.

## Existing studies and limits

The first batch covers Drivetrain, CarGurus careers, Mercury, and Verbatim. The second covers Bart Stefanski, Code Metal, Jerry Seinfeld, and CHEW. All eight use the Type Study framework and homepage browser observations.

The original review did not establish mobile typography, accessibility conformance, contrast ratios, commercial font licensing, or variable-font axes. A later availability review adds per-font source links and reuse classifications as described below. Measurements are published in each study’s tables. Raw inspection records and agent-only instruction files are excluded from this public repository.

## Suggested continuation prompt

“Read README.md, TYPOGRAPHY_REVIEW_PROCESS.md, and the current source in the Website Studies repository. Follow agent instructions if present. Review the supplied sites one at a time using the documented page-selection fallbacks and viewport sample. Preserve the original eight baseline studies unless re-review is authorized. Record scope, substitutions, access limits, measurements, screenshots, and font availability. Agree on a schema extension before publishing multi-page or responsive comparisons; never mix samples into a single desktop table. Check relevant interactions and publish to main only when authorized.”

## Font availability review and filtering

For every future study, add `fontAvailability: {checked: "YYYY-MM-DD", fonts: [...]}`. Each primary family record has `name`, `google` (true, false, or null for unverified), `license` (free, paid, or unknown), `label`, `source`, optional `licenseUrl`, and `note`. Check official Google Fonts catalog pages and the family’s license file, or the foundry/distributor’s licensing page. Record the check date and links. Do not treat a free trial or personal-use-only download as free commercial web use. Do not infer the identity or license of an unexplained CSS alias; record it as unknown. No font binaries need to be copied.

“All fonts on Google Fonts” and “All fonts free for commercial use” require every documented primary family to qualify; empty or incomplete records cannot pass. “At least one Google Font” allows mixed pairings. “Includes paid fonts” and “Includes unverified licenses” are separate: an unknown is not automatically paid. Exclude fallback/system stacks and decorative logo artwork from these primary-font checks, and state the scope in the UI.

Availability is now controlled by Google Font(s) and Free Font(s) toggle buttons alongside the style buttons. Multiple styles combine with OR; the selected availability requirements narrow those style results with AND. Each selected button can be pressed again to remove it. All styles clears only the style selection. There is no dropdown, reset button, explanatory filter paragraph, or result count. Preserve an informative empty state. Test that the all-Google and all-free results are Drivetrain, CarGurus, Bart Stefanski, and Code Metal; that any-Google additionally includes Verbatim and CHEW; that paid includes Verbatim and Jerry Seinfeld; and that unverified includes Mercury and CHEW. Update these expected lists when verified evidence or the catalogue changes.

For each new study, verify availability during the same review and include it on the card and in its detailed font section. Links and dated classifications help users choose fonts to investigate; they do not establish that a particular website used the identical distributed font file or that the user holds a paid license.

## Standardized dropdown navigation

The user requested Typography Learning’s navigation pattern in place of the stacked mobile link row. `navigation.css` and `navigation.js` are adapted from Pythonidaer/typography-learning’s `dist/navigation.css` and `dist/navigation.js`. Keep the 68px sticky frosted header, compact 1080px breakpoint, opaque dropdown, hamburger-to-close treatment, inert closed links, Escape dismissal, outside click/focus dismissal, link dismissal, breakpoint reset, and reduced-motion behavior. Website Studies retains its charcoal/mint palette and its existing destinations. Keep navigation styles in navigation.css and include both navigation assets in the deployment artifact.

## Multi-select filter buttons (October 28, 2026)

User-requested interface: Google Font(s) and Free Font(s) join the existing style buttons. Each button uses aria-pressed and toggles independently. Style choices form a union so Single family and Two families can both be selected without cancelling each other. The availability requirements intersect that union: all documented primary families must be on Google Fonts or verified free for commercial use, respectively. Unknown or empty family records cannot qualify. Both availability buttons may be active together. Clicking All styles clears style restrictions while preserving availability selections. Clicking the last active style restores All styles. No selected filters means the complete gallery.

Removed the dropdown, Reset filters control, filter explanatory paragraph, and result count at the user’s request. Keep detailed licensing sources and scope inside study panels. Test selecting multiple style buttons, combining with both font buttons, toggling individual filters off, preserving other selections, and returning to the full gallery.
