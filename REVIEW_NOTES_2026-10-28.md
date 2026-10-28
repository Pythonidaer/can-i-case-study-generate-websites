# Typography re-review — October 28, 2026

## Scope and reproducibility

All eight sites were revisited in a live browser. The review samples rendered text across selected pages or meaningful sections and inspects accessible CSS. Measurements use the actual browser viewport of **1363 × 936 CSS pixels**, device pixel ratio 1 where reported. Browser zoom was not independently verified. The browser API did not expose viewport resizing; **390 × 844, 768 × 1024, and 1440 × 900 were not rendered or measured**. This is a partial responsive review, not completion of the three-width protocol. CSS declarations below are implementation evidence, not mobile screenshots or computed mobile values.

The original October 27 studies are preserved in [baseline-2026-10-27.json](baseline-2026-10-27.json). Existing public homepage images remain the original dated references; they are not evidence of new widths or additional pages. Current page appearances and single-page sections were inspected during this review. Numeric tables below omit marketing passages and internal browser records.

The review uses the Type Study purpose, font-role, hierarchy, spacing, and reading framework. Role labels describe interface functions; HTML elements are recorded separately. Measurements report computed CSS rather than asserting font-file identity. Body containers inheriting a family without rendering direct text are not added to the primary-font inventory. Color analysis remains out of scope.

## Selection and access outcomes

- Drivetrain: homepage, linked AI-spending article, and linked financial-reporting use case.
- CarGurus: homepage, Life culture page as sustained-reading sample, and job search results. The listing initially exposed a loading shell; a subsequent check showed actual job titles and results. Use the settled sample.
- Mercury: homepage, business-banking product page, and linked partner-bank article. Editorial pages introduce serif families absent from the initial homepage inventory.
- Verbatim: homepage, Skillshare case study, and services page. Animated entrance content initially appeared blank; a later view confirmed the homepage display. The case table includes the measured introduction and body roles, not an invented hero style.
- Bart Stefanski: homepage, linked Cloudflare technical article, and projects listing. Miniature product mockups are excluded from the portfolio’s primary style inventory.
- Code Metal: homepage, linked type-mapping research article, and product page.
- Jerry Seinfeld: one scrolling document, with Welcome, Tour dates, and Work sections. Work summaries substitute for a separate article template. These are sections of one page, not three page templates.
- CHEW: one scrolling document including How we work and The receipts service/case sections. No separate article or product template was present in the observed navigation.

No forms, subscriptions, ticket purchases, or account actions were submitted. No bot challenge or access-control bypass was needed. Some external stylesheets could not be read through the browser CSSOM; computed values remained available.

## Drivetrain

Drivetrain offers financial planning software for finance teams to build forecasts, compare scenarios, and evaluate whether to request a demo.

### Homepage

URL: https://www.drivetrain.ai/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | Google Sans Flex | 56px | 67.2px | 500 | -1.12px | 724px | center |
| Hero description | p | Google Sans Flex | 16px | 25.6px | 400 | -0.16px | 724px | center |
| Hero introductory label | p | Google Sans Flex | 12px | 16.8px | 500 | normal | 313px | center |
| Navigation label | button | Google Sans Flex | 14px | 21px | 500 | -0.14px | 104px | center |
| Action label | a | Google Sans Flex | 14px | 20px | 500 | -0.14px | 84px | center |
| Section heading | h2 | Google Sans Flex | 36px | 48.24px | 500 | -0.9px | 460px | start |
| Display section heading | h2 | Google Sans Flex | 44px | 52.8px | 500 | -0.88px | 574px | center |
| Feature paragraph | p | Google Sans Flex | 16px | 25.6px | 500 | -0.16px | 343px | start |
| Compact section heading | h2 | Google Sans Flex | 32px | 44.8px | 500 | -0.48px | 434px | start |
| Feature heading | h3 | Google Sans Flex | 18px | 27px | 500 | normal | 520px | start |
| Footer description | p | Google Sans Flex | 14px | 21px | 400 | -0.14px | 320px | start |
| Footer legal text | span | Google Sans Flex | 12px | 18px | 400 | -0.12px | 228px | start |

### Article

URL: https://www.drivetrain.ai/post/ai-spending

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Article heading | h1 | Google Sans Flex | 44px | 52.8px | 500 | -0.88px | 760px | start |
| Article introduction | p | Google Sans Flex | 16px | 25.6px | 400 | -0.16px | 760px | start |
| Article section heading | h2 | Google Sans Flex | 24px | 33.6px | 500 | -0.24px | 760px | start |
| Article subsection heading | h3 | Google Sans Flex | 20px | 30px | 500 | -0.2px | 760px | start |
| Article paragraph | p | Google Sans Flex | 16px | 25.6px | 400 | -0.16px | 760px | start |
| Summary list item | li | Google Sans Flex | 16px | 25.6px | 400 | -0.16px | 654px | start |
| Author label | p | Google Sans Flex | 12px | 16.8px | 500 | 0.72px | 710px | start |
| Contents link | a | Google Sans Flex | 12px | 18px | 400 | normal | 197px | start |

### Financial reporting

URL: https://www.drivetrain.ai/use-cases/financial-reporting

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Product heading | h1 | Google Sans Flex | 44px | 52.8px | 500 | -0.88px | 518px | start |
| Product description | p | Google Sans Flex | 16px | 25.6px | 400 | -0.16px | 518px | start |
| Section heading | h2 | Google Sans Flex | 36px | 48.24px | 500 | -0.9px | 521px | center |
| Feature heading | h3 | Google Sans Flex | 24px | 33.6px | 500 | -0.24px | 465px | start |
| Agent heading | h3 | Google Sans Flex | 18px | 27px | 500 | -0.18px | 267px | left |
| Step label | p | Google Sans Flex | 12px | 16.8px | 500 | 0.72px | 465px | start |

Type scale interpretation: The heading set includes 24, 32, 36, 44, and 56px. Adjacent ratios are approximately 1.33, 1.13, 1.22, and 1.27: an adjusted set, not evidence of one repeated modular ratio.

### CSS evidence notes

The sampled `.text-h1`, `.text-body`, and related classes resolve font size, line height, and letter spacing from custom properties. Responsive rules include a `.max-md:text-[1.5rem]` treatment below 768px on matched heading elements. Their presence does not establish the final mobile rendering.

Inspected stylesheet sources:
- https://www.drivetrain.ai/_next/static/immutable/chunks/1akf1-2psci17.css

### Font availability sources

- Google Sans Flex: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Google+Sans+Flex · https://github.com/google/fonts/blob/main/ofl/googlesansflex/OFL.txt

## CarGurus careers

CarGurus’s careers website introduces the workplace, benefits, and open positions so prospective employees can find suitable roles.

### Homepage

URL: https://careers.cargurus.com/us/en/home

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | Outfit | 48px | 60px | 600 | normal | 597px | start |
| Section heading | h2 | Outfit | 48px | 60px | 600 | normal | 1194px | center |
| Introductory paragraph | div | Outfit | 20px | 25px | 400 | normal | 1194px | center |
| Statistic | h3 | Outfit | 68px | 85px | 600 | normal | 345px | center |
| Values heading | h3 | Outfit | 28px | 35px | 700 | normal | 377px | start |
| Feature heading | h3 | Outfit | 28px | 35px | 500 | normal | 317px | center |
| Navigation label | span | Outfit | 18px | 21.6px | 400 | normal | 87px | start |
| Action label | span | Outfit | 16px | 19.2px | 400 | normal | 82px | center |
| Footnote | div | Outfit | 12px | 18px | 400 | normal | 1194px | start |
| Footer heading | h2 | Outfit | 16px | 20px | 700 | normal | 361px | start |
| Footer navigation | a | Outfit | 16px | 16px | 400 | normal | 116px | start |
| Footer legal text | h2 | Outfit | 16px | 20px | 400 | normal | 1194px | end |

### Life at CarGurus

URL: https://careers.cargurus.com/us/en/life

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | Outfit | 56px | 70px | 600 | normal | 597px | start |
| Section heading | h2 | Outfit | 48px | 60px | 600 | normal | 1194px | center |
| Benefit heading | h3 | Outfit | 28px | 35px | 500 | normal | 268px | center |
| Community statement | div | Outfit | 28px | 42px | 500 | normal | 1194px | center |
| Community description | div | Outfit | 14px | 21px | 400 | normal | 118px | center |
| Benefit description | div | Outfit | 16px | 24px | 500 | normal | 1130px | center |

### Job listings

URL: https://careers.cargurus.com/us/en/search-results

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

Results loaded after the initial shell; measurements use the settled list.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Listing heading | h1 | Outfit | 56px | 70px | 600 | normal | 597px | start |
| Filter heading | span | Outfit | 20px | 24px | 600 | normal | 85px | center |
| Job title | a | Outfit | 20px | 25px | 700 | normal | 653px | start |
| Results summary | div | Outfit | 16px | 25.6px | 400 | normal | 185px | start |
| Alert action | button | Outfit | 16px | 19.2px | 400 | normal | 190px | center |

Type scale interpretation: Selected headline sizes are 28, 48, 56, and 68px, with ratios 1.71, 1.17, and 1.21. They appear adjusted for their content roles; the sample does not support one modular ratio.

### CSS evidence notes

The external Phenom/CDN stylesheets were inaccessible through CSSOM. The guide relies on rendered computed values; no fluid-sizing formula or exact breakpoint is claimed.

### Font availability sources

- Outfit: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Outfit · https://github.com/google/fonts/blob/main/ofl/outfit/OFL.txt

## Mercury

Mercury presents business banking and financial tools, explains how its services work, and guides businesses toward opening an account.

### Homepage

URL: https://mercury.com/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | span | arcadiaDisplay | 47.2928px | 52.0221px | 480 | normal | 626px | center |
| Hero description | span | arcadia | 21.008px | 28.3608px | 360 | normal | 619px | center |
| Navigation label | button | arcadia | 16px | 16px | 420 | normal | 125px | center |
| Section heading | span | arcadiaDisplay | 42px | 48.3px | 480 | 0.42px | 626px | center |
| Compact section heading | span | arcadiaDisplay | 32px | 36.8px | 480 | 0.48px | 626px | left |
| Feature heading | span | arcadia | 18px | 24.3px | 480 | normal | 277px | left |
| Feature description | span | arcadia | 18px | 24.3px | 360 | normal | 448px | left |
| Statistic | span | arcadiaDisplay | 62.5258px | 68.7784px | 480 | normal | 184px | center |
| Footer navigation | span | arcadia | 16px | 20px | 420 | normal | 139px | start |
| Footer legal heading | h2 | arcadia | 12px | 16.8px | 400 | 0.24px | 318px | start |
| Footer legal text | span | arcadia | 12px | 16.8px | 400 | 0.24px | 147px | start |

### Business banking

URL: https://mercury.com/business-banking

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Product heading | span | arcadiaDisplay | 54.6074px | 60.0681px | 480 | normal | 791px | center |
| Product description | span | arcadia | 21.008px | 28.3608px | 360 | normal | 688px | center |
| Section heading | span | arcadiaDisplay | 42px | 48.3px | 480 | 0.42px | 626px | center |
| Benefit heading | span | arcadia | 18px | 24.3px | 480 | normal | 288px | center |
| Benefit description | span | arcadia | 18px | 24.3px | 360 | normal | 275px | center |
| Feature heading | span | arcadiaDisplay | 28px | 33.6px | 480 | 0.42px | 245px | left |
| Testimonial | span | arcadiaDisplay | 28px | 33.6px | 360 | 0.42px | 642px | center |

### Partner-bank article

URL: https://mercury.com/blog/how-mercury-works-with-partner-banks

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Article heading | h1 | tiemposFine | 42px | 46.2px | 500 | normal | 626px | center |
| Article introduction | span | tiemposHeadline | 21.008px | 26.26px | 400 | normal | 626px | center |
| Article paragraph | p | tiempos | 18px | 25.2px | 400 | normal | 626px | start |
| Article category | span | arcadia | 14px | 14px | 500 | 0.28px | 626px | center |
| Author metadata | span | arcadia | 14px | 19.6px | 400 | 0.14px | 24px | start |
| Related article heading | h2 | tiemposHeadline | 21.008px | 26.26px | 400 | normal | 297px | start |

Type scale interpretation: Marketing and editorial roles use different families and size sets. The homepage contains 24, 28, 32, 42, and approximately 47.29px display treatments; their uneven ratios do not establish one modular scale.

### CSS evidence notes

The sampled Arcadia classes use custom properties. `.arcadia-body-2` changes its font-size token at min-width 48rem and 64rem. `.arcadia-heading-7` has rules at 64rem and 96rem. These establish authored conditions, not rendered mobile outcomes. An inherited IBM Plex Mono value on a multi-element container was excluded because it did not identify a directly rendered primary text role.

Inspected stylesheet sources:
- https://mercury.com/_next/static/chunks/1nnoba5m4czls.css

### Font availability sources

- Arcadia Display: License unverified. https://mercury.com/
- Arcadia: License unverified. https://mercury.com/
- Tiempos Fine (CSS: tiemposFine): Paid commercial font. https://klim.co.nz/collections/tiempos/ · https://klim.co.nz/licences/
- Tiempos Headline (CSS: tiemposHeadline): Paid commercial font. https://klim.co.nz/collections/tiempos/ · https://klim.co.nz/licences/
- Tiempos Text (CSS: tiempos): Paid commercial font. https://klim.co.nz/collections/tiempos/ · https://klim.co.nz/licences/

## Verbatim

Verbatim presents influencer-marketing and speaker services, using case studies to help brands assess the agency and arrange a conversation.

### Homepage

URL: https://www.weareverbatim.com/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | Hagrid Text Var Variable Regular | 92px | 82.8px | 400 | -1.84px | 864px | center |
| Hero description | p | Bricolage Grotesque | 20px | 26px | 300 | normal | 526px | center |
| Navigation label | a | Bricolage Grotesque | 18px | 21.6px | 300 | normal | 83px | start |
| Animated display phrase | span | Hagrid Heavy | 98px | 98px | 900 | -1.96px | 309px | center |
| Strategy heading | p | Hagrid Text Var Variable Regular | 56px | 56px | 400 | normal | 498px | start |
| Strategy paragraph | p | Bricolage Grotesque | 18px | 23.4px | 300 | normal | 580px | start |
| Oversized section heading | h2 | Hagrid Text Var Variable Regular | 180px | 216px | 400 | -3.6px | 1257px | center |
| Service heading | h3 | Hagrid Text Var Variable Regular | 60px | 72px | 400 | -1.2px | 500px | start |
| Work section heading | h2 | Hagrid Text Var Variable Regular | 80px | 96px | 400 | -1.6px | 500px | center |
| Case card heading | h3 | Hagrid Text Var Variable Regular | 32px | 44.8px | 400 | -1px | 220px | start |
| Case card description | p | Bricolage Grotesque | 16px | 20.8px | 300 | normal | 324px | start |
| Footer description | p | Bricolage Grotesque | 14px | 18.2px | 300 | normal | 480px | start |
| Footer legal text | p | Bricolage Grotesque | 14px | 16.8px | 300 | normal | 119px | start |

### Skillshare case study

URL: https://www.weareverbatim.com/work/skillshare

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Case introduction | p | Bricolage Grotesque | 20px | 26px | 300 | normal | 460px | center |
| Case section heading | h2 | Hagrid Text Var Variable Regular | 36px | 50.4px | 400 | -0.72px | 448px | start |
| Case paragraph | p | Bricolage Grotesque | 20px | 24px | 300 | normal | 448px | start |
| Metric label | p | Bricolage Grotesque | 14px | 16.8px | 300 | -0.28px | 216px | start |
| Metric value | p | Hagrid Text Var Variable Regular | 28px | 33.6px | 400 | -0.56px | 64px | right |
| Testimonial attribution | p | Hagrid Text Var Variable Regular | 24px | 24px | 400 | -0.48px | 880px | left |

### Services

URL: https://www.weareverbatim.com/services

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Service page heading | h1 | Hagrid Text Var Variable Regular | 64px | 57.6px | 400 | -1.28px | 864px | center |
| Service heading | h2 | Hagrid Text Var Variable Regular | 60px | 72px | 400 | -1.2px | 432px | start |
| Service introduction | p | Bricolage Grotesque | 36px | 39.6px | 300 | normal | 442px | start |
| Process heading | h3 | Hagrid Text Var Variable Regular | 48px | 57.6px | 400 | -0.96px | 496px | start |
| Process paragraph | p | Bricolage Grotesque | 18px | 23.4px | 300 | normal | 496px | start |
| Testimonial paragraph | p | Bricolage Grotesque | 17px | 22.1px | 400 | -0.34px | 376px | start |

Type scale interpretation: Display sizes include 32, 56, 60, 80, 92, and 180px. The large jumps and closely spaced variants suggest composition-specific choices rather than one demonstrated modular ratio.

### CSS evidence notes

The matched Framer hero preset declares `--framer-font-size: 92px`, with 68px at widths 810–1199px and 40px at widths up to 809px. It also declares `--framer-font-variation-axes: "wght" 1000`. A direct computed h1 check confirmed `font-variation-settings: "wght" 1000` alongside `font-weight: 400`. Preserve both facts; the weight column alone is insufficient.

Source: page inline styles and matched presets.

### Font availability sources

- Hagrid Text Var: Paid commercial license. https://www.zetafonts.com/hagrid · https://www.zetafonts.com/licensing
- Bricolage Grotesque: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Bricolage+Grotesque · https://github.com/google/fonts/blob/main/ofl/bricolagegrotesque/OFL.txt
- Hagrid Heavy: Paid commercial font. https://www.zetafonts.com/hagrid

## Bart Stefanski

Bart Stefanski’s portfolio presents software projects, technical writing, and experience so visitors can assess his work and find relevant examples.

### Homepage

URL: https://www.bstefanski.com/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | Oxygen | 43.616px | 47.1053px | 700 | -1.30848px | 552px | start |
| Hero heading light phrase | span | Oxygen | 43.616px | 47.1053px | 400 | -1.30848px | 144px | start |
| Navigation label | a | Oxygen Mono | 12.5px | 19.375px | 400 | -0.075px | 63px | start |
| Section index | div | Oxygen Mono | 11.5px | 17.825px | 400 | 0.92px | 743px | start |
| Availability label | span | Oxygen Mono | 11px | 17.05px | 400 | -0.075px | 157px | start |
| Clock statistic | div | Oxygen Mono | 30px | 46.5px | 400 | -0.6px | 343px | start |
| Experience statistic | div | Oxygen Mono | 42px | 42px | 400 | -1.26px | 343px | start |
| Project heading | div | Oxygen | 20px | 24px | 700 | -0.3px | 343px | start |
| Project description | div | Oxygen | 13px | 19.5px | 400 | -0.075px | 343px | start |
| Article list title | span | Oxygen | 14px | 21.7px | 400 | -0.075px | 627px | start |
| Tools heading | h2 | Oxygen Mono | 12px | 18.6px | 400 | 1.2px | 343px | start |
| Footer legal text | span | Oxygen Mono | 11.5px | 17.825px | 400 | -0.075px | 369px | start |

### Technical article

URL: https://www.bstefanski.com/blog/cloudflare-next-invalid-alias

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Article heading | h1 | Oxygen | 48px | 51.84px | 700 | -1.344px | 860px | start |
| Article paragraph | p | Oxygen | 16.5px | 28.875px | 400 | -0.075px | 632px | start |
| Code sample | span | Oxygen Mono | 11.44px | 18.304px | 400 | -0.075px | 590px | start |
| Article date | span | Oxygen Mono | 12px | 18.6px | 400 | -0.075px | 86px | start |
| Next article link | a | Oxygen | 14px | 21.7px | 400 | -0.075px | 203px | right |

### Project listings

URL: https://www.bstefanski.com/projects

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

Miniature product mockups are excluded from the portfolio typography guide.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Listing heading | h1 | Oxygen | 56px | 58.8px | 700 | -1.68px | 624px | start |
| Listing introduction | p | Oxygen | 16px | 24.8px | 400 | -0.075px | 504px | start |
| Featured project heading | h2 | Oxygen | 30px | 33px | 700 | -0.6px | 449px | start |
| Featured project description | p | Oxygen | 15px | 24px | 400 | -0.075px | 449px | start |
| Project card heading | h3 | Oxygen | 16px | 24.8px | 700 | -0.16px | 539px | start |
| Project card description | p | Oxygen | 13.5px | 20.25px | 400 | -0.075px | 539px | start |
| Category label | span | Oxygen Mono | 10.5px | 16.275px | 400 | 0.84px | 93px | start |

Type scale interpretation: The homepage mixes a fluid heading with fixed card and metadata sizes. Comparing 20, 30, 42, and approximately 43.62px treatments does not support one repeated modular ratio; the roles serve different compositions.

### CSS evidence notes

The homepage introduction rule declares `font-size: clamp(30px, 3.2vw, 44px)`, `line-height: 1.08`, and `letter-spacing: -0.03em`, consistent with the observed 43.616px size. A separate max-width 980px declaration uses `clamp(28px, 8vw, 40px)`; final cascade behavior at that width was not rendered. The Google Fonts stylesheet was inaccessible via CSSOM.

Inspected stylesheet sources:
- https://www.bstefanski.com/_astro/Base.Clyu4QMj.css
- https://www.bstefanski.com/_astro/index@_@astro.D6y6w4Gb.css

### Font availability sources

- Oxygen: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Oxygen · https://github.com/google/fonts/blob/main/ofl/oxygen/OFL.txt
- Oxygen Mono: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Oxygen+Mono · https://github.com/google/fonts/blob/main/ofl/oxygenmono/OFL.txt

## Code Metal

Code Metal explains software translation and verification tools, publishes technical research, and helps teams evaluate the product or contact sales.

### Homepage

URL: https://www.codemetal.ai/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | DM Sans | 109.04px | 88.3224px | 500 | -4.3616px | 1225px | center |
| Hero description | p | DM Sans | 20px | 24px | 300 | 0.6px | 544px | center |
| Navigation label | a | DM Mono | 14px | 14px | 400 | 0.35px | 94px | start |
| Action label | a | DM Mono | 14px | 14px | 400 | 0.42px | 157px | center |
| Section heading | h2 | DM Sans | 64px | 57.6px | 500 | -3.2px | 1280px | start |
| Platform heading | h2 | DM Sans | 48px | 48.96px | 400 | -0.96px | 640px | start |
| Platform description | p | DM Sans | 18px | 27px | 400 | normal | 544px | start |
| Feature description | p | DM Sans | 15px | 22.5px | 400 | normal | 306px | left |
| Feature heading | h3 | DM Sans | 18px | 24.75px | 600 | normal | 224px | start |
| Research section heading | h2 | DM Sans | 44px | 47.52px | 400 | -0.88px | 409px | start |
| Featured article heading | h2 | DM Sans | 40px | 42px | 600 | -0.4px | 391px | start |
| Article metadata | p | DM Mono | 12px | 16px | 400 | normal | 820px | start |
| Footer legal text | p | DM Mono | 13.5px | 18px | 400 | normal | 367px | start |
| Footer navigation | a | DM Mono | 14px | 30px | 400 | normal | 67px | start |

### Research article

URL: https://www.codemetal.ai/research/apples-to-apples-getting-type-mappings-right-in-llm-based-code-translation

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Article heading | h1 | DM Sans | 64px | 57.6px | 500 | -3.2px | 704px | start |
| Article introduction | p | DM Sans | 20px | 24px | 300 | 0.6px | 704px | start |
| Author metadata | p | DM Sans | 14px | 19.6px | 400 | 0.56px | 704px | start |
| Article section heading | h2 | DM Sans | 20px | 24px | 700 | -0.4px | 704px | start |
| Article paragraph | p | DM Sans | 18px | 27px | 400 | 0.18px | 704px | start |
| Code sample | span | DM Mono | 14px | 21px | 400 | 0.42px | 35px | left |

### Product

URL: https://www.codemetal.ai/product

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Product heading | h1 | DM Sans | 64px | 57.6px | 500 | -3.2px | 672px | start |
| Product description | p | DM Sans | 20px | 24px | 300 | 0.6px | 540px | start |
| Step heading | h2 | DM Sans | 44px | 44px | 500 | -0.88px | 321px | start |
| Page label | p | DM Mono | 14px | 14px | 400 | 0.42px | 106px | start |

Type scale interpretation: The homepage heading set includes 20, 24, 40, 44, 48, 64, and approximately 109.04px. CSS confirms fluid display sizing, so ratios at this viewport do not establish a universal modular scale.

### CSS evidence notes

The root defines `--text-h1: clamp(3.5rem,8vw,7rem)`, line height `.81`, letter spacing `-.04em`, and font weight `500`; `.text-h1` consumes those properties. At 1363px width, 8vw is 109.04px, matching the sample. `--text-h2` uses `clamp(2.5rem,5vw,4rem)`. Additional matched media rules use min-width 48rem. These are source declarations; mobile and tablet appearance remain unverified.

Inspected stylesheet sources:
- https://www.codemetal.ai/_next/static/immutable/chunks/2f3qrdcudbce6.css

### Font availability sources

- DM Sans: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/DM+Sans · https://github.com/google/fonts/blob/main/ofl/dmsans/OFL.txt
- DM Mono: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/DM+Mono · https://github.com/google/fonts/blob/main/ofl/dmmono/OFL.txt

## Jerry Seinfeld

Jerry Seinfeld’s website helps visitors find tour dates, browse film, television, and books, and reach viewing or ticket links.

### Welcome section

URL: https://jerryseinfeld.com/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

One scrolling document; the following samples are sections, not separate page templates.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Welcome heading | h1 | FuturaBT-CondExtraBlack | 45.4775px | 45.4775px | 400 | normal | 364px | start |
| Welcome paragraph | p | FuturaBTWXX-Medium | 25.9871px | 35.0826px | 400 | normal | 364px | start |
| Signature text | p | FuturaBT-CondExtraBlack | 25.9871px | 35.0826px | 400 | normal | 364px | start |
| Navigation label | a | FuturaBT-CondExtraBlack | 17.6712px | 17.6712px | 400 | normal | 125px | start |
| Footer legal link | a | FuturaBTWXX-Medium | 12.9936px | 12.9936px | 400 | normal | 78px | start |

### Tour listing section

URL: https://jerryseinfeld.com/#tour-dates

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Event date | div | FuturaBTWXX-Medium | 20.7897px | 33.2635px | 400 | normal | 141px | start |
| Event time | div | FuturaBTWXX-Medium | 14.5528px | 17.4633px | 400 | normal | 141px | start |
| Event location | div | FuturaBT-CondExtraBlack | 20.7897px | 16.6318px | 400 | normal | 352px | start |
| Event venue | div | FuturaBTWXX-Medium | 18.191px | 29.1056px | 400 | normal | 352px | start |
| Ticket action | a | FuturaBT-CondExtraBlack | 20.7897px | 20.7897px | 400 | normal | 97px | right |

### Work section

URL: https://jerryseinfeld.com/#work

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

Work descriptions substitute for a separate long-form page; no distinct article template was observed.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Work category heading | h2 | FuturaBTWXX-Medium | 31.1845px | 31.1845px | 700 | normal | 325px | start |
| Work title | a | FuturaBT-CondExtraBlack | 19.4903px | 23.3884px | 400 | normal | 325px | start |
| Work description | p | FuturaBTWXX-Medium | 15.5923px | 21.0496px | 400 | normal | 368px | start |

Type scale interpretation: Sizes are influenced by vmin-based CSS, including the Welcome heading and paragraph. Their ratios describe this viewport only; the sample does not establish one fixed modular scale.

### CSS evidence notes

`h1` declares `font-size: calc(28px + 1.86725vmin)`. `p.lead` declares `calc(16px + 1.067vmin)`. At a 936px shorter viewport dimension, these yield approximately 45.48px and 25.99px, matching the samples. Navigation changes its rem-based size at min-width 1024px; other paragraph rules occur at min-width 768px.

Inspected stylesheet sources:
- https://jerryseinfeld.com/css/jerry.css?id=566f3ec96c0073ace4b5

### Font availability sources

- Futura BT condensed display and medium: Paid commercial license. https://www.myfonts.com/collections/futura-bt-font-bitstream · https://www.myfonts.com/collections/futura-bt-font-bitstream?tab=licensing

## CHEW

CHEW presents food innovation and commercialisation services, its working process, and selected outcomes so potential partners can assess the company and make contact.

### Homepage and service sections

URL: https://www.chewinnovation.com/

Status: desktop sampled; responsive coverage partial. Actual viewport: 1363 × 936 CSS px.

One scrolling document. How we work and The receipts supply service and case-study content; they are not separate pages.

| Role | HTML | Font family | Font size | Line height | Font weight | Letter spacing | Text box width | Alignment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Hero heading | h1 | ChewProtest | 129.485px | 113.947px | 700 | -1.29485px | 752px | start |
| Hero description | p | Space Grotesk | 16px | 28px | 400 | normal | 410px | start |
| Hero introductory label | p | Space Grotesk | 14px | 20.3px | 700 | 3.36px | 752px | start |
| Navigation label | a | Space Grotesk | 14px | 23.8px | 400 | 2.24px | 90px | start |
| Action label | a | Space Grotesk | 13px | 22.1px | 700 | 1.82px | 157px | start |
| Statistic | div | PP Mori | 54.52px | 51.794px | 700 | -2.1808px | 272px | start |
| Statistic label | div | Space Grotesk | 12px | 17.4px | 700 | 1.68px | 272px | start |
| Reformation heading | div | PP Mori | 38.164px | 41.9804px | 600 | -0.76328px | 346px | start |
| Reformation paragraph | div | Space Grotesk | 16px | 28px | 400 | normal | 346px | start |
| Service section heading | h2 | ChewProtest | 163.56px | 143.933px | 700 | -1.6356px | 1244px | center |
| Process heading | h3 | ChewProtest | 81.78px | 75.2376px | 700 | -0.8178px | 1100px | start |
| Capability heading | div | PP Mori | 26px | 31.2px | 600 | -0.52px | 574px | start |
| Client introduction | p | Space Grotesk | 16px | 28.8px | 400 | normal | 720px | start |
| Case statistic | div | PP Mori | 34.075px | 34.075px | 700 | -1.363px | 171px | start |
| Footer legal text | p | Space Grotesk | 12px | 20.4px | 400 | 0.48px | 256px | right |

Type scale interpretation: The heading sizes are fluid and role-specific. The sampled 26, 38.16, 81.78, 129.49, and 163.56px treatments do not establish a single repeated modular ratio.

### CSS evidence notes

`.hero-hed` declares `clamp(60px, 9.5vw, 138px)`, line height `.88`, and letter spacing `-.01em`. At max-width 640px it declares `clamp(54px, 18vw, 86px)`. `.how-work-title` declares `clamp(70px, 12vw, 172px)` with a distinct max-width 640px formula. `.stat-n` declares PP Mori with `clamp(36px, 4vw, 60px)`. Navigation rules also change at max-width 960px.

Inspected stylesheet sources:
- https://www.chewinnovation.com/style.css

### Font availability sources

- ChewProtest: License unverified. https://www.chewinnovation.com/
- Space Grotesk: Free for commercial use · SIL OFL 1.1. https://fonts.google.com/specimen/Space+Grotesk · https://github.com/google/fonts/blob/main/ofl/spacegrotesk/OFL.txt
- PP Mori: Paid commercial font. https://pangrampangram.com/products/mori · https://pangrampangram.com/pages/faq

## Changes to the gallery

The six main sections now use the approved guide structure. Page-grouped tables split font size and line height, include font family and stable role anchors, and show element/text-box details. Commentary links return focus to the referenced row within the open dialog. Detailed licensing follows the main analysis. Original captures remain in a dated disclosure. Availability filters still require every documented primary family to qualify; new font findings expand the inventory without silently counting unknown families as free.

## Remaining work

- Render the agreed mobile, tablet, and desktop target dimensions in a browser that supports resizing. Retain this partial desktop run as evidence rather than overwriting it with predicted CSS values.
- Recheck wrapping, hidden/replaced roles, small-text reading conditions, and extra transition widths only where meaningful.
- Consider the optional public CSS implementation section and a dedicated footer-linked methodology page separately; neither is added by this review.
- Explore the availability labels using the existing README TODO, changing one useful variable at a time.
