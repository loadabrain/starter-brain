---
id: wcag-22-colour-contrast-rules
type: concept
status: active
created: 2026-11-03
updated: 2026-11-03
summary: "WCAG 2.2 AA: 4.5:1 for normal text, 3:1 for large text and for UI components and meaningful graphics; logotypes exempt; colour alone must not carry meaning."
sources:
  - url: "https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html"
    date: 2026-11-03
  - url: "https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html"
    date: 2026-11-03
  - url: "https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html"
    date: 2026-11-03
confidence: high
superseded_by:
tags: [colour, accessibility, wcag, verify-colour]
fingerprint: cf80ea491b10
trust: high
author: W3C WAI
year: 2023
checked: 2026-11-03
---
# WCAG 2.2 colour contrast rules (1.4.3, 1.4.11, 1.4.1)

> [!summary] TL;DR
> Text: 4.5:1 (3:1 if 18 pt / 14 pt bold or larger); no rounding, 4.499 fails.
> UI components, states and meaningful graphics: 3:1 against neighbours (SC 1.4.11).
> Logotypes and disabled controls are exempt; never use colour alone for meaning (SC 1.4.1).

## The rules
- **SC 1.4.3 Contrast (Minimum), AA:** normal text at least 4.5:1; large-scale text at least 3:1. Large = 18 pt, or 14 pt bold (about 24 px and 18.5 px). Ratios are not rounded: 4.499:1 fails.
- **SC 1.4.11 Non-text Contrast, AA:** 3:1 against adjacent colours for what is needed to identify a control and its state (focus, selected) and for parts of graphics needed to understand content.
- **SC 1.4.1 Use of Color, A:** colour must not be the only way to show information, an action or a difference; add text, shape or pattern. Inline links that differ from body text only by colour need 3:1 against the surrounding text (technique G183).

## Exemptions that matter for brands
- Text that is part of a logo or brand name has no contrast requirement (1.4.3).
- Disabled controls, pure decoration, and text inside photos have no requirement.
- 1.4.11 also treats logos as essential presentation, but a logo used as a control still needs a visible focus indicator, and a low-contrast logo version chosen by the author is not exempt.
- Hover effects are supplemental but must not reduce contrast.

## How the ratio is computed
Contrast ratio = (L1 + 0.05) / (L2 + 0.05), L1 the lighter colour's relative luminance, computed from linearised sRGB with weights of about 0.2126 R, 0.7152 G, 0.0722 B. Because it works on sRGB luminance, it says nothing about hue and is known to overrate contrast for dark colours; see APCA and WCAG 3 status.

## Why it matters (evidence)
The thresholds are a standard, not a law of perception; the W3C documents are the normative text (high trust). Laws point at WCAG 2.x, so this is what a brand is measured against today: see European Accessibility Act and brand colours.

## Use
Run [[Checklist - Colour accessibility]] on every palette pair. Build pairs by lightness, not by eye (Oklab and OKLCH).

## History
- 2026-11-03: Verify pass: 4.5:1, 3:1 large text (18 pt / 14 pt bold), logotype exception, no rounding re-read on the W3C Understanding page.

## Sources
- [https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) · 2026-11-03
- [https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) · 2026-11-03
- [https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html) · 2026-11-03
