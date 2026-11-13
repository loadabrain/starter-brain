---
id: ai-crawlers-and-user-agents
type: concept
status: active
created: 2026-10-21
updated: 2026-10-21
summary: "Reference table of the main AI-related robots.txt tokens (Google, OpenAI, Anthropic, Perplexity, Microsoft, Apple, Common Crawl, Mistral, Amazon, DuckDuckGo) and what blocking each one actually does — training, search inclusion and user fetches are separate switches."
sources:
  - url: "https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers"
    date: 2026-10-21
    title: Google's common crawlers - Google Crawling Infrastructure
  - url: "https://platform.openai.com/docs/bots"
    date: 2026-10-21
    title: Overview of OpenAI Crawlers - OpenAI
  - url: "https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler"
    date: 2026-10-21
    title: "Does Anthropic crawl data from the web, and how can site owners block the crawler - Claude Help Center"
  - url: "https://docs.perplexity.ai/guides/bots"
    date: 2026-10-21
    title: Perplexity Crawlers - Perplexity docs
  - url: "https://support.apple.com/en-us/119829"
    date: 2026-10-21
    title: About Applebot - Apple Support
  - url: "https://commoncrawl.org/ccbot"
    date: 2026-10-21
    title: CCBot - Common Crawl
  - url: "https://docs.mistral.ai/robots/"
    date: 2026-10-21
    title: Mistral crawlers - Mistral Docs
  - url: "https://developer.amazon.com/amazonbot"
    date: 2026-10-21
    title: About Amazonbot - Amazon Developer
  - url: "https://duckduckgo.com/duckduckgo-help-pages/results/duckassistbot"
    date: 2026-10-21
    title: Is DuckAssistBot related to DuckDuckGo - DuckDuckGo Help Pages
  - url: "https://blogs.bing.com/webmaster/2026/2/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview/"
    date: 2026-02-10
    title: Introducing AI Performance in Bing Webmaster Tools Public Preview - Bing Webmaster Blog
confidence: high
superseded_by:
tags: [ai-search, technical-seo]
fingerprint: ce43f620774e
trust: high
author: "Vendor documentation (Google, OpenAI, Anthropic, Perplexity, Apple, Common Crawl, Mistral, Amazon, DuckDuckGo, Microsoft)"
year: 2026
---
# AI crawlers and user agents

> [!summary] TL;DR
> Most vendors now split three roles: training crawler, search/index crawler, and user-triggered fetcher.
> Blocking a training token (GPTBot, ClaudeBot, Google-Extended, Applebot-Extended, MistralAI-Training) usually keeps you in that vendor's search; blocking a search token (OAI-SearchBot, PerplexityBot, Claude-SearchBot) removes you from it.
> User-triggered fetchers (ChatGPT-User, Perplexity-User, Amzn-User) may ignore robots.txt by design.

## Explanation
AI companies publish robots.txt tokens so site owners can choose between being used for training, being indexed for AI search, and being fetched live when a user asks. The table below summarises each vendor's own documentation. Two tokens are *control-only* and never appear in logs: **Google-Extended** and **Applebot-Extended** — crawling is done by Googlebot/Applebot, and the token only says how the data may be used.

Key consequences:
- Google's AI Overviews and AI Mode are fed by Googlebot; only snippet controls, noindex or the 2026 Search Console toggle keep content out (Search generative AI control).
- Microsoft Copilot is grounded in Bing's index, so Bingbot access matters (Microsoft Copilot and Bing grounding).
- ChatGPT search requires OAI-SearchBot; blocking GPTBot doesn't affect it (OpenAI crawlers).
- Robots.txt is voluntary; verification and network enforcement are separate problems (Verifying AI crawlers).

## Crawler table (from each vendor's documentation, read 2026-10-21)
| Token | Company | Purpose | Blocking it in robots.txt |
|---|---|---|---|
| Googlebot | Google | Search crawling, incl. AI Overviews/AI Mode | Removes crawl access for Search (use noindex/snippet controls instead) |
| Google-Extended | Google | Control token only: Gemini training + grounding (Gemini Apps, Vertex AI) | No effect on Search or AI Overviews |
| OAI-SearchBot | OpenAI | ChatGPT search inclusion | Not shown in ChatGPT search answers (navigational links possible) |
| GPTBot | OpenAI | Training data | Signals 'don't train' |
| ChatGPT-User | OpenAI | User-triggered fetch | robots.txt 'may not apply' |
| ClaudeBot | Anthropic | Training data | Future content excluded from training |
| Claude-SearchBot | Anthropic | Search indexing | Less visibility in Claude search |
| Claude-User | Anthropic | User-triggered fetch | Claude can't retrieve your page for users |
| PerplexityBot | Perplexity | Search index (not training) | Not surfaced in Perplexity results |
| Perplexity-User | Perplexity | User-triggered fetch | 'Generally ignores robots.txt' |
| Bingbot | Microsoft | Bing index, which grounds Copilot | Out of Bing and Copilot answers |
| Applebot / Applebot-Extended | Apple | Search (Siri, Spotlight, Safari) / training-use control token | Applebot-Extended: no training; still in Apple search |
| CCBot | Common Crawl | Open crawl dataset widely reused for AI | Out of future Common Crawl snapshots |
| MistralAI-Index / -Training / -User | Mistral (EU) | Search index / training / user fetch | Per token |
| Amazonbot / Amzn-SearchBot / Amzn-User | Amazon | Training-possible / Alexa search / user fetch | Per token |
| DuckAssistBot | DuckDuckGo | Real-time fetch for AI answers, no training | Not a source for DuckAssist; organic results unaffected |

## How to use it
- Start from the Playbook - AI crawler access decision matrix (what the client wants: visibility, no training, compensation), then write rules with the Playbook - robots.txt template for AI crawlers.
- Re-check vendor pages every quarter: tokens and descriptions changed repeatedly in 2024–2026 (Google's updates log shows several Google-Extended revisions).
- Community lists such as ai.robots.txt help discover new agents but aren't authoritative.

## Trust & evidence
Trust **high**: every row comes from the vendor's own page opened in this session. Confidence high for stated purposes; actual compliance is not verifiable from these pages (see Perplexity stealth crawling dispute). Meta's crawler page returned 403 and is not included.

## Related
- robots.txt
- OpenAI crawlers
- Anthropic crawlers
- Perplexity
- Google-Extended
- Applebot-Extended
- Common Crawl CCBot
- Mistral crawlers
- Amazon crawlers
- DuckAssistBot
- User-triggered fetchers versus crawlers
- Verifying AI crawlers
- AI crawlers and JavaScript rendering
Meta AI crawlers

## Sources
- [Google's common crawlers - Google Crawling Infrastructure](https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers) · 2026-10-21
- [Overview of OpenAI Crawlers - OpenAI](https://platform.openai.com/docs/bots) · 2026-10-21
- [Does Anthropic crawl data from the web, and how can site owners block the crawler - Claude Help Center](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) · 2026-10-21
- [Perplexity Crawlers - Perplexity docs](https://docs.perplexity.ai/guides/bots) · 2026-10-21
- [About Applebot - Apple Support](https://support.apple.com/en-us/119829) · 2026-10-21
- [CCBot - Common Crawl](https://commoncrawl.org/ccbot) · 2026-10-21
- [Mistral crawlers - Mistral Docs](https://docs.mistral.ai/robots/) · 2026-10-21
- [About Amazonbot - Amazon Developer](https://developer.amazon.com/amazonbot) · 2026-10-21
- [Is DuckAssistBot related to DuckDuckGo - DuckDuckGo Help Pages](https://duckduckgo.com/duckduckgo-help-pages/results/duckassistbot) · 2026-10-21
- [Introducing AI Performance in Bing Webmaster Tools Public Preview - Bing Webmaster Blog](https://blogs.bing.com/webmaster/2026/2/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview/) · 2026-02-10
