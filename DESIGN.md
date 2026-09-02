---
name: Generational Club
description: A community craft club proven through its own two-ink print run — a small zine about real visits, not a nonprofit template.
colors:
  riso-flame-red: "#C4341F"
  riso-flame-red-bright: "#FF4B33"
  riso-flame-red-hover: "#A32A18"
  riso-federal-blue: "#005A8F"
  riso-federal-blue-bright: "#0072B5"
  warm-uncoated-paper: "#F3ECD9"
  lighter-print-stock: "#FBF3E0"
  espresso-ink: "#2A2620"
  soft-ink-wash: "#5C5648"
typography:
  display:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "clamp(32px, 4.6vw, 50px)"
    fontWeight: 700
    lineHeight: 1.1
  headline:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "clamp(26px, 3vw, 32px)"
    fontWeight: 700
    lineHeight: 1.1
  title-lg:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "23px"
    fontWeight: 700
    lineHeight: 1.1
  title:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "19px"
    fontWeight: 700
    lineHeight: 1.1
  title-sm:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "20px"
    fontWeight: 700
    lineHeight: 1.1
  wordmark:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "clamp(20px, 3vw, 26px)"
    fontWeight: 700
  body-lead:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "19px"
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "17px"
    fontWeight: 400
  body-md:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "16.5px"
    fontWeight: 400
  label:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "15.5px"
    fontWeight: 600
  label-btn:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "16px"
    fontWeight: 700
  label-sm:
    fontFamily: "Zilla Slab, Georgia, serif"
    fontSize: "15px"
    fontWeight: 700
  caption:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "14.5px"
    fontWeight: 700
  caption-sm:
    fontFamily: "Public Sans, Arial, Helvetica, sans-serif"
    fontSize: "14px"
    fontWeight: 400
rounded:
  none: "0px"
  circle: "50%"
spacing:
  section: "56px"
  card: "24px"
  gap: "22px"
components:
  button-primary:
    backgroundColor: "{colors.riso-flame-red}"
    textColor: "{colors.lighter-print-stock}"
    rounded: "{rounded.none}"
    padding: "13px 26px"
  button-primary-hover:
    backgroundColor: "#A32A18"
    textColor: "{colors.lighter-print-stock}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.riso-federal-blue}"
    rounded: "{rounded.none}"
    padding: "13px 26px"
  button-secondary-hover:
    backgroundColor: "{colors.riso-federal-blue}"
    textColor: "{colors.lighter-print-stock}"
---

# Design System: Generational Club

## Overview

**Creative North Star: "The Two-Ink Print Run"**

The site presents itself as a small risograph-printed zine about a real, currently-running teen volunteer club, not a nonprofit-template landing page. Two spot inks — a flame red and a federal blue — carry every accent, CTA, and category marker in the system, rendered with `mix-blend-mode: multiply` wherever they sit over paper or a photograph, exactly as a real two-pass riso print would. A fine halftone-dot grain sits under every paper surface and over every photograph, so the site reads as printed material rather than rendered UI. The system is deliberately plain-spoken rather than precious: square corners, solid ink borders instead of shadows, real photography (never illustration or stock imagery) presented as slightly-rotated, registration-marked "tipped-in" print cards where a single photo needs to carry a moment (the hero) and as bordered gallery tiles elsewhere.

The build explicitly rejects two adjacent failure modes: it is not the cream-background/rounded-card/stock-photo default that most "volunteer nonprofit" sites converge on, and it does not tip into a stylish "indie design studio" look that would read as more agency than teen club. Numbered sequence badges are reserved for the one genuinely ordered process on the site (the four-step join flow); parallel or categorical content never borrows that numbering, because a previous pass over-applied it and implied an order that didn't exist.

**Key Characteristics:**
- Two spot inks (red + blue) and nothing else; no third accent color anywhere.
- Flat, bordered surfaces — no box-shadow in the system; depth comes from a 2px solid ink border.
- Square corners everywhere except perfect circles (avatars, partner badges).
- Halftone-dot grain on every paper surface and every real photograph, never selectively.
- Numbered badges are reserved for genuine sequences; categorical content uses a plain ink-color swatch instead.

## Colors

Two spot inks plus a warm paper neutral family; both inks carry a text-safe (darker, WCAG AA-passing) value and a brighter decorative-only value for shapes with no text over them.

### Primary
- **Riso Flame Red** (#C4341F): Primary CTA background, primary folio-badge/ink-mark color, link hover state. Text-safe against both `Lighter Print Stock` and white — used wherever red sits behind or as text.
- **Riso Flame Red — Hover** (#A32A18): The darkened hover/active state for the primary button only. Never used at rest.
- **Riso Flame Red — Bright** (#FF4B33): Decorative-only. The photo hover/focus/active misregistration fringe. Never placed under text.

### Secondary
- **Riso Federal Blue** (#005A8F): Body link color, secondary/outline CTA, secondary folio-badge/ink-mark color, trust-strip background.
- **Riso Federal Blue — Bright** (#0072B5): Decorative-only. The photo hover/focus/active misregistration fringe.

### Neutral
- **Warm Uncoated Paper** (#F3ECD9): Page background, always under the grain texture.
- **Lighter Print Stock** (#FBF3E0): Card, section-band, masthead, and footer background (also under grain); reversed text color on solid-ink surfaces (buttons, CTA block, gallery group labels).
- **Espresso Ink** (#2A2620): Primary text, all borders, headings.
- **Soft Ink Wash** (#5C5648): Secondary/body-soft text (leads, captions, card copy).

### Named Rules
**The Two-Ink Rule.** Only Riso Flame Red and Riso Federal Blue (and their bright decorative variants) carry color in this system. A third accent color is never introduced, even for a single new component.

**The Bright-Never-Under-Text Rule.** The `-bright` decorative variants exist only because they fail WCAG contrast as text/background pairs. They are used exclusively for shapes nothing is written on (ink blobs, hover fringes) — never as a button fill, link color, or text color.

**The No-Dark-Mode Rule.** This system deliberately does not implement `prefers-color-scheme` dark mode. A printed riso zine has no "dark mode" — the single warm-paper palette is the material itself, not a light-theme default awaiting a dark counterpart. This was evaluated and confirmed during an accessibility audit, not overlooked; revisit only as an explicit, deliberate decision, never as a routine dark-mode add.

## Typography

**Display Font:** Zilla Slab (with Georgia, serif fallback)
**Body Font:** Public Sans (with Arial, Helvetica, sans-serif fallback)

**Character:** A confident slab serif for anything that reads as a headline or label, paired with a plain, highly legible grotesque for body copy — deliberately unfussy, closer to a well-set community newsletter than an editorial magazine.

### Hierarchy
- **Display** (700, `clamp(32px, 4.6vw, 50px)`, 1.1 line-height): Hero headline only.
- **Headline** (700, `clamp(26px, 3vw, 32px)`, 1.1): Section headings (`h2`).
- **Title-lg** (700, 23px, 1.1): The Get-Involved CTA-block heading.
- **Title** (700, 19px, 1.1): Card/component headings — member name, partner-box `h3`.
- **Title-sm** (700, 20px, 1.1): Pillar `h3`, folio-badge numeral.
- **Wordmark** (700, `clamp(20px, 3vw, 26px)`): Masthead and footer wordmark specifically (not reused elsewhere).
- **Body-lead** (400, 19px, 1.6): Hero lead paragraph.
- **Body** (400, 18px, 1.6): Running copy, section-head descriptions. No line-length constraint beyond the 980px page wrap.
- **Body-sm** (400, 17px): Table cells, folio/CTA body copy, lightbox caption.
- **Body-md** (400, 16.5px): Pillar body copy.
- **Label** (600, 15.5px): Nav links, partner-box copy, footer base text.
- **Label-btn** (700, 16px): Button and trust-strip text.
- **Label-sm** (700, 15px, uppercase where used): Gallery-group-title chip, footer column headings, photo captions.
- **Caption** (700, 14.5px, uppercase): Member role.
- **Caption-sm** (400, 14px): Hero photo caption, footer copyright line.

Every literal `font-size` in the shipped CSS maps to one of the roles above — this list is generated from the actual stylesheet, not aspirational.

### Named Rules
**The No-Kicker Rule.** No heading is preceded by an eyebrow/kicker label. A prior build shipped one above the hero headline; it was removed and must not return regardless of how it's requested — fold the context into the heading or lead copy instead.

## Layout

Single-column, section-stacked page inside a 980px max-width `.wrap` container with 24px horizontal padding. Sections carry generous vertical rhythm (56px top/bottom padding). Grids are used for genuinely parallel content: `.pillars` and `.partners` are 3-column, `.gallery` and `.members` flow at `repeat(auto-fit, minmax(200px, 240px))` or a fixed 3-column grid, collapsing to 2 columns at 760px and 1 column at 480px. The four-step "Get Involved" flow and the Activities table use a `.spread`/table layout that stacks to a single column under 760px. The masthead is `position: sticky; top: 0`.

## Elevation & Depth

Flat. There is no `box-shadow` anywhere in the system. Every surface that needs to read as distinct from its background uses a 2px solid Espresso Ink border instead — cards, buttons, the CTA block, table, photo frames, the four-step spread. Depth is implied by the ink-block treatment (solid-color fills reading as printed panels) and by the halftone grain differentiating paper tones, never by shadow.

### Named Rules
**The Border-Not-Shadow Rule.** Any new component that needs visual separation from its background gets a 2px solid `Espresso Ink` border. Never reach for `box-shadow` to create that separation — it isn't in this system's material vocabulary.

## Shapes

Square corners everywhere — no `border-radius` on buttons, cards, tables, photo frames, or the CTA block. The one exception is perfect circles (`border-radius: 50%`): the member avatar and the three partner badges. This binary (sharp rectangle vs. perfect circle, nothing in between) is deliberate and should not be softened with an intermediate radius. (An earlier build shipped a stray 4px radius on the mobile nav-toggle button, which contradicted this rule on inspection; it has been corrected to square.)

## Components

### Buttons
- **Shape:** Square corners (0px radius), 2px solid border matching the fill/outline color.
- **Primary (`.btn.solid-red`):** Riso Flame Red fill, Lighter Print Stock text, 13px/26px padding. Hover darkens to `#A32A18`.
- **Secondary (`.btn.outline-blue`):** Transparent fill, Riso Federal Blue border and text. Hover fills solid blue with Lighter Print Stock text.
- Inside the red CTA block, the primary button inverts (Lighter Print Stock fill, red text) so it never sits red-on-red.

### Cards / Containers
- **Corner Style:** Square (0px radius) on every card type — pillar, member card, partner box, four-step folio.
- **Background:** `Lighter Print Stock` layered under the grain texture (`--grain` composited with the paper token, never a flat color alone).
- **Shadow Strategy:** None — see Elevation & Depth.
- **Border:** 2px solid Espresso Ink on all standalone cards; 1px `border-strong` hairline as an internal divider between rows/columns within a shared container (table rows, spread columns).

### Ink-Mark / Folio-Badge (signature components)
- **Ink-mark:** A plain 13px solid-color square (red or blue, `mix-blend-mode: multiply`) used as a category marker for parallel/non-sequential content (Mission pillars, Activities table rows). Carries no digit.
- **Folio-badge:** An outlined numeral (Zilla Slab, 1.5px text-stroke, transparent fill) used exclusively for the four genuinely sequential join-flow steps. **Never use folio-badge numbering on content that isn't a real, order-dependent sequence** — reach for ink-mark instead.

### Photo Frames
- 2px solid ink border, 4:3 aspect ratio, `object-fit: cover`.
- A hairline "+" registration mark sits at the top-left and bottom-right corners of every frame (drawn in CSS, not an image asset).
- A subtle halftone-dot overlay (`mix-blend-mode: multiply`, ~12% opacity) sits over every photo, screening it into the print world without desaturating it.
- A red/blue misregistration "ink fringe" (both colors' bright variants, `mix-blend-mode: multiply`) sits behind the frame at a low baseline opacity/offset (visible at rest, for touch users) and intensifies on hover, keyboard focus-within, and active/tap.

### Hero Photo Card (signature component)
The hero uses the same photo-frame primitive above, wrapped in a fixed-width card (`Lighter Print Stock` under grain, 2px ink border) rotated -2.5° with an italic caption below — a "tipped-in" physical print rather than a full-bleed hero image. Reserve this treatment for a single, specific supporting photo (not a rotating/generic hero image slot); it is not a click-to-enlarge affordance like the gallery frames, so its cursor stays default rather than zoom-in.

### Navigation
- Sticky masthead, Lighter Print Stock background under grain, 3px solid ink bottom border.
- Links: Espresso Ink, 600 weight, underline-on-hover via a 2px bottom border that turns red.
- Mobile: a bordered square icon button (authored SVG hamburger/close, never a Unicode glyph) toggles a stacked link list below the masthead.

### Lightbox
- Near-black warm overlay (`rgba(26,21,18,.94)`), not pure black.
- Enlarged photo keeps the same halftone-dot overlay as its gallery thumbnail — the print treatment must not disappear at the moment a visitor looks closest.
- Close/prev/next controls are authored SVG icons (2px stroke, `currentColor`) inside circular ghost buttons that solidify to Flame Red on hover.

## Do's and Don'ts

### Do:
- **Do** apply the `--grain` halftone texture to every surface using the paper or print-stock neutral — never let a section fall back to a flat, ungrained color.
- **Do** keep buttons, cards, and frames square-cornered; reserve perfect circles for avatars and badges only.
- **Do** author icons as inline SVG at a consistent 2px stroke weight.
- **Do** keep the photo ink-fringe effect present (however subtle) at rest, not gated entirely behind hover, so touch users see it too.
- **Do** reserve numbered folio-badges for content that is a real, order-dependent sequence.

### Don't:
- **Don't** introduce a third spot color; the system is red + blue, full stop.
- **Don't** use a `-bright` color variant as a text or button-fill color — it fails contrast by design and exists for decoration only.
- **Don't** add a kicker/eyebrow label above any heading.
- **Don't** add a colored `border-left`/`border-right` accent above 1px to any card, row, or callout.
- **Don't** add `box-shadow` anywhere; separation comes from a 2px solid ink border.
- **Don't** apply numbered badges to parallel/categorical content (e.g., a 3-item feature list) — that implies a false sequence.
