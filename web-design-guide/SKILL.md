---
name: web-design-categories
description: Classifies a website brief into one of seven modern web design categories (Product-Led Tech, Institutional Trust, Editorial, Quiet Luxury, Organic & Human, Bold Expressive, Premium Product Minimalism / "Apple-like"), plus an optional Immersive layer, then applies that category's tokens, page anatomy, components and checklist. Use when designing, building, critiquing or restyling a website or landing page, choosing a visual direction, or when a user asks "what style should my site be?".
---

# Web Design Categories

## Workflow

1. **Classify the brief.** Work out the site's main job and how loud it can be, then pick one leading category (optionally a secondary one) using the questions in [README.md](./README.md#picking-a-category):
   - High-stakes tasks (money, health, law, government) → **Institutional Trust**
   - Software that must be understood before buying → **Product-Led Tech**
   - Content is the product → **Editorial**
   - Premium, emotional, status purchase → **Quiet Luxury**
   - Trust through warmth and values → **Organic & Human**
   - Standing out beats looking conventional → **Bold Expressive**
   - Premium engineered product (device, vehicle, appliance, wearable) sold on design + specs, "Apple-like" → **Premium Product Minimalism**
   - Launch or story with budget and time on page → add the **Immersive layer**
2. **Read the category file** in `categories/` and follow its tokens, page anatomy and components.
3. **Apply [00-foundations.md](./00-foundations.md)** regardless of category: WCAG 2.2 AA, Core Web Vitals, 8px spacing, fluid modular type, 45–75ch measure, reduced-motion support.
4. **Add one signature element** so the result doesn't read as a generic template (see foundations §10).
5. **Run the category's launch checklist** before calling the work done.

## Category files

| Category | File |
|---|---|
| Product-Led Tech | [categories/01-product-led-tech.md](./categories/01-product-led-tech.md) |
| Institutional Trust | [categories/02-institutional-trust.md](./categories/02-institutional-trust.md) |
| Editorial | [categories/03-editorial.md](./categories/03-editorial.md) |
| Quiet Luxury | [categories/04-quiet-luxury.md](./categories/04-quiet-luxury.md) |
| Organic & Human | [categories/05-organic-human.md](./categories/05-organic-human.md) |
| Bold Expressive | [categories/06-bold-expressive.md](./categories/06-bold-expressive.md) |
| Premium Product Minimalism ("Apple-like") | [categories/08-premium-product-minimalism.md](./categories/08-premium-product-minimalism.md) |
| Immersive layer | [categories/07-immersive-layer.md](./categories/07-immersive-layer.md) |

## Rules to never break

- Don't use Bold Expressive or heavy Immersive for regulated or high-stakes task flows.
- Don't let a style excuse failing contrast (4.5:1 text, 3:1 UI), targets < 24px, hidden focus, or motion that ignores `prefers-reduced-motion`.
- Keep content in semantic HTML; canvas, glass and effects are enhancements with fallbacks.
