# Agent-Reach (Python) — Research Intake Bootstrap English

## Sentence as Program

When UNA needs to research something, invoke agent-reach with the channel that matches the intent, run doctor before any multi-backend platform, and file the result as an IDEA-NNNN birth token with an incorporate-or-reject verdict.

## What This Is

Panniantong/Agent-Reach — Python 3.10+, MIT, ~99K stars, #1 GitHub Trending repo of the day (2026-10-18). One-click internet for AI agents. Not a proxy. An installer and router: it pip-installs a CLI called agent-reach, checks the environment, wires backend tools for sixteen platforms, health-checks them with a doctor command, and gets out of the way while the agent calls those tools directly.

Forked to marvelousempire/Agent-Reach on 2026-10-18. nephew-integration branch cut from main at 94f06c1.

## Complement to bojieli/agentreach

Two different projects, two different jobs.

- bojieli/agentreach (Go, MIT, v0.8, ~180 stars): remote-execution proxy. Agent brain stays local. Shell and file ops run on a remote box over SSH ControlMaster. No FUSE. Forked to marvelousempire/agentreach, nephew-integration branch.
- Panniantong/Agent-Reach (Python, MIT, ~99K stars): research intake. Agent reads the public web — GitHub, YouTube, RSS, Twitter, Reddit, and more — through sixteen channel backends.

Hands and eyes. agentreach moves work to a remote box. Agent-Reach brings the world to the agent.

## Channel Routing (SKILL.md Pattern)

The SKILL.md file is a routing table: which backend to call for which intent, with a hard rule to run doctor before touching any multi-backend platform. That maps one-to-one onto a bootstrap English manifest.

### Core Channels (research intake)

1. GitHub (gh CLI) — read and search repos
2. Web (Jina Reader) — any URL
3. Exa — semantic web search
4. RSS (feedparser) — project blogs and changelogs
5. YouTube (yt-dlp) — demos and tutorials
6. Twitter (twitter-cli) — dev-community signal

### Secondary Channels

7. Reddit — user feedback on products under evaluation
8. V2EX — Chinese tech scene where upstream CLIs live

### Noise Channels (not for research intake)

Facebook, Instagram, XiaoHongShu, Xueqiu, Xiaoyuzhou, Boss — social, shopping, finance, job-board. None feed a feature-research pipeline.

## Doctor Health-Check

The doctor command health-checks every backend before use. If a backend dies — Bilibili blocked yt-dlp — it silently switches to the fallback (bili-cli) without notice. Doctor is the gate: no multi-backend call without a passing check.

As an Automata micro-slice, doctor becomes a health-check node that reports channel status to Nephew Charts.

## Design Tension: Workspace Writes

Agent-Reach refuses to write files in the agent workspace. Everything goes to dot-agent-reach or tmp. The SNF container model wants state inside the egg. Two options: relax the rule for the UNA slice, or treat dot-agent-reach as an external mount the slice owns.

## Open Questions for Super Rick / Scrappy

1. Backend host split — M5 Max versus DGX Spark for running channel backends.
2. Doctor as Automata micro-slice reporting to Nephew Charts — yes or no.
3. SKILL.md as manifest node versus file UNA reads directly.
4. IDEA-token incorporate/reject SLA — how fast must a research intake resolve.
5. SNF state tension — dot-agent-reach/tmp versus egg-internal storage.
6. Data normalization across platforms — Agent-Reach does not normalize. Who does?
7. Untrusted web content safety — research intake is not a sanitization layer.

## CCK Resolution

- Super Rick (Ace of Hearts): is this the best research-intake shape it can be?
- Scrappy Doo (Ace of Diamonds): is this the smallest thing that does intake completely?

## Immutable Receipt

- Fork: marvelousempire/Agent-Reach @ 94f06c1 (2026-10-18)
- Branch: nephew-integration
- Bootstrap ticket: this file
- Cross-link: docs/investigations/agent-reach-research-intake-bootstrap-english.md in marvelousempire/nephew (commit 499c9ce)
- Related fork: marvelousempire/agentreach (bojieli, Go, nephew-integration branch)

## UNA Check

Verb: research. Noun: intake. Adjective: guarded. Guarded research intake through channel-routed backends with doctor-gated multi-backend calls.
