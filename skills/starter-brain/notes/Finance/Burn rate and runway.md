---
id: burn-rate-and-runway
type: concept
status: active
created: 2026-11-03
updated: 2026-11-03
summary: "Gross burn is monthly cash spending, net burn is spending minus cash in; runway is cash balance divided by net burn."
sources:
  - url: "https://www.shopify.com/blog/burn-rate"
    date: 2026-11-03
  - url: "https://carta.com/blog/burn-rate/"
    date: 2026-11-03
confidence: medium
superseded_by:
tags: [cash, concept, runway, verify-cash]
fingerprint: 4926bfa14173
trust: medium
checked: 2026-11-03
---
# Burn rate and runway

> [!summary] TL;DR
> Gross burn = cash out per month; net burn = cash out minus cash in.
> Runway (months) = cash balance / net burn; only meaningful if net burn is positive.
> Use a trailing average and a forward view; one month is noise.

## Definitions (vendor guides agree)
- **Gross burn**: total cash spent per month.
- **Net burn**: gross burn minus cash received per month; usually what "burn rate" means.
- **Runway** = current cash / monthly net burn. Example (Shopify guide): spending 100,000, receipts 50,000, cash 500,000 -> net burn 50,000 -> 10 months.

Sources are vendors (Shopify, Carta, Stripe, Wise): medium trust for definitions, which are simple arithmetic. Carta's page returns HTTP 403 and was not read; the definitions rest on the Shopify guide (re-read 2026-11-03) and the vendor guides, not on Carta.

## Caveats
- If receipts exceed spending, net burn is negative: there is no runway limit, but a *cash-out date* can still come from a lumpy outflow. Use a forecast ([[Cash forecasting - 13-week and 12-month]]).
- Use cash, not profit, and include tax/VAT and loan payments.
- Average 3 months for the base case, then run a downside (late payments, lost client). Measure the downside in buffer days: Cash buffer and buffer days.
- Founders paying themselves: include owner pay in outflows, or say explicitly that it is excluded.

## Steps
Use Template - Runway and burn calculator.

Not financial advice.

## Verify update 2026-11-03 (verify-cash)
Shopify guide re-read: gross burn = total monthly spending; net burn = spending minus revenue; runway = cash reserves / monthly net burn. The worked example in this note (spending 100,000, revenue 50,000, cash 500,000 -> net burn 50,000 -> 10 months) matches the page. Shopify's own sign convention for net burn is inconsistent (it writes revenue minus burn but reports a positive number): use spending minus receipts. Confidence stays medium: vendor sources, arithmetic definitions.

## History
- 2026-11-03: verify-cash: Shopify definitions and example re-read; Carta not readable (403), claim now rests on Shopify.

## Sources
- [https://www.shopify.com/blog/burn-rate](https://www.shopify.com/blog/burn-rate) · 2026-11-03
- [https://carta.com/blog/burn-rate/](https://carta.com/blog/burn-rate/) · 2026-11-03
