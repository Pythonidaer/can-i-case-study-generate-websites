# Website typography review process

Version 2 · October 27, 2026

## Purpose

Review user-supplied homepages one at a time, measure representative typography in a live browser, explain the choices using Type Study concepts, and append a screenshot-backed card to this gallery. These are independent observational studies, not official brand style guides.

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

Read the repository’s AGENTS.md and current files before editing. Inspect the current `main` branch and preserve existing studies and unrelated work. Never rebuild the record list from a stale copy.

If the Type Study framework is not already available, read its README, design instructions, vocabulary page, Choosing Type article, and roadmap notes through GitHub. The framework follows purpose, audience, inspiration, font roles, sizing and spacing, and a documented type guide.

Use plain beginner-friendly language. Distinguish legibility (recognizing characters) from readability (reading passages comfortably).

## 2. Inspect each homepage

1. Retrieve the supplied URL for initial context. Search snippets or extracted page text do not establish rendered font measurements.
2. Open the homepage in an approved live browser and record the actual URL after redirects.
3. Read the visible page structure and inspect its appearance. Reject optional cookies if offered; do not submit forms, purchase tickets, or subscribe.
4. Record the actual viewport width and height in CSS pixels. The first two batches were observed at 1363 × 936 CSS pixels on October 27, 2026 in America/New_York.
5. Inspect the page again if it is blank or mid-animation. Capture only after useful content is visibly present.
6. If access fails, report the actual error and mark the review incomplete. A timeout, 502 response, or connection error does not establish a robots.txt block. Do not bypass bot challenges.

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

Append records to `data.js`; preserve all previous records. Add the matching screenshot and update the visible collection count. Keep tag strings consistent with filters.

Preserve the Website Studies wordmark, Studies and Method anchors, and Review process Markdown download. The compact header stacks the brand above one short link row below 600px, without a dropdown. The Ws monogram is typographic branding, not an action icon. Do not add emoji or substitute text-glyph icons.

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

The review did not establish mobile typography, accessibility conformance, contrast ratios, commercial font licensing, or variable-font axes. Measurements are published in each study’s tables. Raw inspection records and agent-only instruction files are excluded from this public repository.

## Suggested continuation prompt

“Read TYPOGRAPHY_REVIEW_PROCESS.md and AGENTS.md in the Website Studies repository. Append studies for these homepages, preserving previous cards. Inspect each page visually and measure computed CSS. Label interpretations and unknowns, capture verified screenshots, use the existing study schema, check the relevant interactions, and publish to main when authorized.”
