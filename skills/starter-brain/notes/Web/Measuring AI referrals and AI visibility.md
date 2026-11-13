---
id: measuring-ai-referrals-and-ai-visibility
type: concept
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "Four layers of AI-search measurement in 2026: platform reports (Search Console generative AI report, Bing AI Performance), analytics referrals (GA4 AI Assistant channel), crawler logs, and sampled prompt tests or vendor trackers. Each sees a different slice; none sees everything."
sources:
  - url: "https://support.google.com/webmasters/answer/16984139?hl=en"
    date: 2026-10-21
    title: Generative AI performance report - Search Console Help
  - url: "https://developers.google.com/search/docs/appearance/ai-features"
    date: 2026-10-21
    title: AI features and your website - Google Search Central
  - url: "https://blogs.bing.com/webmaster/2026/2/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview/"
    date: 2026-02-10
    title: Introducing AI Performance in Bing Webmaster Tools Public Preview - Bing Webmaster Blog
  - url: "https://www.searchenginejournal.com/bing-webmaster-tools-topics-portfolio-ai-performance/592874/"
    date: 2026-10-14
    title: Bing Webmaster Tools adds Topics Portfolio to AI Performance - Search Engine Journal
  - url: "https://support.google.com/analytics/answer/9756891?hl=en"
    date: 2026-10-21
    title: "[GA4] Default channel group - Analytics Help"
  - url: "https://arxiv.org/abs/2304.09848"
    date: 2023-10-23
    title: "Evaluating Verifiability in Generative Search Engines (Liu, Zhang, Liang) - arXiv"
confidence: high
superseded_by:
tags: [ai-search, analytics-legal]
fingerprint: 078c30af82b7
trust: high
author: Google; Microsoft; vault synthesis
year: 2026
---
# Measuring AI referrals and AI visibility

> [!summary] TL;DR
> Google: impressions in AI features (Search Console report, Web text and multimodal), clicks counted as normal organic.
> Bing: citations, cited pages, grounding queries, plus Intents, Topics, Citation Share (2026).
> Third-party: prompt sampling (own scripts or tools like Profound, Peec AI, Otterly.AI, Ahrefs Brand Radar) — directional, varies by run.

## Explanation
**1. Platform data (most trustworthy, limited scope).** Google's Search Console generative AI performance report shows impressions for pages in AI features, by page, country, device and date. Google's AI features page says traffic from AI features is included in the Performance report's Web search type. Microsoft's Bing AI Performance report (preview from February 2026) shows how often a site is cited in Copilot and Bing AI answers, which pages, and the grounding queries; Search Engine Journal reported a Topics Portfolio beta in October 2026.

**2. Analytics.** The GA4 AI Assistant channel groups visits from AI assistant referrers but excludes AI Overviews and AI Mode; referrer-less visits fall into Direct.

**3. Logs.** Server or CDN logs show which AI crawlers and user-triggered fetchers request your pages ([[AI crawlers and user agents]], Verifying AI crawlers). Fetch volume isn't visibility.

**4. Prompt sampling.** Run fixed prompts across engines and record mentions, citations, accuracy and competitors (Prompt-based visibility testing). Answers vary by wording, model, location, personalisation and time; research found many generated statements unsupported by their citations (Verifiability of generative search engines (Liu et al. 2023)).

## How to use it
- Monthly: export Search Console AI impressions + Bing AI citations + GA4 AI Assistant sessions/conversions + a prompt test → one sheet (Playbook - Measuring AI search traffic).
- Annotate dates of platform changes (e.g. Google generative AI control rollout 31 Aug 2026).
- Treat vendor 'share of voice' as a sample; record prompt list, engines, country and date with every number.

## Trust & evidence
Trust **high** for platform docs; **medium-low** for vendor metrics (proprietary sampling). Confidence high that no single source is complete.

## Related
- Search Console generative AI performance report
- Bing AI Performance report
- GA4 AI Assistant channel
- Prompt-based visibility testing
- Zero-click searches and AI Overviews
- Playbook - Measuring AI search traffic
- Playbook - AI visibility tool choice matrix
- Google Search Console
- Bing Webmaster Tools

## Sources
- [Generative AI performance report - Search Console Help](https://support.google.com/webmasters/answer/16984139?hl=en) · 2026-10-21
- [AI features and your website - Google Search Central](https://developers.google.com/search/docs/appearance/ai-features) · 2026-10-21
- [Introducing AI Performance in Bing Webmaster Tools Public Preview - Bing Webmaster Blog](https://blogs.bing.com/webmaster/2026/2/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview/) · 2026-02-10
- [Bing Webmaster Tools adds Topics Portfolio to AI Performance - Search Engine Journal](https://www.searchenginejournal.com/bing-webmaster-tools-topics-portfolio-ai-performance/592874/) · 2026-10-14
- [[GA4] Default channel group - Analytics Help](https://support.google.com/analytics/answer/9756891?hl=en) · 2026-10-21
- [Evaluating Verifiability in Generative Search Engines (Liu, Zhang, Liang) - arXiv](https://arxiv.org/abs/2304.09848) · 2023-10-23
