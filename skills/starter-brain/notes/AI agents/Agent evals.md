---
id: agent-evals
type: concept
status: active
created: 2026-11-02
updated: 2026-11-02
summary: "Tests for an agent: tasks with success criteria, repeated trials, graders (code, model, human) and transcripts; pass@k vs pass^k."
sources:
  - url: "https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents"
    date: 2026-01-09
confidence: medium
superseded_by:
tags: [basics, testing, verify-basics]
fingerprint: 7390948b3f12
checked: 2026-11-02
lifecycle: active
trust: medium
---
# Agent evals

> [!summary] TL;DR
> Eval = input + grading logic; task = one test; trial = one attempt; transcript = full record; outcome = final environment state.
> Graders: code-based (cheap, brittle), model-based (flexible, needs calibration), human (gold standard, slow).
> pass@k = at least one success in k tries; pass^k = all k succeed (75% per trial gives ~42% over 3).

## Explanation
Source: Anthropic *Demystifying evals for AI agents* (2026-01-09). Grade the **outcome** (is the booking in the database) rather than the agent's claim. Customer-facing agents need pass^k, because users hit every run.
Vendor guidance on its own tooling: trust medium; the definitions are standard.

## Do this
1. Write 10 realistic tasks with a checkable end state. 2. Run each 3 times. 3. Read the transcripts of failures. 4. Track pass^3.

## Related
Agent harness · Stop condition
Playbook - First eval set · LLM-as-judge graders · Regression runs and eval datasets from failures · Promptfoo · Inspect AI

## History
- 2026-11-02: verify-basics: article re-opened; date 2026-01-09, definitions and the 75% to 42% pass^3 example confirmed.
- 2026-11-02: Tagged testing; linked to the first-eval-set playbook and eval tools.

## Sources
- [https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) · 2026-01-09
