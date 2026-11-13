---
id: playbook-agent-security-checklist
type: concept
status: active
created: 2026-11-02
updated: 2026-11-03
summary: "One-page pre-launch checklist for an agent, mapped to OWASP LLM and agentic lists: access, injection, tools/MCP, secrets, sandbox, cost, logging (checked 2026-11-02)."
sources:
  - url: "https://genai.owasp.org/llm-top-10/"
    date: 2026-11-02
  - url: "https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/"
    date: 2025-12-09
  - url: "https://code.claude.com/docs/en/security"
    date: 2026-11-02
confidence: medium
superseded_by:
tags: [testing, security, playbook, verify-2-testing]
fingerprint: 9cbd0be5f5c8
lifecycle: active
checked: 2026-11-02
trust: medium
---
# Playbook - Agent security checklist

> [!summary] TL;DR
> Run through 12 questions before an agent touches real data.
> Each maps to an OWASP item and a vault note with steps.
> Any 'no' becomes a task or a documented accepted risk.

## Checklist
1. **Trifecta/Rule of Two**: which of private data, untrusted input, outward action does it have? Max two or approval. (Agents Rule of Two; OWASP LLM01, ASI01)
2. **Least privilege**: scoped tokens, read-only first. (LLM06 Excessive Agency, ASI03)
3. **Approvals** on send/pay/delete/publish. (Autonomy & Approvals)
4. **Tools and MCP vetted**, versions pinned, only needed tools enabled. ([[Playbook - Vetting an MCP server before you install it]], Tool poisoning; LLM03, ASI04)
5. **Skills/plugins** read before install. (Agent skill security)
6. **Secrets** never in prompts, repo or logs; injected outside the model. (Secrets handling for hosted agents; LLM02)
7. **Sandbox** for code, files, network egress allowlist. (Sandboxing for agents; ASI05)
8. **Output handling**: model output never goes straight into shell, SQL or HTML. (LLM05)
9. **Memory** writes reviewed or scoped. (Memory poisoning; ASI06)
10. **Limits and logs**: max turns/budget, cost alerts, traces with masking. (Agent cost tracking and alerts, Playbook - Logging and tracing an agent; LLM10)
11. **Tests**: canary-leak eval and the first eval set pass. (Playbook - Prompt injection defences, Playbook - First eval set)
12. **Kill switch**: one way to revoke the agent's keys.

## Trust
Synthesis of the linked notes; lists: OWASP Top 10 for LLM Applications 2025 (names high), OWASP Top 10 for Agentic Applications 2026 (names medium). Not a compliance standard.

## History
- 2026-11-02: Verified (verify-2-testing): TL;DR said 10 questions but the list has 12; fixed. OWASP LLM names (LLM01, 02, 03, 05, 06, 10) confirmed on genai.owasp.org; ASI01 Agent Goal Hijack, ASI03 Identity and Privilege Abuse, ASI04 Agentic Supply Chain, ASI05 Unexpected Code Execution, ASI06 Memory and Context Poisoning confirmed via secondary summaries only (OWASP page does not list them); agentic names stay medium.

## Seen in the wild
- 2026-10-31 · A carousel's safety advice before installing agents: expect API costs, run code- or click-capable agents in a sandbox (Docker or a spare machine), paper trade first, and check the last commit and licence rather than trusting stars. · [source](https://www.instagram.com/p/DePWmOHCPX1/) · Signal confidence: medium

## Sources
- [https://genai.owasp.org/llm-top-10/](https://genai.owasp.org/llm-top-10/) · 2026-11-02
- [https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) · 2025-12-09
- [https://code.claude.com/docs/en/security](https://code.claude.com/docs/en/security) · 2026-11-02
  - url: "https://genai.owasp.org/llmrisk/llm01-prompt-injection/"
    date: 2026-10-21
    title: LLM01 Prompt Injection (OWASP GenAI)
  - url: "https://platform.claude.com/docs/en/agents-and-tools/tool-use/computer-use-tool"
    date: 2026-10-21
    title: Computer use tool (Claude Docs)
  - url: "https://modelcontextprotocol.io/specification/latest"
    date: 2026-10-21
    title: Specification (Model Context Protocol)
  - url: "https://github.com/modelcontextprotocol/servers"
    date: 2026-10-21
    title: modelcontextprotocol/servers (GitHub)
confidence: medium
superseded_by:
tags: [ai-world, agents, risks]
fingerprint: b80a2453c8b8
year: 2026
trust: medium
author: "Claude Sonnet 5.5 (crawl), derived from cited sources"
price_date: 2026-10-21
---
# Playbook - Agent security checklist

> [!summary] TL;DR
> Treat all fetched content and tool descriptions as untrusted; prompt injection cannot be fully prevented.
> Sandbox computer-use and browser agents in a VM with no credentials and an allowlist of domains.
> Require human approval for purchases, sends, deletions and terms acceptance.

## When to use
Before any agent gets write access, credentials, or reads untrusted web or email content.

## Checklist
- [ ] Minimal scope in the system prompt; one job per agent.
- [ ] Least-privilege credentials, handled in code, never in prompts (Prompt injection).
- [ ] Untrusted content labelled; no sensitive tool in the same agent that reads untrusted pages.
- [ ] Outputs validated by deterministic code (formats, allowlists).
- [ ] Human approval for high-risk actions (spend, send, delete, accept).
- [ ] MCP servers audited like third-party code; reference servers are not production-ready (MCP Registry and reference servers); tool annotations untrusted (Model Context Protocol).
- [ ] Sandbox: dedicated VM or container, no stored logins, domain allowlist (Computer use, Browser Use).
- [ ] Logging of every tool call; spend caps (Cursor allows caps on third-party model spend).
- [ ] Adversarial tests on a schedule; re-test after model changes.
- [ ] Data location and retention reviewed (Claude API data residency).

## Trust & evidence
Built from OWASP LLM01 mitigations, Anthropic's computer-use precautions and the MCP security principles (all opened). Not a compliance certificate.

## Sources
- [LLM01 Prompt Injection (OWASP GenAI)](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) · 2026-10-21
- [Computer use tool (Claude Docs)](https://platform.claude.com/docs/en/agents-and-tools/tool-use/computer-use-tool) · 2026-10-21
- [Specification (Model Context Protocol)](https://modelcontextprotocol.io/specification/latest) · 2026-10-21
- [modelcontextprotocol/servers (GitHub)](https://github.com/modelcontextprotocol/servers) · 2026-10-21
