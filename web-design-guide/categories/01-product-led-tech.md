# 1 · Product-Led Tech

> **Main job:** show the product working, then turn understanding into a sign-up.
> **Feels:** precise, fast, engineered, confident.
> **Expression level:** 2–4 of 5.

## 1. Essence

The product *is* the hero. These sites exist to answer "what does it do, is it good, and can I trust it with my workflow?" as quickly as possible, usually by showing real UI rather than describing it. The look comes from the software itself: tight grids, hairline borders, crisp type, restrained color, with one expressive moment such as a gradient, a glow or a shader.

In 2026 the category has two main dialects:
- **Techno-futurist / "Linear style":** near-black canvas, gradations of white opacity, subtle gradients and glow, bento grids, micro-motion. Named after Linear.app; it has topped SaaS design roundups since 2024.
- **Editorial-tech:** cream or off-white background, a serif display face, generous whitespace, sometimes illustrated mascots. Used to look more human and less "crypto-dark". (It borrows heavily from Category 3.)

## 2. How it differs from the other categories

| vs. | Difference |
|---|---|
| Institutional Trust | Both are orderly, but Tech sells *capability and speed* to people who evaluate themselves; Institutional sells *safety* to people who need reassurance. Tech tolerates dark mode, gradients and jargon; Institutional doesn't. |
| Editorial | Editorial's product is prose. Tech's product is an interface, so screenshots, demos and code replace articles. |
| Quiet Luxury | Both use restraint, but Luxury hides information to create desire. Tech shows as much as it can to remove doubt. |
| Bold Expressive | Tech allows *one* expressive element; Bold makes the whole page expressive. |
| Premium Product Minimalism | Premium Product sells an *object* with studio renders, one idea per tile and no logo walls; Tech sells a *workflow* with UI screenshots and dense proof. See [Category 7](./08-premium-product-minimalism.md). |

## 3. Where to use it

**Best for:** B2B and prosumer SaaS · developer tools, APIs, infrastructure, databases · AI products and model platforms · fintech infrastructure (payments, banking-as-a-service) · cybersecurity · analytics/data · productivity apps · hardware with a strong software story · crypto and web3 infrastructure.

**Use cases:** homepage, product and feature pages, pricing, changelog, docs landing, launch pages, integrations directory.

**Avoid or tone down for:** audiences that aren't technical or are anxious (retail banking, patient health, government). Swap dark mode for light and cut the jargon. Consumer lifestyle products usually need more warmth (Category 5) or more personality (Category 6).

## 4. Signature traits

- A **real product screenshot or live demo** above the fold.
- **Bento grids** for features: modular rectangles of different sizes, each showing one capability with a small visual. Practitioner write-ups call it the default SaaS feature pattern in 2026, because people can jump straight to the feature they care about.
- **1px hairline borders** and subtle inner highlights instead of heavy shadows.
- **One signature color moment:** a Stripe-style mesh gradient, a Linear-style glow, or a Vercel-style monochrome with a single accent.
- **Grotesk or geometric sans** with tight tracking at display sizes, and **monospace** for code, labels and metrics.
- **Precise micro-interactions:** hover glows, animated cursors in demos, keyboard shortcut hints (`⌘K`).
- **Logo walls, metrics and developer quotes** as proof; compliance badges (SOC 2, ISO 27001, GDPR) for enterprise.

## 5. Design tokens

### Typography
- **Display:** Inter Display, Geist, Söhne, Suisse Int'l, General Sans, Satoshi, Aeonik, Neue Montreal, or a custom grotesk. Stripe's identity rests on the variable Söhne at *light* weights (300–400) with a stylistic set, which proves weight and features can carry identity.
- **Editorial-tech dialect:** a serif display (Instrument Serif, Fraunces, GT Super, Tiempos Headline) paired with a clean sans body.
- **Mono:** Geist Mono, JetBrains Mono, Berkeley Mono, IBM Plex Mono.
- **Scale:** 1.25–1.333. Hero 56–88px, tracking −2% to −4%, line-height 1.0–1.1.
- **Body:** 16–18px, muted grey (e.g., 60–70% white on dark), with 65ch measure for longer text.

### Color
- **Dark dialect:** background `#08090A`–`#0F1011`; surfaces raised by +2–4% lightness; text uses white at 90/65/45% opacity for primary/secondary/tertiary; one accent (violet, electric blue, lime or orange) plus gradients built from it.
- **Light dialect:** white or `#FAFAF9`; near-black text `#0A0A0A`; greys from a cool or neutral scale; the accent is used sparingly on calls to action and links. Stripe's palette is vibrant but very disciplined: accents appear only to draw the eye to interactive elements.
- **Gradients:** always *inside* a controlled area (hero backdrop, card border, glow). Never behind body text without a solid plate.

### Spacing and shape
- 8px base. Section padding 96–160px, card padding 24–32px, bento gap 12–24px.
- **Radius:** 8–16px for cards (bento cards commonly 12–24px), 6–8px for buttons, full pill for tags.
- **Borders:** 1px, `rgba(255,255,255,.08)` on dark or `#E5E5E5` on light.

### Depth
- Dark: a layered surface color plus an inner top highlight (`inset 0 1px 0 rgba(255,255,255,.06)`) and faint outer glow.
- Light: soft, layered, low-opacity shadows (`0 1px 2px rgba(0,0,0,.04), 0 8px 24px rgba(0,0,0,.06)`).
- Glassmorphism **only as an accent** (nav bar, floating toolbar) over a controlled background, with a solid fallback. Accessibility researchers warn that translucent panels can pass contrast on one screen and fail on another.

### Motion
- Micro 120–200ms, ease-out. Cursor-follow glows on bento cards. Staggered reveals of product UI. Looping product "movies" made with real UI (Lottie, Rive or HTML/CSS, not heavy video where possible).
- Shaders and WebGL gradients only in the hero, lazy-initialized, with a static poster fallback.

### Imagery
- Product UI screenshots with a consistent frame, crop and zoom level. **Crop to the interesting part**; don't show a whole dashboard shrunk to thumbnail size.
- Abstract 3D or gradient art only as supporting atmosphere.
- Diagrams (architecture, data flow) drawn in the brand's line style.

## 6. Page anatomy (homepage)

1. **Announcement bar (optional):** "New: X is live →". One line.
2. **Nav:** logo · 4–6 items (Product, Solutions, Developers, Pricing, Customers, Docs) · "Log in" · primary CTA. Sticky, often with a blur backdrop.
3. **Hero:** eyebrow tag → 6–10 word headline stating the outcome → one-sentence subhead → primary CTA ("Start free") + secondary ("Book a demo" / "Read docs") → a **large product visual** directly below, or a code snippet for dev tools.
4. **Logo wall:** "Trusted by…" 6–12 monochrome logos.
5. **Value pillars:** 3 outcomes (not features), each backed by one metric.
6. **Bento feature grid:** 5–8 cards, 1–2 large "hero" cells, each with a mini-demo.
7. **Deep-dive sections:** alternating left/right product walkthroughs, or a sticky scrollytelling panel where the UI updates as the text scrolls past.
8. **Integrations:** logo grid or orbit diagram.
9. **Developer/API section** (dev tools): code tabs by language, copy button, link to docs.
10. **Social proof:** quote cards with photo, name, title and company logo; case-study metrics.
11. **Security/enterprise band:** SOC 2, SSO/SAML, uptime, data residency. For regulated buyers a missing security page counts as a disqualifier.
12. **Pricing teaser or final CTA:** restate the headline and repeat the primary CTA.
13. **Footer:** big sitemap, status link, changelog, social links, legal.

**Pricing page:** 3–4 tiers, highlight the recommended one, monthly/annual toggle, feature comparison table with sticky header, FAQ, enterprise "contact sales".

## 7. Key components

Command-palette mock (`⌘K`) · code block with tabs and a copy button · metric tiles · bento card with hover glow · changelog entry · pricing table · comparison ("vs. competitor") table · integration tile · status badge · keyboard shortcut chip (`<kbd>`).

## 8. Copy and voice

Short and specific, written as verbs and outcomes: "Ship faster. Break nothing." Replace adjectives with numbers ("p99 < 50ms"). No marketing padding. Developers distrust it. Put the docs link near the top for technical buyers.

## 9. Pitfalls

- **Everyone looks the same.** Dark background + purple gradient + Inter + bento is now a cliché. Separate yourself through type, a signature color that isn't violet, custom illustration, or the editorial-tech dialect.
- **Low contrast in dark mode.** Tertiary text at 40% white often fails 4.5:1. Check every opacity step.
- **Heavy hero shaders** hurt LCP and INP on mid-range phones. Poster first, WebGL after idle.
- **Screenshots as unreadable thumbnails.** Crop and zoom.
- **Glass without a fallback.** Honor `prefers-reduced-transparency`.

## 10. Sub-styles

| Sub-style | Traits | Examples of the pattern |
|---|---|---|
| Linear / dark minimal | Near-black, glow, white opacity scale, micro-motion | Linear, Raycast, Resend |
| Stripe / gradient precision | Light, WebGL mesh gradient, light-weight type, disciplined accent | Stripe |
| Monochrome dev | Pure black/white, Geist-like type, grid lines, mono | Vercel |
| Editorial-tech | Cream, serif display, illustration | Many AI labs and newer SaaS companies |
| Bento showcase | Feature grid as the main structure | Apple product pages, many 2026 SaaS homepages |

## 11. Starter tokens

```css
:root {
  --bg: oklch(0.99 0 0);          --surface: oklch(0.97 0 0);
  --text: oklch(0.18 0 0);        --text-muted: oklch(0.45 0 0);
  --border: oklch(0.91 0 0);      --accent: oklch(0.58 0.2 265);
  --radius-card: 16px;            --radius-btn: 8px;
  --shadow: 0 1px 2px oklch(0 0 0 / .04), 0 8px 24px oklch(0 0 0 / .06);
  --font-display: "Geist", "Inter", system-ui, sans-serif;
  --font-mono: "Geist Mono", ui-monospace, monospace;
  --ease: cubic-bezier(.2,0,0,1);  --dur: 180ms;
}
:root[data-theme="dark"] {
  --bg: oklch(0.14 0.005 270);    --surface: oklch(0.18 0.005 270);
  --text: oklch(0.96 0 0);        --text-muted: oklch(0.72 0 0); /* check 4.5:1 */
  --border: oklch(1 0 0 / .08);
  --shadow: inset 0 1px 0 oklch(1 0 0 / .06);
}
.bento { display:grid; gap:16px; grid-template-columns:repeat(6,1fr); }
.bento > .lg { grid-column: span 4; } .bento > .sm { grid-column: span 2; }
@media (max-width: 768px){ .bento > * { grid-column: 1 / -1; } }
```

## 12. Launch checklist

- [ ] Real product UI visible in the first viewport
- [ ] Value proposition understood in ~5s; one primary CTA
- [ ] Bento cells each make exactly one point
- [ ] Security/compliance page linked for enterprise buyers
- [ ] Dark-mode text contrast checked at every opacity step
- [ ] Hero shader/gradient has a static fallback; LCP ≤ 2.5s on a mid-range phone
- [ ] Code samples are copyable and keyboard-accessible
- [ ] At least one signature element that is *not* the default SaaS template
