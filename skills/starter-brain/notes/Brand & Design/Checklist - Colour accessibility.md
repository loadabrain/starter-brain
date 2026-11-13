---
id: checklist-colour-accessibility
type: concept
status: active
created: 2026-11-03
updated: 2026-11-03
summary: "Tick-list for a brand or UI palette: contrast pairs, non-colour cues, colour-blind simulation, dark mode, logo and documentation."
sources:
  - url: "https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html"
    date: 2026-11-03
  - url: "https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html"
    date: 2026-11-03
confidence: medium
superseded_by:
tags: [colour, accessibility, checklist, verify-colour]
fingerprint: 117be2cf2e0e
trust: high
checked: 2026-11-03
---
# Checklist - Colour accessibility

> [!summary] TL;DR
> Test every text/background and UI/background pair against WCAG 2.2 AA.
> Never let colour carry meaning alone; simulate colour blindness.
> Write the approved pairs into the guidelines, with ratios.

Ground rules: [[WCAG 2.2 colour contrast rules (1.4.3, 1.4.11, 1.4.1)]], Colour vision deficiency for designers. Tick each:

- [ ] **Text pairs:** every approved text/background pair is at least 4.5:1 (3:1 only for 18 pt / 14 pt bold and larger). Write the ratio next to each pair.
- [ ] **Brand colour as text:** the main brand colour on white is checked; if it fails, define a darker 'text' variant instead of recolouring the brand.
- [ ] **UI parts:** borders of inputs, icons that carry meaning, focus rings and selected states reach 3:1 against neighbours.
- [ ] **Links:** distinguishable by more than colour (underline), or 3:1 against body text plus another cue on focus/hover.
- [ ] **Colour alone:** error/success, charts, status chips have a label, icon or pattern.
- [ ] **Simulation:** protan, deutan, tritan and greyscale views reviewed.
- [ ] **Light and dark:** the pairs are tested again in the dark version; do not just invert (APCA and WCAG 3 status for a second opinion).
- [ ] **Text on images and gradients:** test the worst spot, or put a scrim behind.
- [ ] **Logo:** exempt from contrast rules for text in logotypes, but keep a version for dark and light backgrounds (Checklist - Logo test).
- [ ] **Documentation:** pairs, ratios and forbidden combinations are in the brand guidelines.
- [ ] **Law:** if you sell online in the EU, check European Accessibility Act and brand colours.

Note: this is a synthesis of the cited standards, not a standard itself.

## History
- 2026-11-03: Verify pass: thresholds match the W3C pages re-read today.

## Sources
- [https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) · 2026-11-03
- [https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html) · 2026-11-03
