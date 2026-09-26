# 00 · Foundations: Rules That Apply to Every Category

A category changes a site's *personality*. It doesn't change the rules below. A neubrutalist site and a government site both have to pass these. Where a category pushes against a rule, its own guide says how to handle it.

---

## 1. Process: strategy before style

1. **Define the main job.** What single action or feeling counts as success: sign up, book, read, buy, trust, remember?
2. **Know the audience's context.** Device mix, how skilled they are online, how much stress they're under (paying tax vs. browsing trainers), and accessibility needs.
3. **Choose the category** (see [README](./README.md#picking-a-category)). Then set your *expression level* within it: 1 = conservative, 5 = award-chasing.
4. **Content first.** Write the real headline, proof and calls to action before making visuals. Every category's "look" falls apart on lorem ipsum.
5. **Tokens next, then components, then pages.** Set type, color, spacing, radius, shadow and motion tokens before drawing any screens.
6. **Test with real people and real devices,** including a mid-range Android phone on a slow 4G connection.

## 2. Layout and grid

- **Columns:** 12 columns on desktop, 8 on tablet, 4 on mobile. Every 12-column grid on the web descends from the Swiss International Typographic Style.
- **Content width:** 1200–1440px max container. Reading text is capped by *measure*, not container width.
- **Measure:** 45–75 characters per line; `max-width: 65ch` is a sensible default for body text.
- **Spacing scale:** base unit 8px, with 4px for tight spots (icon + label).
  `4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96 · 128 · 160`
  - 4px: tight coupling (icon + label)
  - 8px: related items
  - 16px: standard gap
  - 24–32px: separating groups
  - 48–64px: inside sections
  - 96–160px: between sections (luxury and editorial sit at the top of this range)
- **Proximity signals relationship.** Keep things that belong together closer to each other than to their neighbors.
- **Breakpoints:** design mobile-first. Prefer container queries for components and use a few layout breakpoints: ~480, 768, 1024, 1280, 1536.

## 3. Typography

- **Modular scale.** Pick one ratio:
  - 1.2 (minor third): dense UI, Institutional
  - 1.25 (major third): general use
  - 1.333 (perfect fourth): Editorial, Tech marketing
  - 1.5+ (perfect fifth): Bold, Luxury display
- **Fluid sizes with `clamp()`:**
  ```css
  --step-0: clamp(1rem, 0.95rem + 0.25vw, 1.125rem);   /* body 16→18 */
  --step-1: clamp(1.25rem, 1.15rem + 0.5vw, 1.5rem);
  --step-2: clamp(1.56rem, 1.4rem + 0.8vw, 2rem);
  --step-3: clamp(1.95rem, 1.7rem + 1.25vw, 2.75rem);
  --step-4: clamp(2.44rem, 2rem + 2.2vw, 3.75rem);
  --step-5: clamp(3.05rem, 2.4rem + 3.3vw, 5.5rem);    /* display */
  ```
- **Body text:** at least 16px, ideally 17–20px on desktop. Line-height 1.5–1.7 for body, 1.05–1.2 for display.
- **Two families at most** (plus mono if needed). Use **variable fonts**; by 2026 they're the default expectation. Load them with `font-display: swap`, subset them, and preload only the hero weight.
- **Tracking:** tighten large display type (−1% to −3%). Loosen small all-caps labels (+4% to +12%).
- **Personality lives in type.** Several 2026 critiques say that swapping Inter for a typeface with character is the fastest way to stop looking generic or AI-made.

## 4. Color

- **Build scales, not single swatches:** 9–11 steps per hue (50→950), and 8–10 greys, because most of any UI is grey.
- **Name tokens by role, not by value:** `--color-bg`, `--color-surface`, `--color-text`, `--color-text-muted`, `--color-accent`, `--color-border`, `--color-success/warning/danger`.
- **Define colors in OKLCH** so lightness stays even across hues and dark mode can be generated reliably.
- **60/30/10:** roughly 60% dominant neutral, 30% secondary, 10% accent. Bold Expressive deliberately breaks this.
- **Contrast (WCAG 2.2 AA):** 4.5:1 for body text, 3:1 for large text (≥24px, or ≥18.66px bold), 3:1 for UI component boundaries and focus indicators.
- **Color is never the only signal.** Pair it with an icon, text or pattern.
- **Dark mode:** design it from the start. Use elevated surfaces that get *lighter* as they rise, not shadows. Avoid pure `#000` behind long text, and lower the saturation of accents.

## 5. Accessibility (WCAG 2.2 AA minimum)

| Requirement | Practical rule |
|---|---|
| Contrast | Text 4.5:1 (large 3:1); non-text UI 3:1 |
| Target size (2.5.8) | Interactive targets ≥ 24×24 CSS px, or enough spacing around them; aim for 44×44 on touch |
| Focus visible / appearance | Visible focus ring ≥ 2px, 3:1 contrast against both the unfocused state and the surroundings |
| Focus not obscured (2.4.11) | Sticky headers, cookie banners and chat widgets must not cover the focused element |
| Dragging (2.5.7) | Anything done by dragging also has a single-pointer alternative (buttons) |
| Consistent help (3.2.6) | Help and contact appear in the same place on every page |
| Redundant entry / accessible auth | Don't ask for the same data twice; no cognitive-test logins |
| Motion | Honor `prefers-reduced-motion`; nothing flashes more than 3 times per second; autoplay can be paused |
| Semantics | Real `<button>`, `<a>`, headings in order, landmarks, labels on inputs, alt text |
| Transparency | Honor `prefers-reduced-transparency`; glass needs a solid fallback |

The GOV.UK principle applies to everyone: *accessible design is good design*, and using a design system doesn't make a service accessible by itself. You still need to test.

## 6. Performance (Core Web Vitals, judged at the 75th percentile of real users)

| Metric | Good | Needs work | Poor |
|---|---|---|---|
| LCP (loading) | ≤ 2.5s | 2.5–4s | > 4s |
| INP (responsiveness) | ≤ 200ms | 200–500ms | > 500ms |
| CLS (visual stability) | ≤ 0.1 | 0.1–0.25 | > 0.25 |

Rules of thumb:
- Hero image in AVIF/WebP with `fetchpriority="high"`, and never lazy-loaded.
- Set explicit `width`/`height` or `aspect-ratio` on all media.
- Budget: ≤ 170KB of JavaScript for a content page before the immersive layer; ≤ 100KB of fonts.
- Animate only `transform` and `opacity`. Scroll-driven CSS animations on those properties run off the main thread.

## 7. Motion

- **Purpose first:** motion should *guide attention*, *show a change of state* or *express the brand*. The 2026 kinetic-type trend is described as "less spectacle, more directing attention".
- **Durations:** micro 100–200ms, UI 200–300ms, entrances 300–600ms, cinematic 600–1200ms.
- **Easing:** `cubic-bezier(0.2, 0, 0, 1)` (fast out, slow in) for entrances; springs for playful brands.
- **Native first:** CSS scroll-driven animations (`animation-timeline: view()`) and the View Transitions API are now widely supported. Use GSAP or Framer Motion only when native CSS can't do it.
- **Build the finished state first:** content must look right with all animation stripped out. Then add motion inside `@media (prefers-reduced-motion: no-preference)`.

## 8. Imagery

- Real photography of real products and people beats stock photos in every category.
- Give every image one crop per breakpoint (`<picture>`), not just a smaller copy.
- Keep a consistent treatment (grade, grain, crop ratio, illustration style). Consistency makes images look like a brand.

## 9. Content and conversion basics

- A visitor should understand the value proposition in about **5 seconds**.
- **One main call to action per view,** with at most one secondary.
- **Proof near the claim.** Put logos, numbers, quotes and certifications next to what they back up, not in a separate testimonials area.
- **Navigation:** 5–7 top-level items, with labels in the user's words, not company org-chart terms.
- **Forms:** as few fields as possible, labels above inputs, inline validation, and error messages that say how to fix the problem.

## 10. Avoiding the "generic" look

Automated builders and AI tools have made a default template very common: centered hero, Inter, purple gradient, three icon cards, fade-in on everything. To avoid it:
- Choose a typeface with character (see each category).
- Commit to *one* signature device: a color, a shape, a layout break, a motion idea or an illustration style. Use it consistently.
- Use real product, people and place imagery.
- Design components specific to the brand (stat callouts, quote cards, comparison tables) instead of generic cards.
- Give motion a reason, and vary it by context, not a blanket fade-up.
- Write in a specific voice. Generic copy makes a generic design.
