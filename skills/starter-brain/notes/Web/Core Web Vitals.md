---
id: core-web-vitals
type: concept
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "The three user-experience metrics Google uses for loading, responsiveness and visual stability, with their good thresholds at the 75th percentile of page loads."
sources:
  - url: "https://web.dev/articles/vitals"
    date: 2024-10-31
    title: Web Vitals - web.dev
  - url: "https://developers.google.com/search/docs/appearance/core-web-vitals"
    date: 2025-12-10
    title: Understanding Core Web Vitals and Google search results - Google Search Central
confidence: high
superseded_by:
tags: [ux-performance, technical-seo, analytics-legal]
fingerprint: 4d617d07b968
trust: high
author: Google (web.dev and Google Search Central)
year: 2025
---
# Core Web Vitals

> [!summary] TL;DR
> Three metrics: LCP (loading) 2.5 s or less, INP (responsiveness) 200 ms or less, CLS (stability) 0.1 or less.
> Judged at the 75th percentile of page loads, mobile and desktop separately.
> Google says good values align with what its ranking systems reward; it does not call them an explicit ranking signal.

## Explanation
Core Web Vitals (CWV) are three metrics that web.dev calls user-centric: Largest Contentful Paint (LCP) for loading, Interaction to Next Paint (INP) for responsiveness and Cumulative Layout Shift (CLS) for visual stability. Good values: LCP 2.5 s or less, INP 200 ms or less, CLS 0.1 or less. They are measured at the 75th percentile of page loads, split by mobile and desktop.

## What Google says
Google's Search documentation recommends good CWV for success in Search. It says page experience 'aligns with what our core ranking systems seek to reward'. It does not call the metrics an explicit ranking signal, so treat them as a quality bar, not a rank lever.

## How to use it
- Read field data first (Lab data vs field data). Search Console has a Core Web Vitals report for this.
- Use Lighthouse lab runs to debug a single page.
- Set a Performance budget per page template so regressions show before launch.

## Trust & evidence
The thresholds appear on two primary Google-owned pages (web.dev and Google Search Central) that agree, so confidence is high. The 'INP replaced FID in March 2024' date comes from the crawl queue and was not confirmed on the pages opened.

## Related
Chrome UX Report (CrUX) · Playbook - Performance budget template · Directory - UX, Accessibility & Performance

## Sources
- [Web Vitals - web.dev](https://web.dev/articles/vitals) · 2024-10-31
- [Understanding Core Web Vitals and Google search results - Google Search Central](https://developers.google.com/search/docs/appearance/core-web-vitals) · 2025-12-10
