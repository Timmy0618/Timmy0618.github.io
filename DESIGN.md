---
name: 趙奕錡 YICHI Chao — Résumé
description: A ruled project ledger on blueprint paper; one cobalt spot, navy ink, Plex type.
colors:
  blueprint-paper: "#e9edf1"
  open-row-ground: "#f3f5f8"
  navy-ink: "#14202e"
  ink-secondary: "#3d4959"
  graphite-muted: "#5f6b7c"
  hairline: "#c9d1db"
  hairline-strong: "#aab5c3"
  cobalt: "#1f4fd1"
  cobalt-ink: "#1a43b3"
  on-cobalt: "#f4f7fc"
  cloud-zone-tint: "#d9e3f7"
typography:
  display:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "clamp(3rem, 7vw, 5.25rem)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.02em"
  display-romanized:
    fontFamily: "IBM Plex Sans Condensed, IBM Plex Sans, sans-serif"
    fontSize: "clamp(1rem, 1.9vw, 1.6rem)"
    fontWeight: 600
    letterSpacing: "0.18em"
  headline:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "clamp(2rem, 4.5vw, 3.25rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  lede:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "clamp(1.125rem, 1.7vw, 1.375rem)"
    fontWeight: 400
    lineHeight: 1.55
  title:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 700
    letterSpacing: "0.01em"
  group-title:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 700
  row-title:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 700
    lineHeight: 1.4
  body:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.65
    fontFeature: "tnum"
  label:
    fontFamily: "IBM Plex Sans, IBM Plex Sans TC, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 500
  data:
    fontFamily: "IBM Plex Mono, ui-monospace, monospace"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.6
  data-result:
    fontFamily: "IBM Plex Mono, ui-monospace, monospace"
    fontSize: "0.9375rem"
    fontWeight: 500
    lineHeight: 1.5
  column-head:
    fontFamily: "IBM Plex Mono, ui-monospace, monospace"
    fontSize: "0.75rem"
    fontWeight: 500
    letterSpacing: "0.1em"
rounded:
  none: "0px"
spacing:
  row-inset: "0.75rem"
  row-block: "0.85rem"
  column-gap: "1.25rem"
  page-gutter: "clamp(1rem, 4.5vw, 4.5rem)"
  section-gap: "clamp(4rem, 9vw, 7rem)"
  container: "1240px"
components:
  button-primary:
    backgroundColor: "{colors.cobalt}"
    textColor: "{colors.on-cobalt}"
    rounded: "{rounded.none}"
    padding: "0.95rem 1.6rem"
  button-primary-hover:
    backgroundColor: "{colors.cobalt-ink}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.navy-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "0.35rem 0.8rem"
  language-switch:
    backgroundColor: "transparent"
    textColor: "{colors.graphite-muted}"
    rounded: "{rounded.none}"
    padding: "0.4rem 0.8rem"
  language-switch-active:
    backgroundColor: "{colors.navy-ink}"
    textColor: "{colors.blueprint-paper}"
  ledger-row:
    backgroundColor: "{colors.blueprint-paper}"
    textColor: "{colors.navy-ink}"
    padding: "0.85rem 0.75rem"
  ledger-row-open:
    backgroundColor: "{colors.open-row-ground}"
---

# Design System: 趙奕錡 YICHI Chao — Résumé

## Overview

**Creative North Star: "The Drafting Ledger"**

The system is a technical drawing sheet that happens to be a résumé. Cool blue-grey paper, navy ink, and a single cobalt spot carry everything; structure comes from ruled lines, not from boxes. Content is set as a ledger: a heavy ink rule opens each table or section, hairlines separate rows, and every project sits on one scannable line that can be opened in place for its full account.

Density is deliberate. Rows are tight (under a centimetre of block padding), columns are fixed, numerals are tabular, and data (stacks, results, dates, row numbers) is set in a monospace so it reads as measurement rather than prose. The page is flat: there is no elevation, no radius, and no container chrome. Depth is limited to a slightly lighter paper ground under a hovered or opened row.

The world rejects the hero-plus-cards résumé template: no cards, no drop shadows, no pill chips, no rounded corners.

**Key Characteristics:**
- Blueprint paper ground, navy ink, cobalt as the only accent.
- Ruled grammar: 2px ink rule heads, 1px hairlines between rows.
- Disclosure rows (`<details>`) with a height transition; the row is the unit of content.
- Plex Sans / Sans TC for language, Plex Mono for data, Plex Sans Condensed only for the romanized name.
- Square corners everywhere; authored 2px-stroke line icons.
- Light and dark. First visit follows the OS (`prefers-color-scheme`); the top-bar sun/moon button (`#theme`, `html[data-theme]`) overrides it and the choice is saved in `localStorage` (`resume-theme`). Diagrams repaint on switch.

## Colors

A cold, low-chroma drafting palette with one saturated cobalt spot; every colour is a custom property on `:root` with a full dark-scheme counterpart.

### Primary
- **Drafting Cobalt** (cobalt): fills the single primary action (the email button), draws row-list bullet ticks, the focus ring, text selection, and diagram zone strokes. It is a fill and line colour, not a text colour.
- **Cobalt Ink** (cobalt-ink): the text-weight cobalt. Used for result values, the open or hovered row numeral, emphasized phrases in the positioning line, link hover, and the closing email address. Also the primary button's hover fill.
- **On Cobalt** (on-cobalt): text on a cobalt fill.

### Neutral
- **Blueprint Paper** (blueprint-paper): page ground, sticky column-head ground, and the factory-edge zone fill in diagrams.
- **Open Row Ground** (open-row-ground): the only tonal step; sits under a hovered summary and the whole body of an open row.
- **Navy Ink** (navy-ink): headings, primary text, 2px rule heads, the expand cross, and the active language segment fill.
- **Ink Secondary** (ink-secondary): body copy inside rows, stack text, group descriptions, the positioning line.
- **Graphite Muted** (graphite-muted): labels, dates, row numerals at rest, column heads, row subtitles, diagram edge lines.
- **Hairline** (hairline): 1px row separators and the top-bar rule.
- **Hairline Strong** (hairline-strong): column-head underline, group-head underline, outlined control borders, dashed diagram divider, node borders.
- **Cloud Zone Tint** (cloud-zone-tint): fill for the server/cloud zone in architecture diagrams; never used outside diagrams.

Dark scheme values live in the sidecar; they invert paper and ink (paper #0d1520, ink #dfe7f0) and lift cobalt to #6f9bff so it holds contrast on the dark ground.

### Named Rules
**The One Spot Rule.** Cobalt is the only hue with chroma. It marks the action, the results, and the state of the row being read. Introducing a second accent breaks the drawing.

**The Fill vs. Ink Rule.** Cobalt (cobalt) is for fills, strokes, and marks; text in cobalt uses cobalt-ink. Never set running text in the fill value.

**The Diagram Token Rule.** Diagram colours come from the same custom properties as the page, resolved at render time for the active scheme. The factory-edge zone is paper with a dashed cobalt stroke (6 4); the cloud/server zone is the cobalt tint with a solid cobalt stroke. No hardcoded diagram colours.

## Typography

**Display Font:** IBM Plex Sans (with IBM Plex Sans TC for Han characters)
**Body Font:** IBM Plex Sans / IBM Plex Sans TC
**Label/Mono Font:** IBM Plex Mono (with ui-monospace); IBM Plex Sans Condensed for the romanized name only

**Character:** One engineering family across three widths. Sans carries language, Mono carries measurements, Condensed carries the romanized name as a spaced, muted caption to the Han display name.

### Hierarchy
- **Display** (700, clamp 3rem to 5.25rem, line-height 1, -0.02em): the Han name only.
- **Display Romanized** (Condensed 600, clamp 1rem to 1.6rem, 0.18em tracking, muted): sits on the display baseline, raised 0.5em; also the brand mark in the top bar.
- **Headline** (700, clamp 2rem to 3.25rem, 1.15): the closing call-to-contact; max 18em measure.
- **Lede** (400, clamp 1.125rem to 1.375rem, 1.55): the positioning line; max 40em, `text-wrap: pretty`. Bold ink for facts, bold cobalt-ink for the single key phrase.
- **Title** (700, 1.5rem): section heads, always sitting on or above a 2px ink rule. A muted 0.875rem `small` may trail the title on the same line.
- **Group Title** (700, 1.25rem): employer group heads inside the ledger.
- **Row Title** (700, 1.0625rem, 1.4): the project name in a row, with a muted 0.875rem subtitle beneath.
- **Body** (400, 16px, 1.65, tabular numerals globally): bullet text inside rows, max 52em.
- **Label** (500, 0.8125rem, muted sans): definition-term labels (現職 / NOW), figure captions, outlined controls.
- **Data** (Mono 400, 0.8125rem, 1.6 to 1.7): stacks, dates, skills values. **Data Result** (Mono 500, 0.9375rem, cobalt-ink): result column and scores.
- **Column Head** (Mono 500, 0.75rem, 0.1em tracking, muted): ledger column heads only.

### Named Rules
**The Mono Means Measurement Rule.** Monospace is reserved for data and the ledger's own apparatus (row numerals, column heads, stacks, results, dates, scores, email, the language switch, diagram labels). Sentences are never set in mono.

**The Bilingual Pair Rule.** Every user-facing string ships as sibling `<span lang="zh">` / `<span lang="en">` elements; `html[data-lang]` hides the inactive one. Type styles are applied to the parent so both languages inherit the same role.

## Layout

A single centred column (max 1240px, fluid gutter clamp 1rem to 4.5rem). The head is a two-column grid: name and positioning on the left, a right-aligned facts row and actions bottom-aligned on the right. The ledger is a fixed six-column grid shared by the column heads and every row summary (numeral 3rem, project 2.3fr, constraint 1.25fr, stack 1.9fr, result 1.35fr, toggle 1.75rem; 1.25rem column gap; 0.75rem inline inset). The column-head band is sticky at the top of the viewport while the ledger scrolls.

Open-row bodies indent to align with the project column (3rem + 2rem left padding). Secondary sections use definition-list rows on a 9rem label column, and pair up in a two-column split on wide screens. Sections are separated by clamp 4rem to 7rem.

Responsive: at 1080px the head stacks and the stack column drops from the summary (it remains in the open body). At 720px the column heads hide, the ledger title takes the 2px ink rule instead, and each summary becomes a numeral / content / toggle grid stacking project, constraint, and result; split sections collapse to one column.

## Elevation & Depth

Flat. There are no shadows anywhere. Depth is expressed only by line weight (2px ink rule over 1px hairlines) and by a single tonal step: the open-row ground under a hovered or opened row. The sticky column-head band uses the paper colour as an opaque ground, not a shadow, to separate itself from scrolling rows.

### Named Rules
**The Ruled Not Raised Rule.** Hierarchy is drawn with rules, never lifted with shadows or containers. If something needs separation, give it a line.

## Shapes

Square. Every rectangle in the system has a 0 radius: the primary button, outlined controls, the language segment, row grounds. Borders are 1px hairlines or 2px ink rules; dashed lines appear only as the 1px divider above a diagram and as the factory-edge zone stroke. Icons are authored inline SVG on a 16-unit grid: 2px stroke, square caps, no fill, sized at 0.95em beside text. The row toggle is a drawn plus built from two 2px bars whose vertical bar rotates flat to a minus when the row opens. List bullets are short 1px cobalt ticks, not glyphs.

## Components

### Buttons
Decisive and square.
- **Shape:** square corners (0).
- **Primary:** cobalt fill, on-cobalt text, Plex Sans 700 at 1.0625rem, generous padding (0.95rem 1.6rem), trailing authored arrow icon. One per screen region; it is the email action.
- **Hover / Focus:** fill shifts to cobalt-ink over 0.2s on the house ease; focus is a 2px cobalt outline offset 3px (global).
- **Outline (expand-all):** transparent, 1px hairline-strong border, label type, ink text; hover turns border cobalt and text cobalt-ink. Its label flips between expand and collapse to reflect state.

### Links
- **Text link:** Plex Sans 500, underline in hairline-strong offset 0.3em; hover turns underline cobalt and text cobalt-ink. External links carry the authored up-right arrow icon.
- **Closing email:** large Mono 500 in cobalt-ink with a 2px underline; hover turns the underline to ink.

### Navigation
A 60px top bar ruled by a hairline: brand mark left (bold Han name plus Condensed romanized name), language switch right. The language switch is a segmented control in a hairline-strong frame; segments are Mono 500 at 0.8125rem, muted at rest, ink on hover, and the active segment is filled navy ink with paper text (`aria-pressed`).

### Ledger Row (signature)
The unit of the system: a native `<details>` with a summary laid on the shared column grid.
- **Rest:** paper ground, 1px hairline below, muted mono numeral, bold row title over muted subtitle, constraint in sans, stack in muted-secondary mono, result in cobalt-ink mono, drawn plus at the end.
- **Hover / Open:** summary ground shifts to open-row ground; the numeral turns cobalt-ink; when open, the plus becomes a minus.
- **Expansion:** the body animates `block-size` from 0 to auto over 0.45s on the house ease (`interpolate-size: allow-keywords`); reduced motion collapses all transitions to near zero.
- **Body:** open-row ground; full stack line in muted mono, bullet list with 1px cobalt ticks (bold ink for key terms), then an optional architecture figure under a 1px dashed hairline with a muted label caption.
- **Group head:** employer name (group title) with role line and a right-aligned mono date range, underlined by hairline-strong. An optional note paragraph may follow.

### Architecture Diagram
Mermaid flowcharts on the `base` theme, rendered the first time their row opens (so labels are measured while visible). Labels are Plex Mono 13px; nodes are paper with hairline-strong borders; edges are muted. Zone classes follow The Diagram Token Rule. Edges remain curved splines in this renderer.

### Definition Rows
Secondary sections (education, languages, skills) use the same ruled grammar outside the ledger: a 2px ink rule under the section title, then rows on a 9rem muted label column with 1px hairlines between. Dates sit right in muted mono; scores in cobalt-ink mono; skill values in data mono.

## Do's and Don'ts

### Do:
- **Do** open every table or section with a 2px navy-ink rule and separate its rows with 1px hairlines.
- **Do** keep cobalt to the email action, results, the active row numeral, list ticks, focus, and diagram zones.
- **Do** set every number, stack, date, and result in Plex Mono; set every sentence in Plex Sans / Sans TC.
- **Do** read every colour from the `:root` custom properties so the dark scheme and diagrams follow automatically.
- **Do** ship every string as a zh/en sibling pair.
- **Do** draw icons as inline 2px-stroke, square-cap SVG.
- **Do** honour `prefers-reduced-motion` for the row transition and smooth scroll.

### Don't:
- **Don't** use cards, drop shadows, pill chips, or rounded corners; this world is ruled and flat.
- **Don't** add a second accent hue or set running text in the cobalt fill value.
- **Don't** use Plex Sans Condensed for anything other than the romanized name.
- **Don't** hardcode colours in Mermaid source; reference the tokens.
- **Don't** substitute glyph characters or icon fonts for the authored SVG icons, plus/minus toggle, or list ticks.
