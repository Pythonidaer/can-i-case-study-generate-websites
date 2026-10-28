# Website typography review process

Version 5 · October 28, 2026

## Purpose

Reconstruct evidence-backed typography guides from user-supplied websites, one at a time, so readers can understand and adapt their typography approaches when building new websites. Combine rendered measurements, relevant CSS evidence, and clearly grounded interpretation using Type Study concepts. Keep color analysis outside the current scope. These are independent observational studies, not official brand style guides.

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

The current eight records are homepage observations from October 27, 2026 at 1363 × 936 CSS pixels. Preserve their measurements, screenshots, and availability evidence until a separate re-review is authorized. The user authorized a re-review on October 28. It extends the desktop sample across pages and sections; target mobile/tablet and 1440px desktop rendering remain pending. The original records are archived in baseline-2026-10-27.json.

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

At each width, check loaded fonts, heading wrapping, paragraph width, navigation/actions, overflow, and relevant changes of hierarchy. Record family, size, weight, line height, letter spacing, and text box width for corresponding roles. Note when a role disappears or is replaced rather than comparing unrelated elements.

Use a brief resize check or relevant CSS inspection to investigate meaningful changes. Add one diagnostic width only when needed to explain a transition; do not exhaustively scan every pixel. Separate this source-site review from testing the gallery itself. Browser samples do not replace real-device testing or establish accessibility conformance.

### Evidence notes and future presentation

Keep a compact per-site evidence table in repository Markdown: page purpose, final URL/state, selection or substitution reason, review status, observation date, actual viewport, sampled roles, and screenshot reference. Group measurements by page and width so every claim can be traced to a sample. Record changed fonts and repeat the availability check for any newly discovered primary family.

The active schema now groups measurements in review.pages[].roles[]. The archived original schema holds one desktop measurement table. Preserve the original dated snapshot when extending comparisons. Do not overwrite it with mixed-width measurements or place authoring notes in public interface copy. Until that extension is implemented, retain expanded evidence in documentation and state coverage accurately.

Fluid-sizing notes are optional supporting evidence, not a required new public section. If relevant CSS is available, record the property, authored declaration (for example clamp(), min(), max(), viewport units, or media query), selector/role, source location, and observed computed values at the test widths. Describe an exact formula only when the declaration is verified. If only computed values are available, say “size changes across these samples; mechanism unverified.” Do not infer fluid scaling, variable-font axes, or a breakpoint from a screenshot or a few values alone.

## 3. Measure representative text roles

Use browser developer tools or the approved browser’s read-only DOM evaluation capability. Use Role to name the function of text in the interface, such as Hero heading, Hero description, Section heading, Body paragraph, Navigation link, Action label, Caption, or Statistic. Role here does not mean an HTML element, ARIA role, or future semantic color token. Record the HTML element separately when useful.

Scan each selected page broadly from top to bottom rather than sampling only the hero or the first DOM matches. Document meaningful distinct typography decisions wherever encountered, including footer navigation or legal text when they introduce a distinct treatment. Footer coverage is not a mandatory separate checklist item. The commitment is to record meaningful differences encountered in reviewed pages and states, not to claim discovery of every style across the entire site.

Give every sampled role a stable name and identifier within its page/state. Reuse the exact name in tables and commentary. Do not alternate between Body paragraph and Hero description unless evidence establishes they refer to the same treatment; distinguish roles even when some values match. Deduplicate repeated instances of the same role and treatment, but retain meaningful variants.

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
        letterSpacing: s.letterSpacing,
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

Record font stack, size, weight, line height, letter spacing, text transform, alignment, and box width. Keep raw precision in notes, but round measurement tables for readability. Retain only necessary source excerpts; numeric evidence should not reproduce long marketing passages.

### Inspect relevant CSS alongside rendered samples

Inspect accessible authored stylesheets, style blocks, matched rules, font declarations, and typography custom properties where browser capabilities allow. Connect any rule used in the guide to a visible sampled element and its computed values at the recorded viewport. Account for the cascade, inheritance, overrides, and loading state. Unused classes, unused tokens, and font declarations alone do not establish rendered styles. If CSS is inaccessible or unreadable, retain supported computed measurements and record the limitation in evidence notes.

### Evidence rules

- A computed font-family stack is not proof of which font file rendered every glyph.
- CSS family names may be aliases. Do not infer the commercial font identity or license from an alias.
- A CSS weight of 400 can look heavy in a display family. Weight values are not equivalent visual mass across families.
- Intermediate weights do not prove which variable axes exist.
- Line-height ratio equals line height divided by font size. Letter spacing in em equals letter spacing divided by font size.
- Element width is a box measurement, not a character-count measure.
- A few sampled sizes do not establish a complete modular scale or responsive formula.
- A screenshot does not establish contrast ratios or accessibility conformance.
- Distinguish measured facts from interpretations through grounded wording such as “may help” where appropriate. Keep general inference notices in shared methodology rather than repeating disclaimers in every short section.

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
  purpose: 'One or two concise sentences describing what the website offers and the visitor task.',
  pairing: 'Which family handles which role and what the contrast does.',
  rows: [
    ['Hero heading', '56 / 67.2', '500', '−1.12px']
  ],
  hierarchy: 'Reading order, scale, weight, case, and emphasis.',
  spacing: 'Widths, line-height ratios, letter spacing, and alignment.',
  reading: 'Reading conditions and specific untested concerns.',
  lesson: 'One transferable typography principle.',
  exercise: 'One practical comparison to try.',
  fallback: 'Observed fallback stack or an explicit unknown.'
}
```

Size and line height in `rows` are CSS pixels. Each row has four cells: role, size/line height, weight, letter spacing. The legacy records contain approximately five or six roles; this is not a cap for future guides. Include enough distinct observed roles and variants to explain the sampled typography system without listing every DOM instance.

### Target structure for the next authorized re-review

The October 28 renderer implements this structure using page-grouped role tables. Keep each original dated baseline traceable.

1. **Website purpose summary:** One or two concise sentences about what the website offers and what visitors need to learn, find, or do. Do not add generic inference disclaimers, inspection history, unsubmitted-form notes, or unrelated product-assessment caveats. Do not invent audience attributes to fill a second sentence.
2. **Fonts and roles:** Identify observed families, aliases where applicable, assigned roles, pairing, and fallback stacks. Keep detailed availability and licensing information in supporting material near the bottom.
3. **Type style guide:** Make this the main reusable reference. Use Role, Font family, Font size, Line height, Font weight, and Letter spacing consistently; add Font style, Text transform, or other measured properties when relevant. Separate font size and line height for clarity in the future table. Identify page/state and viewport for each sample or grouped table. Keep HTML elements separate from Role. Give rows stable anchors and make role references in later commentary link to their corresponding row in the same study. Ensure those links work within the dialog without dismissing it or losing context.
4. **Visual Hierarchy:** Explain how the measured roles use size, font weight, casing, placement, and spacing to communicate importance and reading order. Refer to the exact named roles and their rows.
5. **Spacing and line length:** Use those same role names to explain measured line height, letter spacing, text width, alignment, wrapping, and relevant block spacing. Distinguish box width from actual line length; do not claim measured character counts unless checked.
6. **Reading conditions:** Explain what the observed typography may do for readers, grounded in particular roles and comparisons. Identify specific supported concerns without repeatedly inserting generic audit disclaimers.

Follow the main analysis with concise supporting material: transferable lesson or exercise where useful, reference captures, detailed font availability/license sources, and the learning reference. Avoid repetitive Google Fonts and licensing statements; each primary family needs one clear dated classification and its relevant sources, while existing card/filter behavior remains intact.

Use developer-friendly CSS terminology throughout: font family, font size, line height, font weight, letter spacing, font style, text transform, and text width. Do not switch to type-design synonyms for the same property. Use the same role names across the guide and analysis.

### Type scale interpretation

A type scale is the set of sizes used. A modular scale generates sizes using a repeated ratio. Compare observed role sizes within the same viewport and coherent role group; do not combine mobile and desktop values to manufacture a ratio. Record relevant adjacent ratios and rounding when discussing an approximate pattern. Distinguish: approximately consistent ratio; ratio with adjustments; apparently individually chosen sizes; or insufficient evidence. Treat these as interpretations unless source declarations establish the system. Do not force a modular explanation, equate visual hierarchy with a modular scale, or claim designer intent from a close numerical match.

### Shared methodology and future implementation notes

Keep common scope and inference explanations in the existing Method section or repository methodology. A dedicated methodology page linked from the footer is a future option, not an implemented change. Keep a limitation next to a finding only when it materially changes interpretation. Public copy must stand alone for visitors and must not address the owner or describe the authoring conversation.

**TODO: CSS implementation notes.** Explore a short supporting section at the end for verified fluid sizing, `clamp()`, `min()`, `max()`, viewport units, typography custom properties, and breakpoint changes. For each useful example, connect the authored declaration and source to a named role and observed values. Distinguish verified implementation from an unexplained change in computed values. Do not add a public section merely to fill a template. This remains future presentation work; relevant evidence can be collected in repository notes during authorized reviews.

Keep the card summary short and details inside the dialog. These are reconstructed guides from sampled pages, not official design tokens or complete responsive specifications. Add per-study/page/viewport metadata before expanded comparisons; never combine different samples into an unlabeled legacy row.

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
2. Check unique IDs, expected count, required fields, measurement rows matching the active schema (four cells in legacy records), and nonempty image files.
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

The first batch covers Drivetrain, CarGurus careers, Mercury, and Verbatim. The second covers Bart Stefanski, Code Metal, Jerry Seinfeld, and CHEW. All eight originally used the Type Study framework and homepage browser observations. The October 28 re-review adds multiple pages or sections where present; see REVIEW_NOTES_2026-10-28.md for the actual scope.

The original review did not establish mobile typography, accessibility conformance, contrast ratios, commercial font licensing, or variable-font axes. A later availability review adds per-font source links and reuse classifications as described below. Measurements are published in each study’s tables. Raw inspection records and agent-only instruction files are excluded from this public repository.

## Suggested continuation prompt

“Read README.md, TYPOGRAPHY_REVIEW_PROCESS.md, and the current source in the Website Studies repository. Follow agent instructions if present. Review the supplied sites one at a time using the documented page-selection fallbacks and viewport sample. Preserve the original eight baseline studies unless re-review is authorized. Record scope, substitutions, access limits, measurements, screenshots, and font availability. Agree on a schema extension before publishing multi-page or responsive comparisons; never mix samples into a single desktop table. Check relevant interactions and publish to main only when authorized.”

## Font availability review and filtering

For every future study, add `fontAvailability: {checked: "YYYY-MM-DD", fonts: [...]}`. Each primary family record has `name`, `google` (true, false, or null for unverified), `license` (free, paid, or unknown), `label`, `source`, optional `licenseUrl`, and `note`. Check official Google Fonts catalog pages and the family’s license file, or the foundry/distributor’s licensing page. Record the check date and links. Do not treat a free trial or personal-use-only download as free commercial web use. Do not infer the identity or license of an unexplained CSS alias; record it as unknown. No font binaries need to be copied.

“All fonts on Google Fonts” and “All fonts free for commercial use” require every documented primary family to qualify; empty or incomplete records cannot pass. “At least one Google Font” allows mixed pairings. “Includes paid fonts” and “Includes unverified licenses” are separate: an unknown is not automatically paid. Exclude fallback/system stacks and decorative logo artwork from these primary-font checks, and state the scope in the UI.

Availability is now controlled by Google Font(s) and Free Font(s) toggle buttons alongside the style buttons. Multiple styles combine with OR; the selected availability requirements narrow those style results with AND. Each selected button can be pressed again to remove it. All styles clears only the style selection. There is no dropdown, reset button, explanatory filter paragraph, or result count. Preserve an informative empty state. Test that the all-Google and all-free results are Drivetrain, CarGurus, Bart Stefanski, Code Metal, and freeCodeCamp; that any-Google additionally includes Verbatim and CHEW; that paid includes Mercury, Verbatim, Jerry Seinfeld, and CHEW; and that unverified includes Mercury and CHEW. Update these expected lists when verified evidence or the catalogue changes.

For each new study, verify availability during the same review and include it on the card and in its detailed font section. Links and dated classifications help users choose fonts to investigate; they do not establish that a particular website used the identical distributed font file or that the user holds a paid license.

## Standardized dropdown navigation

The user requested Typography Learning’s navigation pattern in place of the stacked mobile link row. `navigation.css` and `navigation.js` are adapted from Pythonidaer/typography-learning’s `dist/navigation.css` and `dist/navigation.js`. Keep the 68px sticky frosted header, compact 1080px breakpoint, opaque dropdown, hamburger-to-close treatment, inert closed links, Escape dismissal, outside click/focus dismissal, link dismissal, breakpoint reset, and reduced-motion behavior. Website Studies retains its charcoal/mint palette and its existing destinations. Keep navigation styles in navigation.css and include both navigation assets in the deployment artifact.

## Multi-select filter buttons (October 28, 2026)

User-requested interface: Google Font(s) and Free Font(s) join the existing style buttons. Each button uses aria-pressed and toggles independently. Style choices form a union so Single family and Two families can both be selected without cancelling each other. The availability requirements intersect that union: all documented primary families must be on Google Fonts or verified free for commercial use, respectively. Unknown or empty family records cannot qualify. Both availability buttons may be active together. Clicking All styles clears style restrictions while preserving availability selections. Clicking the last active style restores All styles. No selected filters means the complete gallery.

Removed the dropdown, Reset filters control, filter explanatory paragraph, and result count at the user’s request. Keep detailed licensing sources and scope inside study panels. Test selecting multiple style buttons, combining with both font buttons, toggling individual filters off, preserving other selections, and returning to the full gallery.

## Active review schema and validation

The October 28 re-review is authorized. `data.js` retains existing card fields and adds `review: {version: 2, observed, timezone, coverage, pages: [...]}`. Each page has a stable `id`, `title`, verified `url`, actual `viewport`, `status`, optional selection `note`, and `roles`. Each role records `id`, `role`, `tag`, `family`, full `stack`, computed `size`, `line`, `weight`, `letterSpacing`, `fontStyle`, `textTransform`, `align`, and measured box `width`/`height`; `contentCase` distinguishes uppercase source content from CSS text-transform. Add verified `fontVariationSettings` when it materially affects interpretation.

Analysis references use `[[page-id:role-id]]`. The renderer resolves them to links that scroll and focus the row inside the open dialog. Validate every reference, unique study/page/role identifiers, full font coverage, consistent terminology, and preservation of the baseline. New fields must not silently mix dates, widths, pages, or font availability scopes. The legacy `rows` field is retained for compatibility, not the source for expanded tables.

The eight-site re-review contains 174 selected role samples across eight studies at 1363 × 936 CSS pixels. The browser cannot set requested viewport sizes; coverage is explicitly partial. Keep this limitation in shared methodology, the coverage disclosure, and evidence notes, not repetitive purpose-summary disclaimers. No public CSS implementation section or separate methodology page was added. The original dated screenshots remain historical references.

## freeCodeCamp addition (October 28, 2026)

The gallery now contains nine studies and 208 selected role samples. freeCodeCamp adds 34 roles across homepage, About/FAQ article, and default course catalog, all at the actual 1363 × 936 CSS-pixel viewport. See its section in REVIEW_NOTES_2026-10-28.md for partial coverage and CSS/font limits. Optional `referenceDate` labels the new capture October 28; records without it retain October 27. Single family and availability filters exclude system stacks; freeCodeCamp documents its system-heading exception explicitly. Preserve all original records and captures.
