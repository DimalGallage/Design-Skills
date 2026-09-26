# The Six Categories of Modern Web Design

A research-based field guide that sorts the world's websites into **six style categories**, plus one **experiential layer** that can be added on top of any of them. For each category it covers what makes it different, which industries and use cases it fits (and which it doesn't), its visual traits, and a complete build guide.

> Research basis: design-trend reports for 2025–2026 (Figma, Wix, Elementor, Envato, GoDaddy), UX research (Nielsen Norman Group, Baymard Institute), standards bodies (W3C WCAG 2.2, Google Core Web Vitals, GOV.UK Design System), and many agency and practitioner write-ups. Full list in [`sources.md`](./sources.md).

---

## Why six categories?

Most "web design styles" lists name 9 to 67 aesthetics: minimalism, Swiss, flat, bento, brutalism, neubrutalism, glassmorphism, Y2K, editorial, retro, hand-drawn, and so on. Those are **surface treatments**. Many of them do the same *job* for the same *kind of business*, so they group together.

This guide groups on the two things that actually drive design decisions:

1. **The site's main job.** Is it there to *show a product*, *reassure*, *be read*, *create desire*, *build a relationship*, or *get attention*?
2. **How loud it's allowed to be.** Low-expression sites put clarity first. High-expression sites put memorability first.

Plot styles on those two axes and six stable clusters appear. They hold up across the 2026 trend reports: Envato and Vikilinks group styles into "clean & systematic", "bold & expressive" and "nostalgic & human" families. LogRocket and Striped Horse describe SaaS splitting into "techno-futurist" and "editorial". Luxury write-ups agree on "quiet restraint". Immersive WebGL work now leads the award sites.

```
                     ◄──── clarity first ─────────── memorability first ────►

 show a product         1. PRODUCT-LED TECH
 reassure               2. INSTITUTIONAL TRUST
 be read                3. EDITORIAL
 create desire                              4. QUIET LUXURY
 build a relationship                       5. ORGANIC & HUMAN
 get attention                                                  6. BOLD EXPRESSIVE

                     ─── + optional IMMERSIVE LAYER (WebGL / 3D / scroll story) ──►
                         most often added on top of 1, 4 and 6
```

## The six categories at a glance

| # | Category | Main job | It feels… | Typical industries | Style families it includes |
|---|---|---|---|---|---|
| 1 | [**Product-Led Tech**](./categories/01-product-led-tech.md) | Show the product and turn visitors into sign-ups | Precise, fast, confident | SaaS, dev tools, AI, fintech, crypto/infra, B2B platforms | "Linear style", Stripe-style gradients, bento grids, dark mode, subtle glass |
| 2 | [**Institutional Trust**](./categories/02-institutional-trust.md) | Reassure people and help them finish tasks | Calm, orderly, credible | Banking, insurance, healthcare, government, legal, enterprise, universities, utilities | Swiss / International Typographic Style, flat design, design-system UI |
| 3 | [**Editorial**](./categories/03-editorial.md) | Get people to read and come back | Intelligent, authored, rhythmic | News, magazines, publishers, blogs/newsletters, museums, think tanks, documentation | Magazine layouts, serif revival, typographic minimalism |
| 4 | [**Quiet Luxury**](./categories/04-quiet-luxury.md) | Create desire and signal status | Restrained, slow, precious | Fashion, jewellery, watches, premium beauty, luxury hotels, real estate, architecture, high-end automotive | Luxury minimalism, gallery layouts, monochrome, cinematic photography |
| 5 | [**Organic & Human**](./categories/05-organic-human.md) | Build warmth and a relationship | Warm, approachable, honest | Wellness, food & beverage, restaurants, sustainable/eco brands, nonprofits, family and consumer health, education, local business | Neo-naturalism, biophilic, hand-drawn, soft retro, textured |
| 6 | [**Bold Expressive**](./categories/06-bold-expressive.md) | Get noticed and remembered | Loud, playful, rebellious | Consumer startups, Gen-Z D2C brands, creative agencies, portfolios, music, events, gaming, campaigns | Neubrutalism, brutalism, maximalism, Y2K / dopamine, anti-design, kinetic type, collage |
| + | [**Immersive Layer**](./categories/07-immersive-layer.md) | Tell a story as an experience | Cinematic, spatial | Product launches, automotive, luxury campaigns, entertainment, games, agency showcases, museums | WebGL/Three.js, 3D product views, scroll-driven narratives |

## How the categories differ from each other

The same design decision, answered six ways:

| Decision | 1 Product-Led Tech | 2 Institutional Trust | 3 Editorial | 4 Quiet Luxury | 5 Organic & Human | 6 Bold Expressive |
|---|---|---|---|---|---|---|
| **Hero** | Headline + real product UI | Plain statement + top tasks / search | Lead story or issue cover | Full-bleed photograph or film, very few words | Warm lifestyle photo or illustration + friendly promise | Huge type, loud color, unusual shapes |
| **Typeface** | Tight geometric/grotesk sans, mono accents | Neutral, very legible sans (system or humanist) | Serif display + serif or sans body | Thin didone/high-contrast serif or wide-spaced sans | Soft serif or rounded sans, optional handwritten accent | Heavy display, mono, variable or custom |
| **Color** | Near-black or white + one vivid accent / gradient | Brand blue/green + deep neutrals; color carries meaning | Paper white/cream + ink; small accent | Black, white, stone, cream; no loud accents | Earth tones: clay, sage, sand, terracotta | Saturated primaries, neons, clashing pairs |
| **Density** | Medium; modular bento | Medium-high, well organized | High but rhythmic | Very low; 2–3× the usual whitespace | Low-medium, airy | Varies; often dense and collage-like |
| **Shape language** | 8–16px radius, 1px hairline borders, glow | 4–8px radius, clear borders | Rules and columns; almost no radius | Sharp or 0 radius, thin rules | Big radii, blobs, arches, hand-drawn edges | 2–4px black borders, hard offset shadows |
| **Motion** | Crisp micro-interactions, product demos | Minimal and functional only | Minimal; reading progress | Slow fades and reveals, 600–1200ms | Gentle, springy, delightful | Snappy, bouncy, kinetic type, marquees |
| **Proof / trust** | Logos, metrics, dev quotes, docs | Accreditations, compliance, contact details, plain language | Bylines, dates, sources, corrections | Heritage, craftsmanship, store locator, press | Faces, founders, reviews, certifications (B-Corp, organic) | Community, UGC, attitude |
| **Biggest risk** | Looking like every other SaaS | Looking dull or bureaucratic | Walls of text, ad clutter | Style over usability (hidden nav, low contrast) | Twee or unfocused, low contrast | Failing accessibility; tiring the user |

## Picking a category

1. **Is getting a task done (apply, pay, book, claim) the main purpose, and are the stakes high (money, health, law)?** → **2 Institutional Trust**. A regulated or high-stakes audience should never be the place to experiment.
2. **Is the product itself software people must understand before buying?** → **1 Product-Led Tech**.
3. **Is content (articles, research, docs) the product?** → **3 Editorial**.
4. **Is the price premium and the purchase driven by emotion and status?** → **4 Quiet Luxury**.
5. **Does trust come from warmth, care and values rather than authority?** → **5 Organic & Human**.
6. **Is standing out in a crowded, young or creative market worth more than looking conventional?** → **6 Bold Expressive**.
7. **Is there a launch, flagship product or story that people will spend minutes with, and a budget for it?** → Add the **Immersive Layer** to the category you picked.

**Mixing categories.** Real brands often combine two, but one should lead. Common, working pairs:
- *Tech + Editorial:* "cream + serif" AI and SaaS sites.
- *Luxury + Immersive:* Cartier-style WebGL campaigns.
- *Organic + Editorial:* food magazines, slow-living brands.
- *Institutional + Organic:* consumer healthcare and patient-facing clinics.
- *Bold + Tech:* developer tools that want attitude, such as the neubrutalist Gumroad and Figma marketing phases.

Pairs that tend to fail: Institutional + Bold for regulated flows, and Luxury + Bold (loudness cheapens luxury, except in deliberate streetwear/hype collaborations).

## Standards every category must meet

The six categories change the *look*. They don't change these rules. See [`00-foundations.md`](./00-foundations.md) for the full list:

- **Accessibility:** WCAG 2.2 AA. That means 4.5:1 text contrast, 3:1 for UI elements and focus rings, 24×24px minimum targets, visible focus that isn't hidden behind sticky headers, and support for `prefers-reduced-motion`.
- **Performance:** Core Web Vitals "good" at the 75th percentile: LCP ≤ 2.5s, INP ≤ 200ms, CLS ≤ 0.1.
- **Systems:** spacing scale on a 4/8px base, a modular fluid type scale using `clamp()`, 45–75 character line length, and design tokens for everything.

## Files

```
web-design-guide/
├── README.md                       ← you are here: taxonomy, comparison, picking a category
├── SKILL.md                        ← short version for AI agents / Claude skills
├── 00-foundations.md               ← rules that apply to every category
├── categories/
│   ├── 01-product-led-tech.md
│   ├── 02-institutional-trust.md
│   ├── 03-editorial.md
│   ├── 04-quiet-luxury.md
│   ├── 05-organic-human.md
│   ├── 06-bold-expressive.md
│   └── 07-immersive-layer.md
└── sources.md                      ← research bibliography
```

Every category file uses the same outline, so you can compare them side by side:

1. Essence 2. How it differs 3. Where to use it / avoid it 4. Signature traits 5. Design tokens (type, color, space, shape, depth, motion, imagery) 6. Page anatomy, section by section 7. Components 8. Copy and voice 9. Accessibility and performance pitfalls 10. Sub-styles 11. Reference sites 12. Starter CSS tokens 13. Launch checklist
