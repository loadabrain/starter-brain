---
id: playbook-media-performance-checklist
type: concept
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "A pre-launch checklist for images, video and fonts, each item tied to the note that sources it."
sources:
  - url: "https://web.dev/articles/browser-level-image-lazy-loading"
    date: 2024-08-13
    title: Browser-level image lazy loading for the web - web.dev
  - url: "https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/video"
    date: 2026-10-21
    title: video - HTML video embed element - MDN
  - url: "https://web.dev/articles/font-best-practices"
    date: 2022-10-04
    title: Best practices for fonts - web.dev
confidence: medium
superseded_by:
tags: [ux-performance, frontend, resources]
fingerprint: 411d9e457968
trust: high
author: "Playbook built from primary sources (web.dev, MDN, Apple)"
year: 2026
---
# Playbook - Media performance checklist

> [!summary] TL;DR
> Images: modern format with fallback, dimensions set, lazy only below the fold, LCP image eager.
> Video: sized muted poster, preload none or metadata below the fold, HLS for long films.
> Fonts: font-display chosen, WOFF2 subset, preconnect, size-adjust for swap.

## Use
Run before any site that carries photos, hero video or custom fonts goes to review. Each item links to its source note; items marked (opinion) are practice, not sourced.

## Images
- [ ] Modern format (AVIF or WebP) with a JPEG or PNG fallback through the picture element (Image formats - AVIF and WebP).
- [ ] width and height set on every img (Responsive images and lazy loading).
- [ ] Hero or LCP image is NOT lazy-loaded; it uses default loading (Responsive images and lazy loading).
- [ ] Images below the first viewport use loading=lazy.
- [ ] Responsive sizes (srcset and sizes) so phones do not download desktop files (sourced to the Learn Images course; detail unsourced).

## Video
- [ ] Every video has a sized poster image (Video poster, autoplay and preload).
- [ ] Hero video is muted and plays inline; no autoplay with sound.
- [ ] preload=none or metadata for videos below the fold.
- [ ] Long films considered for HLS (HLS adaptive streaming).
- [ ] Tested on a real iPhone and Android mid-range phone (opinion: no source for device rules here).

## Fonts
- [ ] font-display chosen on purpose (Web font loading).
- [ ] Fonts subset to WOFF2; variable font where it replaces several files.
- [ ] Preconnect to any third-party font origin; preload only the one or two critical files.
- [ ] size-adjust set on the fallback to limit swap shift (Cumulative Layout Shift (CLS)).
- [ ] Font licence checked for self-hosting (see the Design Resources theme).

## Check the result
- [ ] Lighthouse lab run (Lighthouse) and field check in Chrome UX Report (CrUX) when data exists.
- [ ] Largest Contentful Paint (LCP) within 2.5 s target; Cumulative Layout Shift (CLS) 0.1 or less.

## Related
Playbook - Performance budget template · Directory - UX, Accessibility & Performance

## Sources
- [Browser-level image lazy loading for the web - web.dev](https://web.dev/articles/browser-level-image-lazy-loading) · 2024-08-13
- [video - HTML video embed element - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/video) · 2026-10-21
- [Best practices for fonts - web.dev](https://web.dev/articles/font-best-practices) · 2022-10-04
