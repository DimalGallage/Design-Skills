# 2 · Institutional Trust

> **Main job:** reassure people and help them finish important tasks without mistakes.
> **Feels:** calm, orderly, credible, accountable.
> **Expression level:** 1–2 of 5.

## 1. Essence

These sites serve people who are often **stressed, in a hurry, or not confident online**: paying a bill, claiming insurance, booking a clinic appointment, applying for a visa, choosing a pension. Trust comes from *predictability*: familiar patterns, plain language, clear hierarchy, strong accessibility and obvious accountability (who you are, how to reach you, how data is protected).

The visual roots are the **Swiss / International Typographic Style**: modular grids, sans-serif type, objective photography, content over form. The modern practical form is the **design system**: GOV.UK, US Web Design System, IBM Carbon, Material, and banks' in-house systems.

## 2. How it differs from the other categories

| vs. | Difference |
|---|---|
| Product-Led Tech | Tech shows off capability to evaluators. Institutional *reduces anxiety* for people who have to use it. Tech can go dark and trendy; Institutional stays light, conventional and plain-spoken. |
| Editorial | Both are text-heavy, but Editorial wants reading *time*. Institutional wants task *completion*: scan, find, act, leave. |
| Quiet Luxury | Both are restrained, but Luxury hides things and slows down; Institutional reveals things and speeds up. |
| Organic & Human | Organic earns trust through warmth. Institutional earns it through authority and competence. (Patient-facing healthcare blends the two.) |
| Bold Expressive | The opposite end. Research from NN/g and others says neobrutalism is unsuitable where trust, familiarity and readability come first, such as banking, healthcare and enterprise. |

## 3. Where to use it

**Best for:** retail and commercial banking · insurance · pensions and wealth management · healthcare providers, hospitals, pharma · government and public services · legal and accounting firms · universities (admissions and admin) · utilities and telecom account areas · enterprise IT, consulting, manufacturing · B2B procurement-heavy industries · nonprofits handling donations and aid.

**Use cases:** service portals, account dashboards, application forms, knowledge bases, corporate "about/investors" sites, compliance-heavy product pages.

**Avoid for:** brands whose whole proposition is disruption or attitude, lifestyle goods, creative portfolios.

## 4. Signature traits

- **Tasks first.** Search and the top 3–6 tasks are prominent on the homepage ("Pay a bill", "Find a doctor", "Make a claim").
- **Conventional navigation.** Horizontal main nav, breadcrumbs, a clear footer, and consistent placement of help and contact on every page (WCAG 2.2 criterion 3.2.6).
- **Plain language** at roughly a 9th-grade reading level; short sentences; front-loaded headings.
- **Proof of accountability:** regulator numbers, accreditation badges, privacy and security statements, physical address, phone number, named leadership.
- **Structured, predictable grid.** Few layout surprises.
- **Blue, green or teal brand color** (associated with stability and health). Deep neutrals. Color used *semantically* (success/warning/error) rather than decoratively.
- **Accessible, sturdy components:** large form fields, visible labels, strong focus states, error summaries.

## 5. Design tokens

### Typography
- **One highly legible sans** (humanist or neo-grotesque): Source Sans 3, IBM Plex Sans, Public Sans, Inter, Noto Sans, Atkinson Hyperlegible, or the system stack. GOV.UK uses its own "GDS Transport" typeface. Banks often commission their own.
- A serif is optional for heritage brands (law firms, old banks, universities), used only for headings.
- **Scale:** 1.2–1.25. Body **16–19px** (GOV.UK uses 19px body on desktop). Headings are bold rather than huge.
- Line-height 1.5–1.6, measure ≤ 70ch. Sentence case everywhere; avoid all caps except tiny labels.

### Color
- **Primary:** a trust hue (navy, royal blue, teal, forest green), shade 600–800 for text-safe use.
- **Neutrals:** 10-step cool grey scale. White backgrounds; light grey `#F3F4F6` for alternating sections.
- **Semantic:** success green, warning amber (with dark text), error red, info blue. Each paired with an icon and text.
- **Focus:** a high-visibility ring; the GOV.UK pattern is a yellow `#FFDD00` background plus a black underline, which works on any color.
- Everything meets 4.5:1 or better. Aim for AAA (7:1) on body text where possible.

### Spacing and shape
- 8px base; tighter vertical rhythm than marketing sites (section padding 48–96px).
- **Radius:** 0–8px. Square-ish reads as serious.
- Borders 1–2px, clearly visible on form fields (3:1 against the background).

### Depth
- Mostly flat. Light shadows only to show that a card or modal is interactive or layered.

### Motion
- Functional only: accordions, loading, focus. 150–250ms. No parallax, no autoplay. Respect reduced motion.

### Imagery
- **Real people** (staff, patients, customers) in real settings, diverse and representative. Avoid staged stock handshakes.
- Simple functional icons (outline, consistent stroke).
- Data visualizations that are clear and labelled, not decorative.

## 6. Page anatomy

**Homepage (service organization):**
1. Utility bar: language, accessibility options, "Log in", emergency or contact line.
2. Header: logo, main nav (5–7 items), prominent **search**.
3. Hero: plain statement of who you serve + **top task tiles** or search. Photo optional.
4. Alerts band (service outages, deadlines) when relevant.
5. Audience or segment entry points ("Personal / Business / Corporate", "Patients / Visitors / Professionals").
6. Key products or services in cards with clear rates, fees or eligibility.
7. Proof: ratings, accreditations, awards, regulator statement.
8. Help and support: FAQ, contact options, branch or location finder.
9. News and updates (light).
10. Footer: full sitemap, legal, regulatory disclosures, accessibility statement, social links.

**Transactional flow (GOV.UK "one thing per page" pattern):**
- Start page (what you'll need, how long it takes) → one question per page → check-your-answers → confirmation with a reference number and next steps.
- Error summary at the top linked to each field; inline errors that explain how to fix the problem.

**Corporate/enterprise "about" site:** mission, leadership, sectors, case studies, investor relations, careers, ESG, and press. Proof is concrete (clients, years, certifications) rather than claimed.

## 7. Key components

Search with suggestions · task tiles · breadcrumbs · accordions · tabs · step indicator · form fields with hint text · error summary · notification banners · data tables (sortable, responsive) · rate/fee cards · location finder · document download links (with file type and size) · cookie banner that doesn't hide focus.

## 8. Copy and voice

Plain, active, second person ("You can…"). Front-load keywords. Explain jargon or remove it. Give specifics: fees, time needed, eligibility. Never use dark patterns; regulators and users punish them.

## 9. Pitfalls

- **Dull ≠ trustworthy.** Look competent, not neglected. Use good photography, generous spacing and a modern type system.
- **Org-chart navigation** ("Divisions", "Group Functions") instead of user tasks.
- **Hidden fees or contact details.** Their absence is itself a trust signal, a negative one.
- **PDF-only content.** Publish in HTML first.
- **Sticky chat widgets and cookie banners covering focused elements** (fails WCAG 2.4.11).
- **Compliance with a design system ≠ accessibility.** Test with assistive technology users.

## 10. Sub-styles

| Sub-style | Traits | Where |
|---|---|---|
| Public-service utilitarian | System fonts, one column, task-first, text-heavy | GOV.UK, USA.gov, Singapore's design system |
| Corporate Swiss | 12-column grid, bold sans, photography, confident whitespace | Enterprise, consulting, engineering |
| Friendly institutional | Rounded type, illustration, warmer palette | Challenger banks, consumer health, insurtech (blends with 5) |
| Heritage institutional | Serif headings, crest, deep navy/burgundy | Universities, law firms, private banks |

## 11. Starter tokens

```css
:root {
  --bg: #FFFFFF;              --bg-alt: #F3F4F6;
  --text: #0B0C0C;            --text-muted: #505A5F;
  --primary: #1D4ED8;         --primary-dark: #1E3A8A;
  --success: #00703C;         --warning: #B45309;   --danger: #D4351C;
  --border-input: #6B7280;    /* ≥3:1 on white */
  --focus: #FFDD00;
  --font: "Source Sans 3", "Public Sans", system-ui, sans-serif;
  --radius: 4px;              --step-0: 1.1875rem; /* 19px */
}
:focus-visible { outline: 3px solid var(--focus); outline-offset: 0;
                 box-shadow: 0 0 0 5px var(--text); }
input, select, textarea { border: 2px solid var(--border-input); min-height: 44px; }
```

## 12. Launch checklist

- [ ] Top tasks are reachable from the homepage in one click
- [ ] Search is visible and works with misspellings
- [ ] Contact/help appears in the same place on every page
- [ ] Fees, eligibility and timelines are stated plainly
- [ ] Accreditations, regulator info, privacy and accessibility statements are linked
- [ ] Forms: labels, hints, error summary, no repeated entry, accessible authentication
- [ ] WCAG 2.2 AA audit passed, including testing with screen readers and keyboard only
- [ ] Works on low-end devices and slow connections; content isn't locked in PDFs
