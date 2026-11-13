---
id: playbook-tracking-setup-checklist-ga4-gtm-consent-mode-capi
type: concept
status: active
created: 2026-10-22
updated: 2026-11-12
summary: "Ordered checklist to get measurement right before spending on ads: consent, tag manager, GA4 key events, ad platform tags, server events and a reconciliation test. Draft for you to carry out."
sources:
  - url: "https://developers.google.com/tag-platform/security/guides/consent"
    date: 2026-11-12
    title: Manage consent settings (Google tag platform)
    publisher: Google
    kind: primary
  - url: "https://support.google.com/analytics/answer/9355848"
    date: 2026-11-12
    title: Key events (Analytics Help)
    publisher: Google
    kind: primary
  - url: "https://developers.facebook.com/documentation/ads-commerce/conversions-api/deduplicate-pixel-and-server-events"
    date: 2026-11-12
    title: Handling Duplicate Pixel and Conversions API Events (Meta for Developers)
    publisher: Meta
    kind: primary
confidence: medium
superseded_by:
tags: [measure-ops, playbook, tracking, law]
fingerprint: 67fce8a79efb
trust: medium
author: vault synthesis
region: global
checked: 2026-11-12
claim_type: method
---
# Playbook - Tracking setup checklist (GA4, GTM, Consent Mode, CAPI)

> [!summary] TL;DR
> Set consent defaults before any tag; then GA4 and ad platform tags through Tag Manager; then server-side events with deduplication.
> Mark only value-bearing events as key events and send closed deals back to the ad platforms.
> Reconcile platform counts against your own lead log weekly.

## Explanation
Draft for you to carry out; nothing here touches an ad account.

1. Decide the 2 to 3 events that matter: form success, call click, booking, later closed deal (see GA4 events and key events). Cost: 0. Metric: list agreed.
2. Consent: choose a consent banner or CMP; set defaults on every page before any command that sends measurement data, per region if needed (e.g. denied in the EEA), and update as soon as the visitor chooses [1] (see Google Consent Mode v2, Google EU user consent policy). Test: private window, nothing sets ad cookies before choice.
3. Tag Manager: install the two snippets, add a GA4 configuration tag and one trigger per event, test in preview mode (see Google Tag Manager).
4. GA4: mark the events as key events [2]; link Google Ads so key events can be used as conversions (not on the cited page; see Google Analytics 4).
5. UTMs: apply the naming convention to every manual link (see UTM parameters).
6. Meta: install the Pixel, then the Conversions API; send the same event ID and event name from both; Meta drops the duplicate only within 48 hours [3] (see Meta Pixel, Meta Conversions API, Meta Pixel and Conversions API deduplication).
7. Google: add enhanced conversions only after confirming lawful basis (see Google enhanced conversions); store the GCLID with each lead and plan offline import of closed deals (see Google offline conversion import).
8. Server-side tagging: optional later step (see Server-side tagging with Tag Manager).
9. Reconcile: for 2 weeks compare GA4, each ad platform and your lead log; investigate gaps over a quarter of the leads (the brain's own threshold).
10. Attribution: pick one reporting model and write it down (see GA4 attribution models).

## How to use it
Cost: free tools; possible CMP fee and developer time. Metric: share of real leads that appear in GA4 and in each platform. Cheap test: submit 5 test leads from different devices and confirm each appears in every system. This is not legal advice; legal sufficiency of the banner is for the law theme.

## Trust & evidence
Steps 2, 4 and 6 re-read on Google's and Meta's pages on 12 Nov 2026; other steps rest on the linked notes. The order is the brain's own judgment.

## Related
Playbook - Weekly ad report template · Playbook - Meta campaign launch checklist · Playbook - Ad account audit checklist · 🗺️ Tracking & Measurement

## History
- 2026-11-12: L1 check ck-03: consent, key-events and dedup pages re-read; the Google page sets per-region defaults (EEA values not given there); GA4-to-Ads link not on the cited page, now flagged; 48-hour dedup window added; region global.

## Sources
1. [Manage consent settings (Google tag platform)](https://developers.google.com/tag-platform/security/guides/consent) · Google · 2026-11-12 · primary
2. [Key events (Analytics Help)](https://support.google.com/analytics/answer/9355848) · Google · 2026-11-12 · primary
3. [Handling Duplicate Pixel and Conversions API Events (Meta for Developers)](https://developers.facebook.com/documentation/ads-commerce/conversions-api/deduplicate-pixel-and-server-events) · Meta · 2026-11-12 · primary
