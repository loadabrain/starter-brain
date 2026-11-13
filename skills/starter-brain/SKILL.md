---
name: starter-brain
description: Answer questions on sales, marketing, websites, brand and design, small-business finance and AI agents from 42 sourced, dated notes, citing each note's sources and confidence, and using the web only for what the notes don't cover. Use when the user asks how to price work, write a cold message, run a sales call, plan a landing page or a small ad test, check Core Web Vitals or EU cookie rules, judge colour contrast, forecast cash, or vet an MCP server or agent, or asks to "use the starter brain".
---
# Starter brain (Lite OS)

42 short notes in `notes/<field>/`, each with its sources (dated), a `confidence` value and a summary. Fields: Sales, Marketing, Web, Brand & Design, Finance, AI agents.

## How to answer
1. Find the right notes in the index below (or search `notes/`). Open at most 3.
2. Answer from the notes. Name the note, give its sources with their dates, and say how sure it is (`confidence`).
3. Use the web only after the notes, and only for what they don't cover. Say which parts come from the web. If the web is not available, answer from the notes.
4. If no note covers the question, say so plainly and answer from general knowledge or the web, marked as such.
5. Laws, money and health: quote the source and date, and say it is not legal or financial advice; rules may have changed.
6. Never change the files in `notes/`. If the user wants to keep something, suggest a note in their own folder.

## Index
### Sales
- `notes/Sales/Problem-led messaging (poke the bear).md` (medium): Josh Braun's technique: instead of a leading question or a pitch, ask a neutral question that exposes a hidden risk in the prospect's current approach ('How do you know you're not being overcharged for shipping?').
- `notes/Sales/Pain → impact → urgency.md` (medium): Discovery chain shared by SPIN, Sandler, Gap Selling and Force Management: find a business problem, develop its impact (cost, risk, people), then establish why it must be fixed now, all in the buyer's words.
- `notes/Sales/Calibrated questions.md` (medium): Open 'what/how' questions that make the counterpart work on your problem: 'How am I supposed to do that?', 'What makes you ask?', 'How will we know we're on track?'; Black Swan's method.
- `notes/Sales/Customer indecision (JOLT).md` (medium): Dixon & McKenna's research on 2.5M recorded sales calls: 40–60% of deals are lost to no decision, often from fear of messing up; JOLT = Judge, Offer a recommendation, Limit exploration, Take risk off the table. Fear-based pushing backfires.
- `notes/Sales/Quantifying business value.md` (high): Turn the buyer's problems into numbers they own: baseline, expected change, value in time, people, money and risk, with costs and uncertainty, so the economic buyer can compare doing something with doing nothing.
- `notes/Sales/Mutual action plan.md` (medium): A shared buyer-seller plan that works back from the buyer's go-live date: goals, stakeholders, milestones (legal, security, procurement), owners and dates.
- `notes/Sales/Anchoring and first offers.md` (high): The first number pulls the final deal toward it: a 2025 meta-analysis of 90 studies finds a first-mover gain and more gain for ambitious offers, with more impasses and anger; effects shrink in multi-issue deals.

### Marketing
- `notes/Marketing/Landing page anatomy for a service business.md` (medium): The sections a service landing page needs and the sourced reason for each: outcome headline, proof, process, price signal, trust, risk removal and one form, in scannable order.
- `notes/Marketing/Sample size and minimum detectable effect.md` (medium): Evan Miller's calculator takes a baseline conversion, a minimum detectable effect, power and significance; his default example needs 2,545 visitors per variation for a 3-point lift on 10.2%.
- `notes/Marketing/Playbook - Small-budget testing plan (under 20 euros a day).md` (medium): A two-week plan to test one ad channel on less than 20 euros a day, with the learning-phase arithmetic, stated platform minimums and explicit kill and keep rules.
- `notes/Marketing/Minimum budgets across ad platforms.md` (medium): Side-by-side table of the minimum and recommended budgets each platform states in its own pages, with what was not stated; dated 22 October 2026.
- `notes/Marketing/Learning phase across ad platforms.md` (medium): What the learning phase is, how many results each platform needs to leave it, what resets it, and what to do when a small account never gets enough conversions.
- `notes/Marketing/Playbook - Free tiers that are enough to start.md` (medium): Table of free plans read on 22 Oct 2026 with their limits, and a verdict on whether each is enough for a solo company starting out.
- `notes/Marketing/Playbook - Tracking setup checklist (GA4, GTM, Consent Mode, CAPI).md` (medium): Ordered checklist to get measurement right before spending on ads: consent, tag manager, GA4 key events, ad platform tags, server events and a reconciliation test. Draft for you to carry out.

### Web
- `notes/Web/Core Web Vitals.md` (high): The three user-experience metrics Google uses for loading, responsiveness and visual stability, with their good thresholds at the 75th percentile of page loads.
- `notes/Web/Playbook - Builder and CMS choice matrix.md` (medium): A decision matrix for choosing a builder, CMS, e-commerce platform or AI builder for a client site, with the sourced facts per option and the open checks.
- `notes/Web/ePrivacy Directive Article 5(3).md` (high): Article 5(3) of the ePrivacy Directive 2002/58/EC (as amended in 2009) is the EU cookie rule: storing or reading information on a user's device needs consent after clear information, except storage or access strictly necessary to transmit a communication or to provide a service the user explicitly requested.
- `notes/Web/AI crawlers and user agents.md` (high): Reference table of the main AI-related robots.txt tokens (Google, OpenAI, Anthropic, Perplexity, Microsoft, Apple, Common Crawl, Mistral, Amazon, DuckDuckGo) and what blocking each one actually does — training, search inclusion and user fetches are separate switches.
- `notes/Web/Measuring AI referrals and AI visibility.md` (high): Four layers of AI-search measurement in 2026: platform reports (Search Console generative AI report, Bing AI Performance), analytics referrals (GA4 AI Assistant channel), crawler logs, and sampled prompt tests or vendor trackers. Each sees a different slice; none sees everything.
- `notes/Web/Structured data.md` (high): Structured data tells Google what a page is about in a standard format (JSON-LD recommended); it can make a page eligible for rich results, but Google does not guarantee that they appear.
- `notes/Web/Playbook - Media performance checklist.md` (medium): A pre-launch checklist for images, video and fonts, each item tied to the note that sources it.

### Brand & Design
- `notes/Brand & Design/Distinctive brand assets (Romaniuk).md` (medium): Jenni Romaniuk's method to build and measure assets that trigger the brand: fame, uniqueness, and why not to change them.
- `notes/Brand & Design/Visual hierarchy.md` (medium): The order in which a viewer notices and reads things, set by contrast, scale, colour, grouping and position; NN/g's definition and what is evidence versus convention.
- `notes/Brand & Design/Gestalt grouping principles.md` (high): The perceptual grouping rules (proximity, similarity, common fate, continuity, closure, symmetry, common region, connectedness) as reviewed by vision science in 2012, and how a designer should use them.
- `notes/Brand & Design/WCAG 2.2 colour contrast rules (1.4.3, 1.4.11, 1.4.1).md` (high): WCAG 2.2 AA: 4.5:1 for normal text, 3:1 for large text and for UI components and meaningful graphics; logotypes exempt; colour alone must not carry meaning.
- `notes/Brand & Design/Checklist - Colour accessibility.md` (medium): Tick-list for a brand or UI palette: contrast pairs, non-colour cues, colour-blind simulation, dark mode, logo and documentation.
- `notes/Brand & Design/Checklist - Commercial use of AI images.md` (medium): Before using an AI image for a client: confirm plan and licence, revenue thresholds, privacy of generations, indemnity, copyright position, look-alike risk, labelling duties, and keep a dated log.
- `notes/Brand & Design/Checklist - Font licence before handover.md` (medium): Ten checks to run before giving a client brand files: which fonts, which licences, who owns them, whether the client's uses are covered, and what proof to hand over.

### Finance
- `notes/Finance/Value-based pricing.md` (medium): Pricing on the value the client gets rather than on your costs or hours; how it works for service firms and what evidence exists.
- `notes/Finance/Utilisation rate for service businesses.md` (medium): Billable hours / available hours: how to compute it for a studio or one-person firm, benchmarks (about 66-75 % for professional services) and how it drives the day rate.
- `notes/Finance/Template - Pricing calculator.md` (medium): Ready spreadsheet layout: costs, billable days, target margin, day rate, project quote with buffer, margin check and discount test.
- `notes/Finance/Change orders.md` (medium): A change order is a written, priced, approved change to scope, schedule or cost; PMBOK integrated change control says a change in one baseline affects the others.
- `notes/Finance/Cash vs profit vs revenue.md` (medium): Revenue is what you invoice, profit is revenue minus costs on an accrual basis, cash is money that actually moved in the bank; the three differ in timing.
- `notes/Finance/Burn rate and runway.md` (medium): Gross burn is monthly cash spending, net burn is spending minus cash in; runway is cash balance divided by net burn.
- `notes/Finance/Cash forecasting - 13-week and 12-month.md` (medium): A 13-week forecast is a weekly, direct-method roll-forward of receipts and payments; a 12-month forecast is monthly and plans buffer and big dates.

### AI agents
- `notes/AI agents/Playbook - Hype check.md` (medium): Questions to separate what companies announced from what people claim on X; includes the legal lines (FTC earnings claims, EU/UK fake urgency).
- `notes/AI agents/Playbook - Agent security checklist.md` (medium): One-page pre-launch checklist for an agent, mapped to OWASP LLM and agentic lists: access, injection, tools/MCP, secrets, sandbox, cost, logging (checked 2026-11-02).
- `notes/AI agents/Playbook - Vetting an MCP server before you install it.md` (medium): Ten-minute check before adding an MCP server: publisher, source, command, scopes, sandbox; based on MCP security docs and the postmark-mcp incident (checked 2026-11-02).
- `notes/AI agents/Agent evals.md` (medium): Tests for an agent: tasks with success criteria, repeated trials, graders (code, model, human) and transcripts; pass@k vs pass^k.
- `notes/AI agents/Playbook - Evaluating an agent case study.md` (medium): Ten-minute checklist to rate an agent case study (independent, self-reported, vendor): who says it, what was measured, against what baseline, what went wrong; with worked ratings from cases in this vault.
- `notes/AI agents/Playbook - Pre-launch failure review.md` (medium): A one-hour review before an agent goes live: pick the failure classes it can reach, test each with a concrete attack or mistake, and record the control and the owner.
- `notes/AI agents/Playbook - Margin calculator.md` (medium): Compute gross margin per customer for an AI product or service from token, tool, hosting, payment and support costs, with worked examples and stress tests.
