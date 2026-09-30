---
name: Antares
description: Reproductor de música para Windows, ligero y sin anuncios.
colors:
  ink: "#08090b"
  surface: "#101216"
  surface-raised: "#14171c"
  surface-active: "#1a1e24"
  hairline: "#21252c"
  hairline-strong: "#2d323b"
  text: "#e7e9ec"
  text-dim: "#9aa1ac"
  text-faint: "#8b929d"
  track: "#1d2127"
  steel-blue: "hsl(213 49% 71%)"
  steel-blue-bright: "hsl(213 55% 79%)"
  on-accent: "#0a0d11"
  ember: "#e0533d"
typography:
  display:
    fontFamily: "Inter, Segoe UI Variable, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(2.35rem, 1rem + 3.2vw, 4.25rem)"
    fontWeight: 600
    lineHeight: 0.98
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "Inter, Segoe UI Variable, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(2.1rem, 1.1rem + 3vw, 4rem)"
    fontWeight: 600
    lineHeight: 1.02
    letterSpacing: "-0.04em"
  title:
    fontFamily: "Inter, Segoe UI Variable, Segoe UI, system-ui, sans-serif"
    fontSize: "21px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  body:
    fontFamily: "Inter, Segoe UI Variable, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Inter, Segoe UI Variable, Segoe UI, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 500
    letterSpacing: "0.34em"
rounded:
  control: "10px"
  panel: "16px"
  cell: "20px"
  feature: "28px"
  pill: "999px"
spacing:
  gutter: "clamp(16px, 4vw, 48px)"
  section: "clamp(104px, 13vw, 176px)"
  cell-pad: "24px"
components:
  button-primary:
    backgroundColor: "{colors.steel-blue}"
    textColor: "{colors.on-accent}"
    rounded: "{rounded.pill}"
    padding: "14px 22px"
    height: "52px"
  button-primary-hover:
    backgroundColor: "{colors.steel-blue-bright}"
  button-ghost:
    backgroundColor: "rgb(255 255 255 / 0.03)"
    textColor: "{colors.text}"
    rounded: "{rounded.pill}"
    padding: "14px 22px"
  feature-cell:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.cell}"
    padding: "{spacing.cell-pad}"
  player-button:
    backgroundColor: "{colors.steel-blue}"
    textColor: "{colors.on-accent}"
    rounded: "{rounded.pill}"
    size: "52px"
---

# Design System: Antares

## Overview

**Creative North Star: "The Player Is the Page"**

The landing is built from Antares's own interface rather than around a screenshot of it. The palette is the app's Grafito theme, the type is the Inter it bundles, the icons are the app's own stroke paths, and the demo player reuses its player bar. Visitors should feel they already opened the app.

Depth is dark and quiet: near-black grounds, three surface steps, hairline borders, and slow aurora fields of steel blue, navy and a little ember behind everything. The one accent is steel blue, and like the app's Carátula theme it can glide to the hue of the cover that is playing. The ember red appears only where the logo's pulse appears.

**Key Characteristics:**
- Real UI fragments instead of icon cards.
- One accent, tone and saturation only; lightness is fixed so it always reads on the dark ground.
- Big, tight Inter headlines; body copy in dim grey at a comfortable measure.
- Motion explains behavior (lyrics advancing, EQ presets, queue insertion), never decorates idle space.

## Colors

A graphite night with one steel-blue voice and an ember pulse.

### Primary
- **Steel Blue** (steel-blue): primary buttons, active states, progress, focus rings, the visualizer. Declared as hue and saturation (`--accent-h`, `--accent-s`) so it can shift to a cover's hue with a 600 ms registered-property transition.

### Secondary
- **Ember Pulse** (ember): the logo's sound wave. Used for the marquee separators, the footer meter and the import progress bar. Never on buttons or text.

### Neutral
- **Ink** (ink): page ground.
- **Graphite Surface / Raised / Active** (surface, surface-raised, surface-active): cells, panels, active rows and tabs, in that order of elevation.
- **Hairline / Hairline Strong** (hairline, hairline-strong): borders and dividers; the strong one for control outlines.
- **Text / Dim / Faint** (text, text-dim, text-faint): headings, body copy, and metadata. Faint is the floor for legible text on tinted areas.

### Named Rules
**The Fixed Lightness Rule.** The accent changes hue and saturation only; its lightness stays at 71 % so contrast with ink never depends on the cover.
**The Ember Is the Logo Rule.** The red only marks the sound pulse; it never becomes a second action color.

## Typography

**Display Font:** Inter (with Segoe UI Variable, system-ui)
**Body Font:** Inter
**Label/Mono Font:** Cascadia Mono / Consolas, only for real code (the recommender formula, file paths).

**Character:** One family at two voices: display at weight 600 with heavy negative tracking, and the app's wide-tracked uppercase wordmark (0.34em) as the brand signature.

### Hierarchy
- **Display** (600, clamp(2.35rem…4.25rem), 0.98): the hero line only; second phrase in text-dim.
- **Headline** (600, clamp(2.1rem…4rem), 1.02): one per section, max 16ch, no eyebrow above it.
- **Title** (600, 21px, 1.2): feature cells and cards.
- **Body** (400, 17px, 1.55): lead paragraphs up to 34em, in text-dim.
- **Label** (500, 13px, 0.34em, uppercase): the ANTARES wordmark only.

### Named Rules
**The No Eyebrow Rule.** Section headlines stand alone; small uppercase kickers above them are not part of this system.

## Layout

Content sits in a 1240 px container with a fluid gutter (16 to 48 px) and generous section spacing (104 to 176 px). The hero is a two-column split above 1180 px (copy left, the 3D app window bleeding off the right edge) and stacks below it. The feature grid is a four-column bento with mixed spans, collapsing to two columns under 1100 px and one under 720 px. The horizontal page never scrolls: the hero clips its own overflow.

## Elevation & Depth

Depth comes from tonal layering (ink, surface, raised, active) and hairlines, not shadows. Shadows are neutral black and reserved for things that float: the hero window, the mini player, and pressed controls.

### Shadow Vocabulary
- **Float** (`0 40px 80px -20px rgb(0 0 0 / 0.7)`): the hero window.
- **Lift** (`0 6px 16px -6px rgb(0 0 0 / 0.6)`): primary button.

### Named Rules
**The Neutral Shadow Rule.** Shadows are black, never tinted with the accent; the only colored light is the aurora and the glow behind the hero window.

## Shapes

Soft, consistent corners from the app's radius scale: 10 px for controls and search fields, 16 px for panels, 20 px for feature cells, 28 px for the download panels, full pills for buttons and chips. Album art is always a rounded square.

## Components

### Buttons
- **Shape:** full pill (999px), 52 px tall in content, 40 px in the nav.
- **Primary:** steel-blue fill with on-accent text; can carry a second line (version and size) in 12 px.
- **Hover / Focus:** brighter accent on hover (pointer devices only); 2 px accent outline on focus-visible; scale(0.97) on press.
- **Ghost:** 3 % white fill, hairline-strong border, optional "Pronto" tag chip.

### Chips
- **Style:** accent wash background with accent text, 11 to 13 px, for status like "Pronto" and "Próximamente".

### Cards / Containers
- **Corner Style:** 20 px (cells), 28 px (download).
- **Background:** graphite surface with a faint top highlight; some cells carry a steel or ember radial tint.
- **Border:** 1 px hairline; on hover a 260 px spotlight ring follows the cursor.
- **Internal Padding:** 24 px (20 px on mobile).

### Navigation
- Fixed 68 px bar; transparent over the hero, blurred ink after scrolling. Links 15 px text-dim, pill hover; links hide under 960 px and the Download button stays.

### Player Bar (signature)
- The app's own controls: previous, play in a 52 px accent circle, next, a 4 px seek track filled with the accent, like, mute and volume. Volume follows a cubic curve like the app.

## Do's and Don'ts

### Do:
- **Do** build sections from real Antares UI fragments with the app's icon paths.
- **Do** keep the accent at 71 % lightness and change only hue and saturation.
- **Do** honor prefers-reduced-motion: no drift, no marquee movement, no tilt; opacity changes only.

### Don't:
- **Don't** add eyebrows or section numbers above headlines.
- **Don't** use accent-colored glows or shadows on buttons.
- **Don't** introduce a second action color; ember is reserved for the logo pulse.
