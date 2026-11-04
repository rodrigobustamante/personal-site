---
name: Rodrigo Bustamante — Personal Site
description: An annotated atlas of systems work. Serif editorial type and isometric dioramas over a cool indigo field, with one saturated accent.
colors:
  starlight-paper: 'oklch(0.975 0.01 270)'
  starlight-paper-2: 'oklch(0.945 0.016 272)'
  starlight-card: 'oklch(0.993 0.004 270)'
  indigo-ink: 'oklch(0.25 0.06 278)'
  indigo-ink-soft: 'oklch(0.38 0.06 278)'
  indigo-muted: 'oklch(0.47 0.045 276)'
  indigo-faint: 'oklch(0.6 0.035 274)'
  indigo-line: 'oklch(0.88 0.022 272)'
  indigo-line-soft: 'oklch(0.925 0.016 272)'
  nebula-magenta: 'oklch(0.55 0.21 355)'
  nebula-magenta-ink: 'oklch(0.5 0.2 355)'
  sun-amber: 'oklch(0.64 0.15 64)'
  aurora-teal: 'oklch(0.6 0.1 195)'
  night-sky-indigo: 'oklch(0.2 0.05 278)'
  night-sky-indigo-2: 'oklch(0.235 0.058 280)'
  night-sky-card: 'oklch(0.255 0.062 281)'
  starlight-ink: 'oklch(0.96 0.014 260)'
  nebula-magenta-night: 'oklch(0.72 0.18 355)'
  nebula-magenta-ink-night: 'oklch(0.8 0.13 355)'
  paper-cream: 'oklch(0.972 0.013 79)'
  paper-ink: 'oklch(0.27 0.018 55)'
  paper-terracotta: 'oklch(0.565 0.125 42)'
typography:
  display:
    fontFamily: "'Newsreader', Georgia, 'Times New Roman', serif"
    fontSize: 'clamp(48px, 10vw, 104px)'
    fontWeight: 400
    lineHeight: 0.96
    letterSpacing: '-0.025em'
  headline:
    fontFamily: "'Newsreader', Georgia, 'Times New Roman', serif"
    fontSize: 'clamp(32px, 5vw, 50px)'
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: '-0.02em'
  title:
    fontFamily: "'Newsreader', Georgia, 'Times New Roman', serif"
    fontSize: 'clamp(24px, 3.2vw, 32px)'
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: '-0.015em'
  lede:
    fontFamily: "'Newsreader', Georgia, 'Times New Roman', serif"
    fontSize: 'clamp(20px, 2.6vw, 28px)'
    fontWeight: 300
    lineHeight: 1.42
  body:
    fontFamily: "'Hanken Grotesk', system-ui, -apple-system, sans-serif"
    fontSize: '17px'
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "'Hanken Grotesk', system-ui, -apple-system, sans-serif"
    fontSize: '12px'
    fontWeight: 600
    letterSpacing: '0.08em'
rounded:
  focus: '4px'
  chip: '6px'
  item: '8px'
  panel: '14px'
  pill: '999px'
spacing:
  page-pad: 'clamp(20px, 5vw, 64px)'
  content-max: '1080px'
  section-y: 'clamp(64px, 9vh, 110px)'
  section-head: 'clamp(40px, 6vh, 64px)'
components:
  button-primary:
    backgroundColor: '{colors.nebula-magenta}'
    textColor: '{colors.starlight-card}'
    rounded: '{rounded.pill}'
    height: '50px'
    padding: '0 24px'
  button-ghost:
    textColor: '{colors.indigo-ink}'
    rounded: '{rounded.pill}'
    height: '50px'
    padding: '0 24px'
  button-ghost-hover:
    backgroundColor: '{colors.starlight-card}'
  tool-button:
    textColor: '{colors.indigo-ink-soft}'
    rounded: '{rounded.pill}'
    height: '36px'
    padding: '0 12px'
  chip:
    backgroundColor: '{colors.starlight-card}'
    textColor: '{colors.indigo-ink-soft}'
    rounded: '{rounded.chip}'
    padding: '4px 11px'
  highlight-pill:
    textColor: '{colors.nebula-magenta-ink}'
    rounded: '{rounded.pill}'
    padding: '5px 12px 5px 10px'
  work-card:
    backgroundColor: '{colors.starlight-paper-2}'
    rounded: '{rounded.chip}'
    padding: '28px 28px 24px'
  nav-link:
    textColor: '{colors.indigo-ink-soft}'
    typography: '{typography.body}'
    padding: '4px 0'
---

# Design System: Rodrigo Bustamante — Personal Site

## Overview

**Creative North Star: "The Annotated Atlas"**

The site reads like an atlas of systems Rodrigo has built: each plate is an isometric diorama, each caption a serif title, and each figure (years, teams, passengers) a piece of evidence set in the margin. Type does the editorial work, the dioramas do the explaining, and the chrome stays out of the way. The default **Cosmos** style sets this on a cool indigo field with one saturated accent and two illustration-only companions, after the flat, saturated look of Kurzgesagt illustrations. **Paper** is the alternative style: the site's original warm cream with earthy accents.

Density is low and the rhythm unhurried: one 1080px column, generous section spacing, thin rules between sections. Components are precise and quiet, with fine 1px borders and small radii. Fills and shadows are reserved for the one action that matters on a screen. The accent earns its place: it marks the primary action, the current location, and small editorial details (section numbers, highlight pills, link underlines), never large surfaces.

The system is fully themed: two styles (Cosmos, Paper), each with light and dark modes and a runtime-switchable accent. Every combination keeps WCAG AA contrast, and the `/system` page renders the live tokens and components.

**Key Characteristics:**

- Serif display (Newsreader) over a grotesque body (Hanken Grotesk); italic serif for small editorial marks.
- Cool indigo neutrals with a single saturated accent; amber and teal companions only inside illustrations.
- Flat surfaces separated by tone and 1px lines; shadows are rare and tied to state or floating layers.
- Pills for actions and tools, small 6px corners for content containers and chips.
- Motion is short and directional (reveal on scroll, arrows nudging the way they point), and fully disabled under `prefers-reduced-motion`.

## Colors

A cool, low-chroma indigo field carrying one high-chroma accent, all authored in OKLCH so every theme and accent keeps predictable contrast.

### Primary

- **Nebula Magenta** (`nebula-magenta`): Cosmos's default accent. It fills the primary button, colours the wordmark dot, the nav underline and the active-link marker, and draws hover borders on work cards. In dark mode it lightens to **Nebula Magenta, Night** (`nebula-magenta-night`).
- **Nebula Magenta Ink** (`nebula-magenta-ink`): the accent's text variant, used for small accent text on paper (section numbers, highlight pills, case-study links, the active language) and for the focus outline. In dark mode, **Nebula Magenta Ink, Night** (`nebula-magenta-ink-night`).
- **Accent soft** (12% of the accent in light mode, 16% in dark, mixed in OKLab): pill backgrounds and the `::selection` background.

The accent can be switched at runtime. Cosmos offers Magenta (default), Coral, Amber, Teal, Sky and Violet; Paper offers Terracotta (default), Ochre, Olive, Indigo and Plum. Each one ships four values: accent and ink, for light and dark (`src/utils/palettes.ts`).

### Secondary

- **Sun Amber** (`sun-amber`) and **Aurora Teal** (`aurora-teal`): the illustration companions to Magenta (`--accent-2`, `--accent-3`), so the dioramas keep three distinct hues. Every Cosmos accent carries its own pair. In Paper both companions collapse into the accent.

### Neutral

- **Starlight Paper** (`starlight-paper`): page background in Cosmos light.
- **Starlight Paper 2** (`starlight-paper-2`): the recessed tone for work cards, hover rows and quiet panels.
- **Starlight Card** (`starlight-card`): raised surfaces (chips, popovers, ghost-button hover) and the near-white text on the primary button.
- **Indigo Ink** (`indigo-ink`): headings and primary text. **Indigo Ink Soft** (`indigo-ink-soft`): nav links, chip text, card body. **Indigo Muted** (`indigo-muted`): sub-headings, meta and footer. **Indigo Faint** (`indigo-faint`): de-emphasised marks only, never body text.
- **Indigo Line** (`indigo-line`): borders on buttons, chips and the scrolled header. **Indigo Line Soft** (`indigo-line-soft`): rules between sections and card borders.
- **Night Sky Indigo** (`night-sky-indigo`, `night-sky-indigo-2`, `night-sky-card`) with **Starlight Ink** (`starlight-ink`): the same roles in Cosmos dark.
- **Paper Cream** (`paper-cream`), **Paper Ink** (`paper-ink`) and **Paper Terracotta** (`paper-terracotta`): the Paper style's base pair and default accent, warm counterparts to the Cosmos roles.

### Named Rules

**The Ink-for-Text Rule.** Small accent text always uses the ink variant (`--accent-ink`), never the raw accent; the raw accent is for fills, rules and marks. The ink variant is what keeps AA contrast on paper and card.

**The Illustration-Only Companions Rule.** `--accent-2` and `--accent-3` exist for dioramas and figures. UI chrome uses the accent alone.

**The Every-Combination Rule.** A new colour role must hold AA contrast in all four style × mode combinations and with every accent before it ships.

## Typography

**Display Font:** Newsreader (with Georgia, 'Times New Roman', serif)
**Body Font:** Hanken Grotesk (with system-ui, -apple-system, sans-serif)

**Character:** A literary, optical-size serif for anything that names or claims something, paired with a clean, slightly warm grotesque for reading and UI. The serif's italic is the editorial marker, used for small notes rather than emphasis in prose.

Both families are self-hosted, subset and instanced (Newsreader 300–500 with italics, Hanken Grotesk 400–600).

### Hierarchy

- **Display** (400, `clamp(48px, 10vw, 104px)`, 0.96, −0.025em): the hero name only.
- **Headline** (400, `clamp(32px, 5vw, 50px)`, 1.02, −0.02em): section titles, case-study and page titles.
- **Title** (500, `clamp(24px, 3.2vw, 32px)`, 1.1, −0.015em): company names in the experience timeline. Work-card titles use 400 at `clamp(24px, 3vw, 32px)`; post titles use 500 at 24px (19px on phones).
- **Lede** (serif 300, `clamp(20px, 2.6vw, 28px)`, 1.42): the hero pitch.
- **Body** (17px, 1.6): all prose and UI. Section subtitles use 19px in muted ink with a 56ch measure. Nav links are 14px; chips, tool buttons and meta are 13px.
- **Label** (600, 12px, 0.08em tracking, uppercase): eyebrow tags such as WORK above page titles.
- **Section number** (serif italic, 16px, accent ink): the `01`, `02` markers above section titles.

### Named Rules

**The Serif-Names-Things Rule.** Serif is for names, titles, figures and claims; sans is for reading and operating. A button, label or nav link is never serif.

**The Pretty-Wrap Rule.** Prose and subtitles use `text-wrap: pretty`; dates and periods use tabular numerals.

## Layout

A single centred column (max 1080px) with fluid side padding (`clamp(20px, 5vw, 64px)`). Sections breathe vertically (`clamp(64px, 9vh, 110px)`), and consecutive sections are separated by a 1px soft rule rather than background changes. Section heads sit `clamp(40px, 6vh, 64px)` above their content.

Groups (nav, chips, stats, CTAs, card lists) are laid out with flex or grid and `gap`, never per-item margins. The sticky header is transparent at rest and turns into a blurred, 85% paper bar with a bottom rule once the page scrolls.

Responsive behaviour: below 900px the inline nav gives way to a menu button that opens a popover with the same links. Below 480px the wordmark drops its dot and the header tools tighten into icon-only 36px circles, and below 400px the style toggle moves into the menu. Long content (case studies, posts) narrows its measure rather than widening the column.

## Elevation & Depth

Depth is mostly tonal: paper → paper-2 (recessed) → card (raised), with 1px lines doing the separating. Shadows exist but are scarce: today they are the primary button's accent glow on hover and the mobile menu's soft drop. This is the current tendency, not a ban; a new component may use a shadow when it floats above the page or responds to a state.

### Shadow Vocabulary

- **Accent glow** (`box-shadow: 0 10px 26px -10px color-mix(in oklab, var(--accent) 70%, transparent)`): primary button hover only.
- **Floating layer** (`box-shadow: 0 18px 40px -20px color-mix(in oklab, var(--ink) 40%, transparent)`): popovers such as the mobile menu.
- **Active marker** (`box-shadow: inset 2px 0 0 var(--accent)`): the current link inside the mobile menu. A line, not a lift.

### Named Rules

**The Tone-Before-Shadow Rule.** Reach for a tonal step or a 1px line before a shadow. If a shadow is used, derive its colour from `--ink` or `--accent` with `color-mix`, never a neutral grey or black.

## Shapes

Two families of corners: fully rounded pills (999px) for anything you press in the chrome (buttons, header tools, highlight pills, skip link), and small, near-square corners (6px) for content (chips, work cards, tooltips, the portrait). Rows inside menus use 8px, and floating panels use 14px. Focus outlines are 2px in accent ink with a 3px offset and a 4px radius.

Borders are 1px throughout. Underlines (1px, accent) mark links and the current nav item; they draw in from the left on hover.

## Components

### Buttons

Precise and quiet: a pill with a fine border, where only the primary action gets a fill.

- **Shape:** full pill (999px), 50px tall, 24px side padding, 16px/500 text, 17px icons with a 9px gap.
- **Primary:** accent fill, accent border, on-accent text (near-white on light, deep indigo on dark).
- **Ghost:** transparent with a 1px line border and ink text; on hover the border darkens to ink-soft and the fill becomes card.
- **Hover / Focus:** a 1px lift (motion permitting); the primary adds the accent glow. Focus is the global accent-ink outline.

### Header tools

- **Style:** 36px pills with a 1px line border, 13px ink-soft text or a 16px stroke icon (1.7 stroke). On hover the border and text darken to ink.
- **Tooltips:** on hover-capable devices only, a small ink chip with paper text (12px/500, 6px radius) appears below and right-aligned after 350ms.
- **Language toggle:** shows `EN / ES` with the current language in accent ink at 600 weight and the other one muted.

### Chips

- **Style:** 13px ink-soft text on card, 1px line border, 6px radius, 4px 11px padding, no wrap.
- **Highlight pill:** a pill in accent-soft with accent-ink 13px/500 text and a small leading mark, used for one standout achievement per entry.
- **Motion:** in a revealed stack, chips cascade in 35ms apart.

### Cards / Containers

- **Corner Style:** 6px.
- **Background:** paper-2, with a 1px line-soft border.
- **Shadow Strategy:** none; hover swaps the border to the accent and nudges the CTA arrow 4px.
- **Internal Padding:** 28px on the sides and top, 24px at the bottom.

### Navigation

- **Desktop:** 14px ink-soft links with 26px gaps. Hover darkens to ink and draws a 1px accent underline in from the left. The current section (`aria-current="page"`) keeps ink colour and a full underline.
- **Mobile:** below 900px a menu button opens a popover (card, 1px line, 14px radius, floating-layer shadow) holding the same links as 16px rows with 8px radius and a paper-2 hover. The current link carries a 2px inset accent bar.
- **One menu everywhere:** Experience, Work, Skills, Blog, Contact on every page.

### Isometric dioramas (signature)

Flat SVG plates drawn on an isometric grid (`src/components/portfolio/dioramas`), one per case study plus Santiago and Madrid on the home page. They are coloured only through `--accent`, `--accent-2` and `--accent-3` plus neutral tones, so they follow the active style, mode and accent. Small loops (trucks, cranes, planes) run only with `prefers-reduced-motion: no-preference` and pause when off-screen.

## Do's and Don'ts

### Do:

- **Do** author new colours in OKLCH and check them in Cosmos and Paper, light and dark, against paper and card.
- **Do** use `--accent-ink` for any accent-coloured text and `--accent` for fills, rules and marks.
- **Do** separate sections with the 1px soft rule and the `clamp(64px, 9vh, 110px)` rhythm instead of alternating backgrounds.
- **Do** keep actions as pills and content as 6px containers.
- **Do** gate every transform and animation behind `prefers-reduced-motion: no-preference`, and use the `cubic-bezier(0.2, 0.7, 0.2, 1)` ease for reveals.
- **Do** show new tokens or components on `/system` when they become part of the system.

### Don't:

- **Don't** use the accent as a large background or section fill; it marks, it doesn't flood.
- **Don't** use the illustration companions (`--accent-2`, `--accent-3`) in UI chrome.
- **Don't** set buttons, labels or navigation in the serif.
- **Don't** add gradients or emoji to the interface.
- **Don't** hard-code hex or neutral-grey shadows; derive from the tokens with `color-mix`.
