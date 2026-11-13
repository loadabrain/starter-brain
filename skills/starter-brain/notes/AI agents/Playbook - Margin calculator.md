---
id: playbook-margin-calculator
type: playbook
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "Compute gross margin per customer for an AI product or service from token, tool, hosting, payment and support costs, with worked examples and stress tests."
sources:
  - url: "https://sitegpt.ai/pricing"
    date: 2026-10-21
    title: Pricing (SiteGPT)
  - url: "https://developers.openai.com/api/docs/pricing"
    date: 2026-10-21
    title: API pricing (OpenAI)
  - url: "https://platform.claude.com/docs/en/about-claude/pricing"
    date: 2026-10-21
    title: Pricing (Claude Docs)
  - url: "https://stripe.com/en-be/pricing"
    date: 2026-10-21
    title: Pricing (Stripe Belgium)
confidence: medium
superseded_by:
tags: [money, economics, business-models]
fingerprint: e1f43a540935
year: 2026
trust: medium
author: "Claude Sonnet 5.5 (crawl), derived from cited sources"
price_date: 2026-10-21
---
# Playbook - Margin calculator

> [!summary] TL;DR
> Gross margin = (price − tokens − tools − hosting − payment fees − support/time) ÷ price, per customer per month.
> Example: a 59 USD chatbot plan with 5.92 USD of tokens and ~1.5 USD of fees keeps about 87 percent before hosting and support.
> Always stress-test with 2x token price, +30 percent tokens, 20 percent monthly churn and your hourly rate for services.

## When to use
Before pricing, before accepting a client, and every quarter.

## Steps
1. List variable costs per customer-month: tokens (Playbook - Token cost calculator, prices in LLM API price comparison October 2026), tool fees (web search 10 USD per 1,000), hosting, payment fees (Payment and billing fees for a Belgian seller).
2. Add support/time: hours × your hourly cost (services) or ticket volume (software).
3. Margin % = 1 − costs ÷ price. Compare with the AI-native band 50-60 % (AI gross margins versus SaaS, low-trust).
4. Stress tests: ×2 token price (Token price trends), +30 % tokens (tokenizer), heavy-user case, 5/10/20 % churn (Churn and retention of AI apps).
5. Decide caps, minimums and tier limits.

## Worked examples (USD, assumptions stated)
| Case | Price | Variable cost | Margin |
|---|---|---|---|
| Chatbot plan (SiteGPT-like Starter) | 59 | tokens 5.92 + card 1.1 + Billing 0.4 = 7.4 | 87 % before hosting/support |
| Same, tokens ×2 and ×1.3 | 59 | 15.4 + 1.5 = 16.9 | 71 % |
| Agent run, 1,000 runs at 0.20 (cached) charged 0.50 each | 500 | 200 + fees ~10 | 58 % |
| Same uncached (0.70 per run) | 500 | 700 | negative |
| Automation retainer, 400 EUR/month, 3 h work at 60 EUR/h, 15 EUR APIs | 400 | 195 | 51 % |

## Checklist
- [ ] token log · [ ] cache/batch share · [ ] free-user cost · [ ] payment fees · [ ] support hours · [ ] 2x price case · [ ] churn case

## Trust & evidence
Arithmetic on vendor list prices (high); usage assumptions are hypothetical (Inference cost versus price charged, Cost of running AI agents).

## For a solo founder
Include your own time at a real hourly rate; a service with 50 % margin after your time is healthy, software below 60 % before time is thin.

## Sources
- [Pricing (SiteGPT)](https://sitegpt.ai/pricing) · 2026-10-21
- [API pricing (OpenAI)](https://developers.openai.com/api/docs/pricing) · 2026-10-21
- [Pricing (Claude Docs)](https://platform.claude.com/docs/en/about-claude/pricing) · 2026-10-21
- [Pricing (Stripe Belgium)](https://stripe.com/en-be/pricing) · 2026-10-21
