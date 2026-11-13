---
id: template-pricing-calculator
type: concept
status: active
area: pricing
created: 2026-11-03
updated: 2026-11-03
summary: "Ready spreadsheet layout: costs, billable days, target margin, day rate, project quote with buffer, margin check and discount test."
sources:
  - url: "https://www.freelanceinformer.com/career-tips-for-freelancers/2026-uk-freelance-day-rate-formula-how-to-calculate-your-true-cost-of-business/"
    date: 2026-11-03
  - url: "https://socialsecurity.belgium.be/sites/default/files/content/docs/fr/elaboration-politique-sociale/independants/note_de_cotisations_2026_tableau_fr.pdf"
    date: 2026-11-03
confidence: medium
superseded_by:
tags: [pricing, template, day-rate, playbook]
fingerprint: 2497c1e8c40e
trust: medium
checked: 2026-11-03
---
# Template - Pricing calculator

> [!summary] TL;DR
> One workbook that turns costs and a target margin into a day rate, a quote and a discount test. Method: Day rate for a service business or studio, Margin vs markup, Discounts and their margin effect.

## Tab 1 - Inputs (one row per line)
`line | amount per year | type (owner pay / fixed cost / variable cost) | note`
Rows: target owner pay; social contributions (see RSVZ-INASTI - Social contributions for the self-employed 2026); tax reserve % (ask accountant); software; insurance; accountant; office; marketing; training; equipment depreciation.

## Tab 2 - Day rate
- `B1 weekdays` = 260
- `B2 minus holidays, leave, sickness, training, admin and sales days`
- `B3 billable days` = B1 - B2 (cross-check: B3 / (B1 - holidays - leave) = utilisation, see [[Utilisation rate for service businesses]])
- `B4 revenue needed` = SUM(owner pay + contributions + fixed costs) / (1 - tax reserve %)
- `B5 day rate (floor)` = B4 / B3
- `B6 target margin on projects` (e.g. 30 %) and `B7 day rate with margin` = B5 / (1 - B6) if you also want profit above owner pay

## Tab 3 - Quote
`task | days low | days high | days planned (=(low+4*high)/5 or your rule) | variable cost | price at day rate`
- `subtotal` = planned days x day rate + variable cost
- `risk buffer %` (10-20 %, state why)
- `quote` = subtotal x (1 + buffer)
- `margin %` = (quote - variable cost - planned days x cost per day) / quote
- `value check`: estimated client value; ratio quote / value.

## Tab 4 - Discount test
`quote | discount % | contribution margin % | required extra volume = d/(m-d) | go / no-go`

## Steps
1. Fill Inputs. 2. Read the floor day rate. 3. Quote with a buffer. 4. Run Checklist - Margin check before quoting. Not financial advice; ask your accountant about tax and contribution assumptions.

## Sources
- [https://www.freelanceinformer.com/career-tips-for-freelancers/2026-uk-freelance-day-rate-formula-how-to-calculate-your-true-cost-of-business/](https://www.freelanceinformer.com/career-tips-for-freelancers/2026-uk-freelance-day-rate-formula-how-to-calculate-your-true-cost-of-business/) · 2026-11-03
- [https://socialsecurity.belgium.be/sites/default/files/content/docs/fr/elaboration-politique-sociale/independants/note_de_cotisations_2026_tableau_fr.pdf](https://socialsecurity.belgium.be/sites/default/files/content/docs/fr/elaboration-politique-sociale/independants/note_de_cotisations_2026_tableau_fr.pdf) · 2026-11-03
