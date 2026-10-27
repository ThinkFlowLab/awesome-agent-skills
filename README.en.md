# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Curated Agent Skills ecosystem** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> A curated list for **Agent Skills** (capability packages agents can load) — **not** a prompt library, **not** an MCP server directory.

**In scope:** Anthropic Agent Skills / `SKILL.md` specs and implementations, portable skill packs, skill marketplaces/directories, authoring & validation tools, skill composition & distribution practices.  
**Out of scope:** Generic prompt / jailbreak dumps, MCP server yellow pages (→ `awesome-agent-mcp`), agent framework megapacks, plugin stores unrelated to loadable skill packages.

**Markers:** ⭐ Established / widely adopted · ☄️ Rising / watchlist  
**Structure:** Method Family × Domain  
**Languages:** English edition; Chinese is primary at [README.md](README.md). Project names and links stay in English.

### Skills ≠ MCP ≠ Mem (read first)

| Concept | What it is | This repo? |
|---|---|---|
| **Skill** | Loadable capability package (often `SKILL.md`, scripts, assets) | ✅ Here |
| **MCP** | **Protocol** for tools/context and server/client | ❌ → mcp repo |
| **Mem** | State and recall (long-term memory, session) | ❌ → mem repo |
| **Prompt pack** | Static prompt dump with no loadable skill contract | ❌ Rejected |

A Skill may **call** MCP tools or read/write Mem; we still list it under Skills and note the dependency.

---

## Contribution rules

- **⭐ Established:** Spec or impl cited by multiple parties; solid docs; runnable examples or clear production use; public ~≥ 6 months or de-facto standard.
- **☄️ Rising:** Active in the last 12 months; clear `SKILL.md` (or equivalent contract); reproducible install/load; aligned with portable skills.
- **Required:** What task the skill solves, whether it follows `SKILL.md` (or note equivalent), link, section, ⭐/☄️.
- **Reject:** Marketing-only pages, no skill contract file, actually an MCP server list or prompt dump, off-topic for Skills.
- PRs welcome; open an issue first if the section is unclear.

---

## Table of Contents

- [Method · Spec & Official](#method--spec--official)
- [Method · Portable Packs](#method--portable-packs)
- [Method · Marketplaces](#method--marketplaces)
- [Method · Authoring Tools](#method--authoring-tools)
- [Method · Loaders & Composition](#method--loaders--composition)
- [Domain · Coding / Research / Office / Ops](#domain--coding--research--office--ops)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & cross-links](#related-awesome--cross-links)
- [License](#license)

---

## Method · Spec & Official

Authoritative specs, reference implementations, official docs, and example skills.

| Mark | Project | One-liner | Link |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | Open Agent Skills spec and docs site source; AAIF stewardship target | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | `SKILL.md` frontmatter / directory contract (canonical) | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | Overview and progressive disclosure model | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Anthropic reference skill tree (`skill-creator`, docx/pdf/pptx/xlsx, etc.); points to agentskills.io | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | Neutral governance home (Agent Skills donated to Agentic AI Foundation) | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | Donation narrative and adoption context | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | Host discovery paths (`.cursor/skills/`, `.agents/skills/`, etc.) | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | Official authoring guide (folder + `SKILL.md`) | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | Product / API-oriented overview | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · Portable Packs

Skill directories you can copy across hosts: `SKILL.md`, optional scripts/assets, declared deps (tools/MCP/binaries).

| Mark | Project | One-liner | Link |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Official Vercel portable packs (React/Next practices, deploy, etc.); a primary `npx skills` install target | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | Installable agentic skills + software delivery methodology; strong adoption signal | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | Production engineering skill packs for coding agents | https://github.com/addyosmani/agent-skills |

**Bar for inclusion:** A recognizable skill manifest (`SKILL.md` or documented equivalent) + reproducible load steps. Pure “prompts.md” dumps are rejected.

---

## Method · Marketplaces

Discovery, install, versioning, and ratings (when available). This repo **cross-links as a peer** — we do not mirror entire catalogs.

| Mark | Project | One-liner | Link |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | Leading community Agent Skills awesome (multi-host, many entries) — **peer list**, selective cross-link | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | Discovery / install leaderboard UI for `npx skills` | https://www.skills.sh |

---

## Method · Authoring Tools

Generate `SKILL.md` from a task description, lint permissions/paths, test that skills load correctly.

| Mark | Project | One-liner | Link |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | Pre-install scanner for agent skills (injection, exfiltration, supply-chain risk) | https://github.com/NVIDIA/SkillSpector |

> More authoring / optimizers (e.g. SkillOpt, SkillCorpus) in later waves; skill-level acceptance cross-links `awesome-agent-eval`.

---

## Method · Loaders & Composition

How hosts discover skills, hot-load, permission sandboxes, multi-skill orchestration (still Skills — not a generic Orchestrator repo).

| Mark | Project | One-liner | Link |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — open install CLI across many agents; pairs with skills.sh | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | Host + pack install cookbook | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Cursor / Claude skill discovery** | In-product discovery dirs and load conventions (see Spec docs rows) | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · Coding / Research / Office / Ops

### Coding

| Mark | Skill pack | One-liner | Link |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | Design taste / art-direction skills (incl. browser checks) | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | Agent skill that generates architecture diagrams from ideas or codebases | https://github.com/tt-a1i/archify |

> Engineering-oriented portable packs also appear under [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) and [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) (Portable Packs).

### Research / Science

| Mark | Skill pack | One-liner | Link |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | Large scientific skill library; claims Agent Skills standard compatibility | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | Recent-info research skill across Reddit/X/YT/HN/Web | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| Mark | Skill pack | One-liner | Link |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + open-format skills (Markdown / Bases / Canvas) | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills (office examples)** | Official reference tree examples: docx / pdf / pptx / xlsx, etc. | https://github.com/anthropics/skills |

### Ops / Data

| Mark | Skill pack | One-liner | Link |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | Multi-stage security audit skill with machine-readable findings | https://github.com/cloudflare/security-audit-skill |
| ☄️ | **yoruuuchan/chatgpt-mcp-connect** | Reproducible recipes for connecting local and hosted MCP servers to ChatGPT (Streamable HTTP, stdio bridges, OAuth 2.1, Cloudflare, Tailscale Funnel) | https://github.com/yoruuuchan/chatgpt-mcp-connect |

---

## Contrast · vs MCP / Prompts / Plugins

| Easy to confuse | Difference | Send to |
|---|---|---|
| MCP server lists | Protocol endpoints & tool schemas, not skill manuals | `awesome-agent-mcp` |
| Prompt library | No load contract, no resource/permission model | Rejected |
| IDE plugin markets | Extend host UI/API; may not be an Agent Skill | Only if they also ship a `SKILL.md` pack |
| Memory frameworks | Store state; do not define “what I can do” | `awesome-agent-mem` |
| Multi-agent orchestration | Orchestrator; skills are just callable units | Not in the first 8 launch repos |

---

## Related Awesome & cross-links

| Theme repo (planned) | Relationship |
|---|---|
| `awesome-agent-mcp` | MCP servers Skills often declare as deps |
| `awesome-agent-mem` | Memory backends Skills may read/write |
| `awesome-agent-cli` | Terminal runners that load skills |
| `awesome-agent-sandbox` | Execution isolation for skill scripts |
| `awesome-agent-eval` | Skill-level acceptance & trajectory eval |
| `awesome-agent-rsi` | Self-improvement loops that produce/revise skills |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | Peer community list (no mirroring) |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — list content is free to reuse.

## Disclaimer

This list is **not affiliated** with Anthropic, Cursor, OpenAI, Vercel, NVIDIA, or other vendors/projects; inclusion and ⭐/☄️ are **not endorsements**. Entries must meet a loadable skill contract (`SKILL.md` or equivalent); star count alone is not a ranking key.

## Maintainers

- ThinkFlowLab / hs (launch Awesome)

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
