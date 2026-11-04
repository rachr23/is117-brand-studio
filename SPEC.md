# Brand Studio decisions

This is the durable agreement between the learner and agent. Keep it concise and update it only with agreed choices or actual evidence. `Not chosen yet` is a valid status. Persona cards are hypotheses unless supported by real research.

[LEARNING.md](LEARNING.md) holds the short, reviewable record of learner explanations and help received. Keep the brand decisions and implementation evidence here; link rather than duplicate them.

## Current stage

- Stage: Postmodernist visual direction implemented; manual browser review recorded.
- Current feature: BRAND-001 — first branded storefront and live style guide.
- Status: In progress on feature/brand-001.
- Next small decision: Add any learner reflection or revise the slice before the issue and pull request workflow.

## Product boundary

The product is the same white T-shirt throughout the comparison. The baseline offers a size selector and temporary demo bag. No real orders, payment, accounts, or persistence. Keep product facts stable between directions; do not add unsupported claims about materials, manufacturing, sustainability, fit, delivery, scarcity, reviews, or sales.

## Audience hypotheses

The primary need guides the page. Give the secondary card one contrasting need to check that same page; keep both cards brief.

| Tiny card                             | Primary audience                                                                       | Secondary audience                                            |
| ------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| Person in a concrete situation        | Alex, 22, a college student interested in streetwear                                   | Jordan, 20, a budget-conscious college student                |
| Goal or meaning they seek             | Find a white T-shirt with a distinctive silhouette that complements streetwear outfits | Find an affordable, versatile white T-shirt for everyday wear |
| Concern before choosing               | Unsure whether the shirt's fit and proportions will look right                         | Concerned about spending too much on a basic T-shirt          |
| What the page should help them decide | Understand the shirt's fit, sizing, and appearance                                     | Understand the price, sizing, and value                       |
| Evidence or assumption                | Assumption; not validated                                                              | Assumption; not validated                                     |

## Early brand brief

| Decision                                 | Agreement                                                                                                                                      |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Brand name                               | UNFORM                                                                                                                                         |
| One-sentence promise                     | Different by Design: UNFORM challenges conventional clothing silhouettes through minimalist streetwear that emphasizes fit and individuality.  |
| Primary archetype: the brand's character | The Outlaw — independent, unconventional, and rebellious                                                                                       |
| Three voice traits                       | Bold, Minimal, Rebellious                                                                                                                      |
| One example line in this voice           | Less noise. More form.                                                                                                                         |
| Learner's predicted audience effect      | Streetwear enthusiasts will recognize UNFORM as a brand that prioritizes distinctive silhouettes and individuality without excessive graphics. |

## Visual decision

Compare two small hero previews before building the whole page. Hold the product, headline, supporting copy, and action identical. Use specific real design references and annotate visual choices, intended effect, and risk.

A simple original SVG wordmark is enough. Show small-size and one-color presentations; they may use the same asset when it works.

| Item                                              | Agreement or evidence                                                                                                                                                                                                                                                                            |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Shared headline / support / action                | “Different by Design.” / “A plain white T-shirt, reframed for people who choose their own silhouette.” / “Add to demo bag”                                                                                                                                                                       |
| Modernist preview, reference, and annotations     | `public/studio.html`: ordered two-column grid and restrained labels. Reference: [Bauhaus Dessau Building](https://bauhaus-dessau.de/en/architecture/bauhaus-building/) (Walter Gropius, 1926). Intended effect: clear, dependable scanning. Risk: too orderly for the Outlaw voice.              |
| Postmodernist preview, reference, and annotations | `public/studio.html`: layered type, rotated shirt, acid accent, and mixed type cues. Reference: [Memphis Milano official archive](https://memphis.it/it/) (Memphis group founded 1981). Intended effect: individuality and disruption. Risk: asymmetry can slow scanning.                        |
| Chosen direction and reason                       | Postmodernist. I chose this direction because its unconventional layout and bold typography reflect UNFORM's Outlaw archetype and rebellious identity. It helps communicate individuality to my primary audience of streetwear enthusiasts while allowing the white T-shirt to remain the focus. |
| Original SVG logo                                 | Existing `public/assets/wordmark.svg`, used as the UNFORM wordmark                                                                                                                                                                                                                               |
| Monochrome and small-size variants                | Same SVG at header size, style-guide small preview, and flat one-color preview                                                                                                                                                                                                                   |
| Logo review at actual use size                    | Learner manually checked the UNFORM SVG in the navigation and style guide; readable in both.                                                                                                                                                                                                     |
| Shared palette, typography, spacing, and assets   | `public/styles.css` is shared by storefront, style guide, and studio; shared wordmark and white-shirt assets                                                                                                                                                                                     |

## Ethical persuasion

Choose two applications that help the visitor make a voluntary, informed decision. Record their real implementation and mechanism rather than a principle name alone. Required size selection or validation alone does not establish consistency. Do not invent social proof, scarcity, authority, or product facts.

| Principle                  | Actual copy or interaction                                                                                                                 | Visitor benefit / factual support                                                                    |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Reciprocity                | Product color, fictional price, demo sizes, and the explicit “no product claims” boundary are visible before the visitor chooses an action | Helps Alex and Jordan make an informed choice without invented proof                                 |
| Commitment and consistency | After a visitor voluntarily selects a size, the action and live status confirm that exact size in the temporary demo bag                   | Connects a small choice to a clear, reversible classroom interaction; no order or payment is implied |

## BRAND-001 — first branded storefront and live style guide

**Scope:** turn the working neutral storefront into UNFORM's first coherent page. Keep the existing size selector and demo bag usable. Do not add checkout or all future features.

Keep when:

- The learner has chosen the audience hypotheses, brief, visual direction, and logo; the page visibly expresses those choices.
- Two annotated hero directions compare modernist/postmodernist thinking with the same content and real source links.
- The selected SVG logo works at small size and in one color; the presentations may share one asset.
- The storefront and live style guide share CSS variables, typography, components, and assets; they do not drift into separate identities.
- Two ethical persuasion applications are visible and their claims are supportable.
- Prepared checks pass, the agent has reviewed the slice, and the learner has reported desktop/mobile, keyboard, logo, and size-selector observations.
- The issue, branch, commit, and PR explain this feature in the learner's repository; agreed decisions and actual evidence are saved here. The learner has approved keeping and merging the change, and the merge into `main` is verified. Publishing is a separate choice.

## Evidence

Write a short result and link only evidence that exists. A passing browser check is evidence for its assertions, not customer research or proof of full accessibility.

| Spec ID   | Files                                                                                                                                    | Issue / PR      | Actual checks and observations                                                                                                                                                                                                                                                                                                                                                                                                |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BRAND-001 | `public/index.html`, `public/styles.css`, `public/shop.js`, `public/styleguide.html`, `public/studio.html`, `public/assets/wordmark.svg` | Not created yet | `npm.cmd run check` passed: Prettier, ESLint, HTML validation, Stylelint, 7 server tests, and 10 Chromium browser/accessibility/responsive tests. Learner manually observed: desktop storefront passed; mobile storefront passed, readable, and had no horizontal overflow; Tab navigation passed with visible focus indicators; UNFORM logo was readable in navigation and style guide; size selector and Add to Bag worked. |

## Later

No follow-up is selected. After keeping `BRAND-001`, choose one next cycle: perhaps a brand story, a supported fit guide, or richer demo-bag behavior. Agree its scope and add one new spec ID at that time.
