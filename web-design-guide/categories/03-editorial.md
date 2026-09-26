# 3 · Editorial

> **Main job:** get people to read deeply and come back.
> **Feels:** intelligent, authored, rhythmic, cultured.
> **Expression level:** 2–4 of 5.

## 1. Essence

Editorial design brings the craft of print magazines and books to the screen. Typography does almost all the work: dramatic headlines to pull readers in, carefully set body text for long reading, and deliberate pacing across thousands of words. Layout follows a **hierarchy of stories** (lead, secondary, tertiary). Pages feel *authored* rather than templated.

The 2026 **serif revival** has pushed editorial beyond publishers. Serif display faces now appear on SaaS landing pages, e-commerce and even developer docs, because sharp modern screens render serifs well and serifs signal craft and intention at a time of automated sameness.

## 2. How it differs from the other categories

| vs. | Difference |
|---|---|
| Institutional Trust | Both handle lots of text. Institutional wants people to *scan and leave*; Editorial wants them to *stay and read*. Editorial uses serif, drama and asymmetry; Institutional uses neutral sans and predictability. |
| Product-Led Tech | Tech's hero is UI; Editorial's hero is a headline and an image. Editorial-tech borrows Editorial's type and palette but keeps Tech's structure. |
| Quiet Luxury | Both are refined, but Luxury is *sparse* (few words, big images). Editorial is *dense but orderly* (many stories, strong hierarchy). Luxury fashion houses often run an editorial "journal" section that sits between the two. |
| Organic & Human | Organic uses soft shapes and warmth. Editorial uses rules, columns and typographic contrast. |

## 3. Where to use it

**Best for:** newspapers and news sites · magazines (culture, fashion, design, food, travel) · independent publishers and newsletters (Substack/Ghost-style) · personal blogs and essays · museums, galleries, cultural institutions · think tanks, research groups, reports · book publishers · long-form case studies and annual reports · company blogs and "journals" · documentation hubs · brands whose strategy is content marketing.

**Use cases:** article pages, homepages/fronts, section pages, author pages, long-form features, newsletters, research reports.

**Avoid for:** pure transactional flows and apps, or products where the value is visual or interactive rather than written.

## 4. Signature traits

- **Serif typography** for headlines and often body text; sans for navigation, labels and captions.
- **Strong typographic hierarchy:** kicker/section label → headline → standfirst/dek → byline → body.
- **Multi-column, asymmetric grids** on fronts; a **single, narrow reading column** on articles.
- **Rules (hairlines)** separating stories, as in print; almost no rounded cards.
- **Large, well-art-directed photography** with captions and credits.
- **Print devices:** drop caps, pull quotes, footnotes/sidenotes, section numbering, issue numbers.
- **Paper-like palette:** off-white or cream, near-black ink, a single accent (often red, which traditionally marks news urgency).
- **Signals of credibility:** bylines, dates, "updated" stamps, sources, corrections policy.

## 5. Design tokens

### Typography
- **Display serif:** GT Super, Tiempos Headline, Canela, Editorial New, Instrument Serif, Fraunces (has a variable "wonk" axis for character), Playfair Display, Noto Serif Display, Newsreader.
- **Text serif (long body):** Tiempos Text, Source Serif 4, Newsreader, Literata, Charter, Georgia (system), Lora.
- **Sans for UI:** Söhne, Graphik, Inter, Neue Haas Grotesk, IBM Plex Sans.
- **Classic pairings:** serif headline + serif body (literary) or serif headline + sans body (modern). Use optical-size axes where available.
- **Scale:** 1.333–1.5 on fronts. Article headline 40–72px; standfirst 20–24px; **body 18–21px**, line-height 1.6–1.75, **measure 60–70ch**.
- Real typography: curly quotes, proper dashes, old-style numerals in body, small caps for acronyms, `hanging-punctuation`, `text-wrap: pretty` for body and `text-wrap: balance` for headlines.

### Color
- Background: `#FFFFFF`, `#FAF9F6` (paper), or `#F4EFE6` (cream).
- Ink: `#111` to `#1A1A1A`. Muted text: `#555`–`#6B6B6B`.
- Accent: one color (e.g., editorial red `#C8102E`, deep blue, or a section-coded palette).
- Dark "reading mode": warm dark grey `#1C1B19` with off-white text, never pure black.

### Spacing and shape
- Tight inside stories, generous between them. 8px base; article paragraphs spaced by line-height (1em margins).
- **Radius 0.** Hairline rules (1px) in ink at 10–20% opacity; thicker 2–4px rules for section breaks.

### Depth
- None. Flat, like paper. Hierarchy comes from type size, weight and rules.

### Motion
- Almost none. A reading progress bar, subtle image fade-ins, and footnote popovers. Scrollytelling only for special features (see the [Immersive Layer](./07-immersive-layer.md)).

### Imagery
- Art-directed photography with **consistent aspect ratios per slot** (e.g., 3:2 lead, 1:1 thumbnails, 4:5 portrait features).
- Illustration commissioned per story is a strong differentiator.
- Always caption and credit.

## 6. Page anatomy

**Front page / homepage:**
1. Masthead: wordmark (often a serif or custom logotype), date/issue, section nav, subscribe, search.
2. **Lead story:** largest headline and image, plus 2–4 related links.
3. Secondary stories in a 2–4 column asymmetric grid, separated by rules.
4. Section rows (Politics, Culture, Opinion…) each with its own mini-hierarchy.
5. "Most read" / "Latest" rail.
6. Newsletter sign-up module (one field).
7. Opinion/columnists with author portraits.
8. Footer: sections, about, masthead/staff, ethics/corrections policy, subscribe.

**Article page:**
1. Section kicker → headline → standfirst → byline, date, read time → share.
2. Lead image or video with caption.
3. Body column (≤ 70ch) with pull quotes, inline images that break out wider than the column, sidenotes.
4. Author bio → related stories → comments/newsletter.
5. Ads (if any) in *reserved* slots with fixed dimensions to avoid layout shift.

**Long-form feature:** full-bleed opener, chapter headings, section images that span edge to edge, occasional scroll-driven graphics.

## 7. Key components

Masthead · story card variants (lead/secondary/list/thumbnail) · kicker labels · byline block · pull quote · drop cap · footnote/sidenote · image with caption · table of contents · reading progress · newsletter sign-up · paywall prompt · related stories · author card · tag/section chips.

## 8. Copy and voice

The writing *is* the design. Headlines should be specific and active; standfirsts should add information, not repeat the headline. Keep a house style (numbers, dates, capitalization) and follow it consistently.

## 9. Pitfalls

- **Ad clutter and pop-ups** that destroy reading and CLS. Reserve ad slots and delay non-essential prompts.
- **Too-wide measure** on desktop. Always cap it.
- **Light-grey body text** (fashionable but often fails 4.5:1).
- **Web-font FOIT/FOUT** on long text. Use `font-display: swap`, match fallback metrics with `size-adjust`, and preload the text face.
- **Hierarchy collapse** on mobile. Keep kicker/headline/standfirst clearly different sizes.

## 10. Sub-styles

| Sub-style | Traits | Where |
|---|---|---|
| Newspaper | Dense multi-column, rules, red accent, serif headlines | NYT, Guardian, FT (salmon paper) |
| Magazine / culture | Big imagery, asymmetric grids, expressive display serif | Culture, fashion, design titles |
| Literary / blog | Single column, serif body, minimal chrome | Newsletters, essays, personal sites |
| Institutional editorial | Museum/research tone, grid discipline, sans + serif | Museums, think tanks |
| Editorial-commerce | Journal content blended with products | Aesop, many D2C "journal" sections |

## 11. Starter tokens

```css
:root {
  --paper: #FAF9F6;   --ink: #141414;   --ink-muted: #5C5C5C;
  --rule: color-mix(in oklch, var(--ink) 15%, transparent);
  --accent: #C8102E;
  --font-display: "Fraunces", "Tiempos Headline", Georgia, serif;
  --font-text: "Source Serif 4", "Charter", Georgia, serif;
  --font-ui: "Inter", system-ui, sans-serif;
}
body { background: var(--paper); color: var(--ink);
       font: 1.1875rem/1.7 var(--font-text); font-optical-sizing: auto; }
article > p { max-width: 66ch; margin-inline: auto; text-wrap: pretty; }
h1, h2 { font-family: var(--font-display); text-wrap: balance; line-height: 1.08; }
.kicker { font: 600 .8rem/1 var(--font-ui); letter-spacing: .08em; text-transform: uppercase; color: var(--accent); }
.story + .story { border-top: 1px solid var(--rule); }
```

## 12. Launch checklist

- [ ] Body text 18px+, measure ≤ 70ch, contrast ≥ 4.5:1
- [ ] Clear hierarchy of kicker/headline/standfirst/byline on every template
- [ ] Bylines, dates and "updated" timestamps; a corrections policy exists
- [ ] Ads and embeds have reserved dimensions (CLS ≤ 0.1)
- [ ] Web fonts preloaded with metric-matched fallbacks
- [ ] Article pages readable with JS disabled
- [ ] Structured data (Article, Author) for search and AI discovery
- [ ] Newsletter/subscription path visible but not intrusive
