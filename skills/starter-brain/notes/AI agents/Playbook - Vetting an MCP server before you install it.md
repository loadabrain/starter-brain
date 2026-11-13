---
id: playbook-vetting-an-mcp-server-before-you-install-it
type: concept
status: active
created: 2026-11-02
updated: 2026-11-02
summary: "Ten-minute check before adding an MCP server: publisher, source, command, scopes, sandbox; based on MCP security docs and the postmark-mcp incident (checked 2026-11-02)."
sources:
  - url: "https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices"
    date: 2026-11-02
  - url: "https://github.com/modelcontextprotocol/servers"
    date: 2026-11-02
confidence: medium
superseded_by:
tags: [tools, playbook, mcp, testing, security, gap-standards, verify-testing]
fingerprint: a7f8edd0f5a8
checked: 2026-11-02
lifecycle: active
trust: medium
---
# Playbook - Vetting an MCP server before you install it

> [!summary] TL;DR
> A listing proves who published a server, not that it is safe.
> Check publisher, repo activity, exact start command, and requested scopes; run it sandboxed with read-only access first.
> Prefer first-party remote servers with OAuth.

## Why
In September 2025 a copy of the postmark-mcp npm package added a hidden BCC to every email from v1.0.16 (postmark-mcp incident). The MCP registry does not review submissions (Official MCP registry).

## Steps
1. **Who?** Is it published by the service itself (GitHub, Stripe) or the protocol maintainers? Check the namespace or org on the repo; beware look-alike names.
2. **Alive?** Last commit and release dates, open issues, number of maintainers. Many registry servers publish once and stop (MCP server ecosystem quality studies).
3. **Command:** read the exact start command and args; no shell chains, no `sudo` (MCP security best practices).
4. **Pin:** install an exact version, not `@latest`; re-review on update.
5. **Scopes:** least privilege; read-only token or role first; for databases a dedicated read-only role (Database tools for agents).
6. **Sandbox:** container or VM, no home directory, restricted network.
7. **Scan:** optionally run a scanner: Snyk Agent Scan (github.com/snyk/agent-scan, Apache-2.0, the successor line of Invariant Labs mcp-scan; needs a Snyk account and SNYK_TOKEN, so tool names and descriptions go to Snyk) or Cisco mcp-scanner (github.com/cisco-ai-defense/mcp-scanner, Apache-2.0). Expect false positives (see below); neither replaces reading the code.
8. **Allowlist tools:** enable only the tools you need (`allowed_tools`, toolset allowlist).
9. **Log** tool calls for the first week and read them.
10. Record the decision in the vault tool note (template `BrainOS/Templates/Tool.md`).

## Trust & evidence
MCP security page (high); incident details from trade press (medium); scanner names unverified.

## Added 2026-11-02
- Step 4 detail: tool descriptions can change after approval (rug pull, Invariant Labs 2025-04-01); diff descriptions on every update (Tool poisoning).
- Step 6 detail: even an unmodified official server can be abused through content it reads; scope a session to one repository/account (Toxic agent flow - GitHub MCP exfiltration).
- Claude Code docs (2026-11-02): Anthropic reviews connectors against listing criteria but does not security-audit any MCP server.

## Related
OWASP MCP Top 10 · [[Playbook - Agent security checklist]]

## History
- 2026-11-02: Verify pass: scanner names checked on GitHub: Snyk agent-scan and Cisco mcp-scanner both Apache-2.0; Snyk needs a token.
- 2026-11-02: 2026-11-02: scanners named in the AppSec Santa audit added with their false-positive results.
- 2026-11-02: Tagged testing; added rug-pull and scoping steps.

## Scanners to run before you trust a server (checked 2026-11-02)
- Cisco mcp-scanner v4.3.0: pattern rules on tool descriptions and schemas. In the AppSec Santa sample it gave 27 detections on 10 servers; about 78% were false positives after review. Run it, then read the flags.
- Invariant Labs mcp-scan v0.4.3: detects config drift (definition changes), tool-name shadowing and exfiltration flags.
- mcp-audit v0.14.1: remote auth, project-config auto-spawn and typosquats. It produced one false positive on an official reference server in that sample.
- None of them proves a server safe; they are a filter before a code read. Source: AppSec Santa MCP server security audit 2026.

## Sources
- [https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices](https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices) · 2026-11-02
- [https://github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) · 2026-11-02
