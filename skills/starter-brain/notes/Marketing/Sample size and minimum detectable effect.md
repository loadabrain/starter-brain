---
id: sample-size-and-minimum-detectable-effect
type: concept
status: active
created: 2026-10-22
updated: 2026-11-12
summary: "Evan Miller's calculator takes a baseline conversion, a minimum detectable effect, power and significance; his default example needs 2,545 visitors per variation for a 3-point lift on 10.2%."
sources:
  - url: "https://evanmiller.org/ab-testing/sample-size.html"
    date: 2026-11-12
    title: Sample Size Calculator (Evan Miller)
    publisher: Evan Miller
    kind: primary
  - url: "https://www.evanmiller.org/how-not-to-run-an-ab-test.html"
    date: 2010-04-18
    title: How Not To Run an A/B Test (Evan Miller)
    publisher: Evan Miller
    kind: primary
confidence: medium
superseded_by:
tags: [creative-copy, funnels]
fingerprint: 90dca3734c76
trust: medium
author: Evan Miller
year: 2026
region: global
checked: 2026-11-12
claim_type: method
---
# Sample size and minimum detectable effect

> [!summary] TL;DR
> The calculator inputs: baseline conversion rate, minimum detectable effect (absolute or relative), statistical power and significance level.
> Default example: 10.2% baseline to 13.2% needs 2,545 per variation.
> Low-traffic sites should test big changes or use qualitative tests, because small effects need large samples.

## Explanation
Evan's Awesome A/B Tools offers a sample size calculator. Inputs: baseline conversion rate (default 10.2%), minimum detectable effect (MDE) entered as an absolute or relative difference (default range 10.2% to 13.2%, a 3-point absolute lift), statistical power (1−β) and significance level (α). With the defaults it reports 2,545 per variation. Conversion rates in the grey area of the range are not distinguishable from the baseline. The page does not state the power and significance defaults.

My arithmetic using the rule of thumb from Miller's article (AB testing basics and why not to peek): for a 5% baseline and a 2.5-point absolute minimum effect, n = 16 × 0.05 × 0.95 / 0.025² ≈ 1,216 per variation. A landing page with 200 visits a month would need many months to read that, so low-traffic tests should aim at large changes (a different offer, not a different button colour).

## How to use it
Write the baseline from your own last month, pick the smallest effect that would change your decision, run the calculator, and divide the sample by weekly visits to get the duration. If the duration is over about 6 weeks, redesign the test.
**Cost:** free. **Metric:** visitors per variation reached, conversions per variant. **Cheap test:** calculate before buying traffic; a local niche in a small market often supports only one or two real tests per quarter.

## Trust & evidence
Tool and article by a single independent author (medium-high trust). The calculation in the second paragraph is the crawler's own arithmetic from the article's rule of thumb, flagged as such. Confidence: medium.

## Related
- AB testing basics and why not to peek
- Creative testing structure for small budgets
- Landing page conversion benchmarks and their limits
🗺️ Creatives & Testing

## History
- 2026-11-12: L1 check ck-04: calculator defaults (10.2% baseline, 10.2–13.2% range, 2,545 per variation) and the n = 16 sigma^2/delta^2 rule (article 18 Apr 2010) confirmed; arithmetic re-checked (1,216); region BE -> global.

## Sources
1. [Sample Size Calculator (Evan Miller)](https://evanmiller.org/ab-testing/sample-size.html) · Evan Miller · 2026-11-12 · primary
2. [How Not To Run an A/B Test (Evan Miller)](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) · Evan Miller · 2010-04-18 · primary
