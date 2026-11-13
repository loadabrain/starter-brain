---
id: playbook-evaluating-an-agent-case-study
type: concept
status: active
created: 2026-11-02
updated: 2026-11-02
summary: "Ten-minute checklist to rate an agent case study (independent, self-reported, vendor): who says it, what was measured, against what baseline, what went wrong; with worked ratings from cases in this vault."
sources:
  - url: "https://metr.org/blog/2026-02-24-uplift-update/"
    date: 2026-02-24
  - url: "https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have"
    date: 2025-03-24
  - url: "https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/"
    date: 2025-07-10
    title: "METR original study: forecast 24% faster, believed 20% faster, measured 19% slower"
confidence: medium
superseded_by:
tags: [cases, playbook, evaluation, verify-2-cases]
fingerprint: 04a5e5fc1337
checked: 2026-11-02
lifecycle: active
trust: medium (this vault's synthesis)
---
# Playbook - Evaluating an agent case study

> [!summary] TL;DR
> Rate the teller first: vendor on own product = low to medium; independent, named testers with a method = high.
> Then rate the number: counted or claimed, baseline, period, definition of 'resolved', what is missing (cost, failures).
> Output: one evidence label (independent, self-reported, vendor) and a confidence, written in the note.

## Why
Agent case studies are mostly marketing, conference talks and CEO remarks. The same company can give a detailed, useful account (Anthropic's compiler post) or an unverifiable one (a USD 297 contract). This checklist sorts them in minutes. It applies the `source-trust` skill to cases.

## Evidence labels
| Label | Meaning | Examples in this vault |
|---|---|---|
| **independent** | Outsider measured it, method visible | Case - METR randomised trial- experienced developers and AI tools (2025, update Feb 2026), Case - Answer.AI tests Devin for a month (Jan 2025) |
| **self-reported** | Operator or user reports own numbers, no outside check | Case - The Ralph loop and the USD 297 contract claim, Case - An AI automation agency owner closes a 'USD 80k a month' agency (Jan 2026) |
| **vendor** | The seller or maker reports on its own product | Case - Vercel's inbound lead-qualification agent (10 SDRs to about 1), Case - Intercom Fin customer results (Synthesia, Fundrise, Lightspeed, Anthropic) |

A vendor can still be detailed and candid (Case - 16 Claude agents write a C compiler (Anthropic, Feb 2026)). Rate the number, not just the logo.

## The checklist (score 1 point per yes)
1. Is the teller independent of the product's sales?
2. Is the customer named and on the record?
3. Is there a baseline (before, or humans, or a control)?
4. Is the metric defined ('resolved' = customer did not return in 7 days?) and counted, not estimated?
5. Are period and sample size stated?
6. Is cost stated, including humans who review?
7. Are failures and limits stated by the teller?
8. Could someone else check it (open repo, public test, filing)?
9. Did the situation change afterward (Klarna, CBA, McDonald's: check for reversals)?
10. Is the claim a ratio or round number with no range ('10x', '95%')?  *(a yes here costs a point)*

Score 7+ : use with its label. 4-6 : use as a lead and say so. 0-3 : do not cite as evidence.

## Red flags seen in this vault
- A figure forwarded in a message with no scope: the USD 297 contract.
- Logos on a website that customers deny: Case - 11x AI SDR- disputed customers and churn (TechCrunch, March 2025).
- 'Handled' reported as 'resolved': Case - Salesforce cuts support headcount with Agentforce (Benioff, Sept 2025).
- A demo whose CI fails and whose build needed manual fixes: Case - Cursor's agent-built browser (FastRender, Jan 2026).
- Perception beating measurement: METR's developers expected 24% faster, believed afterwards they were 20% faster, and were measured 19% slower in early 2025 (the Feb 2026 update says its newer data are weak evidence).

## Steps
1. Open the original page, not a summary. Note author, date, and who pays them.
2. Fill the case card: who, built, stack, cost, measured result, what went wrong.
3. Run the 10 questions; write the score and the label at the top of your note.
4. Search for a follow-up (reversal, correction, replication) in the last 12 months.
5. Pick a single sentence you can safely repeat to a client, with the label and the date.
6. Before copying a result, run a 2-week pilot on your own tasks with the metric defined in step 4.

Related: Playbook - Measuring time saved by an agent · Playbook - First eval set · Case Studies

## History
- 2026-11-02: Verified against METR (2025 post and Feb 2026 update) and TechCrunch (11x); perception figures added, Cursor wording aligned with its case note.

## Sources
- [https://metr.org/blog/2026-02-24-uplift-update/](https://metr.org/blog/2026-02-24-uplift-update/) · 2026-02-24
- [https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have](https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have) · 2025-03-24
- [METR original study: forecast 24% faster, believed 20% faster, measured 19% slower](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/) · 2025-07-10
