---
id: playbook-small-budget-testing-plan-under-20-euros-a-day
type: concept
status: active
created: 2026-10-22
updated: 2026-11-12
summary: "A two-week plan to test one ad channel on less than 20 euros a day, with the learning-phase arithmetic, stated platform minimums and explicit kill and keep rules."
sources:
  - url: "https://ppc.land/learning-phase/"
    date: 2026-09-23
    title: "Explaining learning phase (PPC Land, 23 Sept 2026)"
    publisher: PPC Land
    kind: secondary
  - url: "https://forbusiness.snapchat.com/advertising/pricing"
    date: 2026-11-12
    title: Flexible Snapchat Ads Pricing (Snapchat)
    publisher: Snap
    kind: primary
  - url: "https://business.linkedin.com/advertise/ads/best-practices/maximize-your-budget"
    date: 2026-11-12
    title: Making the Most of Your Budget (LinkedIn)
    publisher: LinkedIn
    kind: primary
  - url: "https://ads.tiktok.com/help/article/budget-and-bidding-faq?lang=en"
    date: 2026-11-12
    title: Budget and Bidding FAQs (TikTok Business Help)
    publisher: TikTok
    kind: primary
  - url: "https://www.facebook.com/business/ads/pricing"
    date: 2026-11-12
    title: Meta ads pricing (Meta for Business)
    publisher: Meta
    kind: primary
  - url: "https://support.google.com/google-ads/answer/16797388?hl=en"
    date: 2026-11-12
    title: Demand Gen campaign performance guide (Google Ads Help)
    publisher: Google
    kind: primary
  - url: "https://help.pinterest.com/en/business/article/pinterest-performance-plus"
    date: 2026-11-12
    title: Pinterest Performance+ (Pinterest Business Help)
    publisher: Pinterest
    kind: primary
confidence: medium
superseded_by:
tags: [meta-ads, google-ads, other-paid, paid-platforms, playbook, budgets]
fingerprint: 749fc3a83f7a
trust: medium
author: vault synthesis
price_date: 2026-11-12
region: global
checked: 2026-11-12
claim_type: method
---
# Playbook - Small-budget testing plan (under 20 euros a day)

> [!summary] TL;DR
> At 20 a day, reaching 50 events in 7 days needs a cost per event of 2.80 or less (7 x 20 / 50); at 10 a day, 1.40.
> If your cost per lead is higher, optimise an earlier, cheaper event or consolidate to one ad set.
> Stated floors (as of 12 Nov 2026): Snapchat USD 5 a day, LinkedIn 10 a day, TikTok 20 per ad group and 50 per campaign; Demand Gen wants 10x target CPA: only some fit under 20 a day.

## Explanation
Draft plan for you to run; amounts as stated on each platform page (currency often unnamed).

Step 0: allowable cost per lead (value x close rate x share). Step 1: one channel, one campaign, one ad set, 3 ads. Step 2: budget B per day for 14 days: B = 10 costs 140, B = 15 costs 210, B = 20 costs 280.
Learning arithmetic (our calculation, on the ~50 events in 7 days that Meta's learning phase needs [1]): max cost per event to reach 50 events in 7 days = 7 x B / 50. B = 20 gives 2.80, B = 15 gives 2.10, B = 10 gives 1.40 (see [[Learning phase across ad platforms]]). If your cost per lead is above this, either optimise an upstream event (form open, landing view) or accept that the ad set will stay Learning Limited and read results as directional only.
Which channels fit: Meta suggests starting with at least USD 5 and a budget that can run 7 days [5]; Snapchat USD 5 a day minimum [2]; LinkedIn 10 a day minimum [3]; TikTok states 20 per ad group and 50 per campaign (the page does not say daily) [4]; Demand Gen wants a budget of at least 10x target CPA, so skip [6]; Pinterest Performance+ wants 5x CPA [7] (see [[Minimum budgets across ad platforms]]). Google Search has no stated minimum on the pages opened, but cost per click and competition decide whether 20 a day gives enough clicks to learn anything.
Rules (vault judgement): do not edit the ad set during the first 7 days; at day 7 read cost per qualified lead; if it is more than 3x the allowable cost, kill; if within 1.5x, keep and iterate one creative; if below, raise budget by 20 to 30 percent (Pinterest guidance [7]) or at most 15 percent (Demand Gen guidance [6]), not more.
Log: spend, leads, qualified leads, cost per qualified lead, what you changed.

## How to use it
Cost: 140 to 280 over two weeks. Metric: cost per qualified lead and the learning status. Cheap test: this is the plan; end it at day 14 whatever the result and write a one-page summary.

## Trust & evidence
Arithmetic is exact; the kill and keep thresholds are the vault's judgement and not from a source. Platform minima are from the first-party pages in the linked notes.

## Related
Playbook - Meta campaign launch checklist · Playbook - Google Search campaign launch checklist · Playbook - Which ad platform for which business · Meta budgets and spend pacing · 🗺️ Meta Ads

## History
- 2026-11-12: L1 check ck-03: corrected Demand Gen (Google now says budget >= 10x target CPA and budget steps of at most 15%; '100 a day' and '5-10% a week budget' were wrong, 5-10% is for bids); TikTok minimum is 20 per ad group and 50 per campaign; currencies added; Demand Gen and Pinterest pages added as sources; region global.

## Sources
1. [Explaining learning phase (PPC Land, 23 Sept 2026)](https://ppc.land/learning-phase/) · PPC Land · 2026-09-23 · secondary
2. [Flexible Snapchat Ads Pricing (Snapchat)](https://forbusiness.snapchat.com/advertising/pricing) · Snap · 2026-11-12 · primary
3. [Making the Most of Your Budget (LinkedIn)](https://business.linkedin.com/advertise/ads/best-practices/maximize-your-budget) · LinkedIn · 2026-11-12 · primary
4. [Budget and Bidding FAQs (TikTok Business Help)](https://ads.tiktok.com/help/article/budget-and-bidding-faq?lang=en) · TikTok · 2026-11-12 · primary
5. [Meta ads pricing (Meta for Business)](https://www.facebook.com/business/ads/pricing) · Meta · 2026-11-12 · primary
6. [Demand Gen campaign performance guide (Google Ads Help)](https://support.google.com/google-ads/answer/16797388?hl=en) · Google · 2026-11-12 · primary
7. [Pinterest Performance+ (Pinterest Business Help)](https://help.pinterest.com/en/business/article/pinterest-performance-plus) · Pinterest · 2026-11-12 · primary
