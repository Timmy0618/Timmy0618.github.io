---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Surface: index.html (résumé site)

Mode: Persuade. Audience: recruiter 30-second screen, then engineering manager deep read. Action: email to set up an interview (GitHub secondary). Must keep: zh/EN toggle. Dropped: E-Ink mock panel; dark mode not required.

## Direction contract

THESIS: The résumé is a project ledger — every project one ruled row a recruiter can scan (constraint, stack, result) and a manager can open. Refuses the hero-plus-cards résumé template.
OWN-WORLD: Blueprint drawing paper #e9edf1, navy ink #14202e, cobalt #1f4fd1 as the only spot. Ruled hairlines, 2px ink rule on table heads, IBM Plex Sans TC body, Plex Mono only for data columns, numerals, stacks. No cards, no shadows, no chips.
STORY: In one viewport the reader knows who, current employer, years, and sees five projects with their numbers; they open a row for architecture and bullets; they email.
FIRST VIEWPORT: Name ~84px top-left with positioning line; top-right facts (現職 / 經驗 / 地點 / 兵役) above the cobalt email button; below, the ledger header and rows grouped by employer. Adaptation: all rows load collapsed (not "first row open") so rows 01–05 fit in 1440x900 and STORY holds; hover and open states use the cobalt numeral + card ground.
FORM: Project Ledger, position 4 on the ranked list (dealt lead). seed:53a148c70fd546d7
Signature interaction: row expand with height transition + expand-all control; Mermaid architecture renders on first open.
FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance

Dropped ceiling item: orthogonal/straight diagram edges. Mermaid 11.4.1 ignores flowchart.curve (initialize, %%{init}%% directive) and linkStyle interpolate in this renderer; edges stay splines.
