---
id: structured-data
type: concept
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "Structured data tells Google what a page is about in a standard format (JSON-LD recommended); it can make a page eligible for rich results, but Google does not guarantee that they appear."
sources:
  - url: "https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data"
    date: 2026-10-21
    title: Intro to structured data - Google Search Central
confidence: high
superseded_by:
tags: [technical-seo, seo-tools, ai-search]
fingerprint: 69b0fceab653
trust: high
author: Google Search Central
year: 2026
---
# Structured data

> [!summary] TL;DR
> Google supports three formats: JSON-LD (recommended), Microdata and RDFa; any of them works if valid and implemented correctly.
> A page is eligible for a rich result only if the object carries all of its required properties; accurate, complete properties matter more than many incomplete ones.
> Validate the markup with the Rich Results Test before and after release; eligibility is not a guarantee that a rich result will show.

## Explanation
Structured data is a standard format for giving Google information about a page. Google's introduction says it helps Google understand the content, and can enable richer search results, called rich results.

Three formats are supported: JSON-LD, Microdata and RDFa. JSON-LD is the recommended choice: it sits in a script tag separate from the visible text and is easiest to implement and maintain at scale. The vocabulary comes from Schema.org.

## What Google requires
An object must include all required properties to be eligible for the enhanced display. Google says accurate, complete properties matter more than adding many incomplete ones. It does not say that structured data guarantees rich results.

## Rules that matter for a client site
- Markup must describe what is visible on the page. Marking up content that users cannot see is a spam risk (see Spam policies).
- Only one of the three formats per page; do not mix formats for the same object (opinion; the page read does not state this rule).
- Keep markup in step with the page: a changed price or date must change in the markup too.

## How to use it
1. Pick the type per page: organisation on the home or About page, article on blog posts, local business on contact pages (see Organization structured data, Article structured data, LocalBusiness structured data).
2. Write JSON-LD with the required properties first, then the recommended ones that apply.
3. Test the URL or the snippet in the Rich Results Test before release.
4. After release, re-check the same URL and check the page's rich-result status in Google Search Console (the exact report name was not read).
5. Keep a template per page type, so new pages inherit the markup (Playbook - JSON-LD templates for common pages).

## FAQ and HowTo
FAQ rich results were removed in 2026; see FAQ rich results. Do not build a client's plan on them.

## Trust & evidence
From Google's structured data introduction (opened 2026-10-21): high for the formats and eligibility rules. Schema.org's vocabulary is high trust. The 'do not mix formats' point is our practice, labelled as such. Confidence high.

## Related
Schema.org · Rich Results Test · Product structured data and merchant listings · Directory - Technical SEO
Google guidance on generative AI search features

## Sources
- [Intro to structured data - Google Search Central](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data) · 2026-10-21
