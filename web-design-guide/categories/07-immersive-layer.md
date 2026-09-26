# + · The Immersive Layer

> **Main job:** turn a website into an *experience*: a story people move through.
> **Feels:** cinematic, spatial, memorable.
> **Not a standalone category:** an intensity layer added on top of a base category (most often 1, 4 or 6, sometimes 3 or 5).

## 1. Why it's a layer, not a category

Immersive sites leading Awwwards and FWA in 2026 don't share a *look*. Cartier's "365: A Year of Cartier" is luxury; a WebGL developer-conference site is tech; a band's album site is bold. What they share is a **delivery mode**: real-time 3D (WebGL/WebGPU, Three.js), scroll-driven narrative, unusual navigation and high production value. So pick the base category first. It sets the palette, type and tone. Then decide how much immersion to add.

| Base + Immersive | Result |
|---|---|
| Quiet Luxury + Immersive | Cinematic brand worlds, 3D jewellery/watch configurators, hotel virtual tours |
| Product-Led Tech + Immersive | 3D product explorers, interactive architecture diagrams, shader heroes, launch keynotes |
| Bold Expressive + Immersive | Game-like campaign sites, music/album worlds, agency showreels |
| Editorial + Immersive | Scrollytelling journalism, data stories |
| Organic + Immersive | Virtual farm/vineyard tours, nature-journey storytelling |

## 2. Where to use it

**Best for:** product launches (phones, cars, sneakers, consoles) · automotive configurators · luxury campaigns · entertainment (films, games, albums) · creative agency showcases · museums and virtual exhibitions · real estate pre-sales (virtual walkthroughs) · data journalism · tourism destinations · brand anniversaries.

**Avoid when:** the audience needs to complete tasks quickly, budgets are small (custom WebGL is expensive to build and maintain), most traffic is on low-end mobile devices, or the content is updated often by non-specialists.

## 3. Signature traits

- **Narrative structure** (beginning, middle, end) instead of a page hierarchy. The story unfolds as you scroll.
- **Scroll as the storytelling device:** each section is a beat with an *entrance, hold and exit*.
- **Real-time 3D** scenes, product models, particles, shaders, post-processing.
- **Unusual navigation**, designed rather than bolted on. Award write-ups argue that changing the grammar of a site beats adding effects to an existing one.
- **Sound design** (always opt-in).
- **Preloaders** that are part of the experience.

## 4. How award juries judge it (and how to plan)

Five axes that appear repeatedly in 2026 award analysis:
1. **Technical execution:** shader and 3D quality.
2. **Narrative cohesion:** does the scroll tell a story?
3. **Performance discipline:** load time and sustained frame rate.
4. **Accessibility integration:** progressive enhancement and fallbacks.
5. **Emotional impact:** memorability.

## 5. Build guide

### Plan
- Write the **story script** first: 5–9 beats, each with one message and one visual idea.
- Storyboard each beat: camera, object state, text, interaction.
- Define **device tiers** and a **performance budget** up front: desktop with a discrete GPU, flagship mobile, mid-range mobile, plus a static fallback.

### Technology
- **CSS first:** scroll-driven animations (`animation-timeline: scroll()/view()`) and View Transitions now cover most reveal, parallax and page-transition needs natively and off the main thread.
- **JS animation:** GSAP + ScrollTrigger for complex timelines; Lenis for smooth scroll (without breaking native keyboard scrolling).
- **3D:** Three.js / React Three Fiber, or Spline for simpler scenes; WebGPU where supported, with a WebGL fallback.
- **Assets:** glTF + Draco/Meshopt compression, KTX2/Basis textures, baked lighting, low polygon counts on mobile.

### Performance budget (suggested)
- First meaningful paint from **HTML/CSS content**, not the canvas. LCP ≤ 2.5s with a real text or image LCP element.
- Initial JS ≤ 300KB gzip before the 3D bundle; lazy-load 3D after first interaction or idle.
- 3D payload ≤ 5–10MB desktop, ≤ 2–3MB mobile tier.
- 60fps target (30fps floor) on mid-range mobile; adapt pixel ratio (`min(devicePixelRatio, 1.5)` on mobile).
- INP ≤ 200ms: never block input with heavy per-frame work on the main thread.

### Progressive enhancement and accessibility
- **All content and navigation exist in semantic HTML.** The canvas decorates; it doesn't hold the only copy of the information.
- **Tiered delivery:** full scene on capable desktops, simplified scene on mobile, static images or video on low-end devices or when WebGL is unavailable. A fallback is "another implementation of the same user task", not a poster added at the end.
- **If the WebGL context is lost,** keep the HTML interface, explain what happened, and offer a retry or the content path.
- **`prefers-reduced-motion`:** shorten camera travel, replace parallax with direct state changes, stop autoplay rotation, keep orientation stable.
- A **"Skip intro / view as page"** option; keyboard-operable hotspots; text alternatives for 3D content; captions for audio and video; sound off by default.
- Don't hijack scroll in ways that break trackpads, keyboards and screen readers.

## 6. Page anatomy (typical launch experience)

1. **Preloader:** branded, shows progress, ≤ 3s ideal; content skeleton behind it.
2. **Opening beat:** hero scene with product/world, one line of text, "Scroll to explore" cue.
3. **Beats 2–6:** each reveals one feature or chapter; the camera moves, the object transforms, text enters, holds and exits.
4. **Interactive moment:** configurator, rotate or explore, mini-game.
5. **Resolution:** the payoff shot, key message, primary CTA (buy, pre-order, book).
6. **Conventional footer section:** specs, pricing, FAQ, legal, as normal HTML.
7. **Persistent UI:** minimal nav, sound toggle, progress indicator, skip/menu.

## 7. Starter pattern

```css
/* Native scroll-driven reveal: works without JS, respects reduced motion */
.beat { view-timeline-name: --beat; }
@media (prefers-reduced-motion: no-preference) {
  .beat .copy {
    animation: beat-in linear both;
    animation-timeline: --beat;
    animation-range: entry 10% contain 40%;
  }
}
@keyframes beat-in { from { opacity: 0; transform: translateY(40px); } to { opacity: 1; transform: none; } }
```

```js
// Load 3D only when capable and wanted
const canWebGL = !!document.createElement('canvas').getContext('webgl2');
const reduce = matchMedia('(prefers-reduced-motion: reduce)').matches;
const lowEnd = navigator.hardwareConcurrency <= 4 || navigator.deviceMemory <= 4;
if (canWebGL && !reduce) {
  requestIdleCallback(() => import('./scene.js').then(m => m.init({ tier: lowEnd ? 'lite' : 'full' })));
} // else: static images/video already in the HTML stay visible
```

## 8. Launch checklist

- [ ] Story script with ≤ 9 beats; each beat has one message
- [ ] All content present in semantic HTML; canvas is enhancement only
- [ ] Device tiers tested: desktop GPU, flagship mobile, mid-range mobile, no-WebGL
- [ ] LCP ≤ 2.5s from HTML content; INP ≤ 200ms; stable fps on mid-range phones
- [ ] Reduced-motion version and "skip/view as page" option exist
- [ ] Sound off by default with a visible toggle
- [ ] Keyboard and screen-reader users can reach every piece of content and the CTA
- [ ] The primary CTA isn't buried at the end of a long, unskippable sequence
