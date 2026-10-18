---
name: A.S.D. WE SPORT
description: Dark-ground inclusive sport brand — one signal teal accent, bold "Kobe" display type over airy "Outfit" body copy, organic asymmetric imagery against pill-shaped UI chrome.
colors:
  signal-teal: "#00a6b2"
  near-black: "#1d1d1b"
  charcoal-surface: "#262624"
  pure-white: "#ffffff"
  soft-white: "rgba(255, 255, 255, 0.85)"
  muted-white: "rgba(255, 255, 255, 0.72)"
  hairline-white: "rgba(255, 255, 255, 0.28)"
typography:
  display:
    fontFamily: "Kobe, sans-serif"
    fontSize: "76px"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Kobe, sans-serif"
    fontSize: "52px"
    fontWeight: 800
    lineHeight: 1.05
  title:
    fontFamily: "Kobe, sans-serif"
    fontSize: "30px"
    fontWeight: 800
    lineHeight: 1.1
  body:
    fontFamily: "Outfit, sans-serif"
    fontSize: "18px"
    fontWeight: 300
    lineHeight: 1.6
  label:
    fontFamily: "Kobe, sans-serif"
    fontSize: "14px"
    fontWeight: 600
    letterSpacing: "0.14em"
rounded:
  pill: "999px"
  card: "28px"
  field: "14px"
spacing:
  xs: "16px"
  sm: "24px"
  md: "32px"
  lg: "56px"
  xl: "96px"
components:
  button-primary:
    backgroundColor: "{colors.signal-teal}"
    textColor: "{colors.near-black}"
    rounded: "{rounded.pill}"
    padding: "16px 32px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.pure-white}"
    rounded: "{rounded.pill}"
    padding: "14px 30px"
  card:
    backgroundColor: "{colors.charcoal-surface}"
    rounded: "{rounded.card}"
---

# Design System: A.S.D. WE SPORT

## Overview

**Creative North Star: "The Shared Rhythm"**

Swimming and dance are both forms of rhythm and movement, and the system treats inclusion the same way: not a separate track bolted onto the brand, but the current everyone moves through together. The ground is a near-black charcoal stage that lets one color — Signal Teal — do all the talking; everything else is tonal (charcoal surfaces, three opacities of white) rather than additional hue. Display type is heavy and confident (Kobe, 700–900), set against body copy that stays deliberately light (Outfit, 300), so statements land with weight while explanations stay airy and easy to read at length.

The system's signature is asymmetric: hero and split photography sit in frames with one or two corners pulled into a deep organic curve while the others stay tight, echoing the brand's own "fluidità" value rather than defaulting to a uniform rounded-rectangle. UI chrome does the opposite — buttons are full pills, cards and the contact form share one consistent 28px radius — so the organic imagery and the disciplined interface read as two deliberately different vocabularies, not an inconsistency.

There are no shadows anywhere in the system. Depth comes from tonal contrast — near-black against lighter charcoal surfaces, white at three opacities, and a dark overlay dropped over the one full-bleed photographic moment (Claim) — never from elevation.

**Key Characteristics:**
- One accent, no exceptions: Signal Teal is the only hue in the system.
- Heavy display type over light body type — a deliberate weight snap, not a mismatch.
- Organic, asymmetric corners on photography; disciplined pill/28px corners on UI chrome.
- Flat by construction — tonal layering stands in for shadows everywhere.

## Colors

The palette is almost monochrome by design: near-black and two tones of charcoal/white carry the entire surface, and Signal Teal is deployed as a rare, deliberate signal rather than a secondary brand color.

### Primary
- **Signal Teal** (`#00a6b2`): The brand's one accent. Used for the eyebrow labels, the `.outline`'s rare colored use, link color, hover states (nav, ghost button, footer links), the primary button fill, list-item bullets, input focus rings, and the decorative "fluidity" gradient disc. Never used as a large background fill outside the primary button.

### Neutral
- **Near-Black** (`#1d1d1b`): The base page background and the primary button's text color (teal-on-black inverts to black-on-teal).
- **Charcoal Surface** (`#262624`): Raised surfaces — discipline cards, the contact form panel, and the mobile nav dropdown. One step lighter than the page background; this is the system's only elevation cue.
- **Pure White** (`#ffffff`): Primary text color and the `.outline` stroke color.
- **Soft White** (`rgba(255,255,255,.85)`): Body copy inside sections (paragraphs, card/value body text).
- **Muted White** (`rgba(255,255,255,.72)`): Secondary/footer text.
- **Hairline White** (`rgba(255,255,255,.28)`): Borders — input borders, the dashed "coming soon" card border, the footer top rule.

### Named Rules
**The Lone Signal Rule.** Signal Teal is the only accent color in the system. A second accent hue is never introduced; new emphasis is expressed through weight, size, or the existing white opacities, not a new color.

## Typography

**Display Font:** Kobe (with sans-serif fallback) — a custom webfont loaded as five weight/style cuts (400, 700, 900, each with an oblique).
**Body Font:** Outfit (with sans-serif fallback) — loaded from Google Fonts at weights 300/400/500.

**Character:** Kobe carries every headline-scale and label-scale moment at heavy weight (700–800); Outfit carries every paragraph at light weight (300). The pairing's whole personality is that contrast: bold statements, quiet explanations.

### Hierarchy
- **Display** (800, 76px desktop / 56px ≤900px / 44px ≤560px, line-height 1.02, letter-spacing -0.02em): The hero `<h1>` only.
- **Headline** (800, 52px desktop / 42px ≤900px / 36px ≤560px, line-height 1.05): Section titles (`.title`) — "chi siamo", "discipline", "per chi", "contatti".
- **Title** (800, 30–34px): Card and value titles (`.card__title`, `.value__title`).
- **Body** (300, 18px desktop / 17px ≤560px, line-height 1.6): All paragraph copy. Soft White or Muted White, never pure white.
- **Label** (600, 14px, letter-spacing 0.14em, uppercase): Eyebrow kickers above headlines, always in Signal Teal; the footer's association name reuses the same label treatment at 14px/0.08em.

### Named Rules
**The Weight Contrast Rule.** Display-role type is never set below 700 weight; body-role type is never set above 400 weight (it is 300 everywhere observed). The gap between the two is the system's typographic voice — don't narrow it with a mid-weight compromise.

## Layout

A single centered container (`1280px` max-width, `32px` gutter, `20px` on screens ≤560px) holds every section. Sections stack vertically with generous vertical rhythm — `96px` top/bottom padding, tightening to `64px` on screens ≤560px. Two-column "split" sections (text + media) and the discipline card grid both wrap to a single column via `flex-wrap` once their content no longer fits at a `440px`+ basis, rather than using fixed breakpoints for every layout. Primary breakpoints: `900px` (type scale steps down) and `560px` (gutter, section padding, and type scale step down again); the header's own nav collapses to a dropdown at `700px`.

## Elevation & Depth

Flat by construction — there is no `box-shadow` anywhere in the system. Depth is read entirely through tonal contrast: the near-black page background, one step up to Charcoal Surface for cards/form/mobile-nav, and the single dark overlay (`rgba(29,29,27,.62)`) dropped over the Claim section's full-bleed photograph so pale display type stays readable over an image.

### Named Rules
**The No-Shadow Rule.** Never add a `box-shadow` to communicate elevation. Reach for a lighter tonal surface (Charcoal Surface) or an overlay instead.

## Shapes

Two deliberately different corner vocabularies coexist. UI chrome is disciplined: buttons are full pills (`999px`), and cards/the contact form/the mobile-nav panel all round to `28px` (the mobile-nav panel only rounds its bottom two corners, `0 0 24px 24px`, since it drops down from the header). Photography is organic: hero and split media sit in frames with one to two corners pulled into a large soft curve while the rest stay tight or square — e.g. the hero image at `280px 24px 24px 120px`, the "chi siamo" image at `24px 24px 220px 24px`, the "per chi" image mirrored at `220px 24px 24px 24px`. Value-section portraits break from both vocabularies and sit in plain circles (`50%`). Form inputs round to a smaller `14px`, between the two systems.

## Components

### Buttons
- **Shape:** Full pill (`999px` radius) on every variant.
- **Primary:** Signal Teal background, Near-Black text, `16px 32px` padding, 500 weight. Hover brightens the fill (`filter: brightness(1.1)`) rather than changing color.
- **Ghost:** Transparent background, `1.5px` solid Pure White border and text, `14px 30px` padding. Hover shifts border and text to Signal Teal (no brightness filter).
- **Small variant:** Same shapes at tighter `12px 26px` padding, used for the header's "Iscriviti" nav CTA.
- **Submit (`.btn--button`):** A block-level ghost-radius-free variant — `52px` min-height, no border, used only for the contact form's submit action.

### Cards
- **Corner Style:** `28px` radius, uniform on all variants.
- **Background:** Charcoal Surface; the "coming soon" placeholder variant drops to transparent with a `1.5px` dashed Hairline White border instead.
- **Shadow Strategy:** None — see Elevation & Depth.
- **Internal Padding:** `32px`.

### Inputs / Fields
- **Style:** Near-Black fill, `1px` solid Hairline White border, `14px` radius; single-line inputs are `52px` tall.
- **Focus:** `2px` solid Signal Teal outline with `2px` offset — no border-color change, no glow.

### Navigation
- Body-weight links at `16px`; hover shifts color straight to Signal Teal, no underline. The primary nav always carries the small ghost-free "Iscriviti" pill as its final, visually distinct item.
- **Mobile (≤700px):** Collapses into a Charcoal Surface dropdown (`0 0 24px 24px` radius) that slides/fades open from under the header; respects `prefers-reduced-motion` by dropping the transition entirely.

### Fluidity Disc (signature)
The one fully abstract element among otherwise photographic imagery: a circular "value" icon (same `220px` circle frame as the photographic value icons) built from layered radial and conic gradients blending Signal Teal into a pale yellow-green and a deep teal-black. It stands in for the "fluidità" value and is the clearest graphic expression of the brand's movement/water idea.

## Do's and Don'ts

### Do:
- **Do** keep Signal Teal as the system's only accent color — new emphasis comes from weight, size, or white-opacity, not a new hue.
- **Do** pair heavy display weight (700+) with light body weight (300); never settle on a mid-weight compromise.
- **Do** give hero/split photography at least one deep, asymmetric corner radius — never let an image frame use four matching corners.
- **Do** keep all buttons at full pill radius (`999px`), distinct from the `28px` card/form radius.

### Don't:
- **Don't** add `box-shadow` anywhere; depth is tonal (Near-Black → Charcoal Surface → overlay), never elevation-based.
- **Don't** introduce a second or third accent color; this is deliberately a one-accent system.
- **Don't** set body copy above 400 weight — the light/bold contrast is load-bearing for the system's voice.
- **Don't** round photography corners symmetrically; that vocabulary belongs to UI chrome (buttons, cards, form), not to imagery.
