# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Agent Skills 生态精选** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> Curated list for **Agent Skills** (capability packages agents can load) — **not** a prompt library, **not** an MCP server directory.

**In scope（收）：** Anthropic Agent Skills / `SKILL.md` 规范与实现、可移植 skill 包、skill 市场/目录、编写与校验工具、skill 组合与分发实践。  
**Out of scope（不收）：** 通用 prompt / jailbreak 合集、MCP server 黄页（→ `awesome-agent-mcp`）、agent 框架全家桶、与「可加载技能包」无关的插件商店。

**标记：** ⭐ 成熟 / 广泛采用 · ☄️ 上升中 / 值得盯  
**结构：** Method Family × Domain  
**语言：** 中文说明为主；另有 [English](README.en.md) / [日本語](README.ja.md) / [한국어](README.ko.md) / [Français](README.fr.md) / [Español](README.es.md)；项目名与链接保留英文

### Skills ≠ MCP ≠ Mem（先读）

| 概念 | 是什么 | 本仓？ |
|---|---|---|
| **Skill** | 可加载的能力说明包（常含 `SKILL.md`、脚本、资源） | ✅ 本仓 |
| **MCP** | 工具/上下文的 **协议** 与 server/client | ❌ → mcp 仓 |
| **Mem** | 状态与回忆（长期记忆、session） | ❌ → mem 仓 |
| **Prompt pack** | 静态提示词合集，无可加载技能契约 | ❌ 不收 |

Skill 可以 **调用** MCP 工具或读写 Mem；收录时仍归 Skills，并在条目中注明依赖。

---

## 贡献 / 收录规则 · Contribution

- **⭐ Established：** 规范或实现已被多方引用；文档完整；有可运行示例或明确生产用法；公开约 ≥ 6 个月或已成事实标准。
- **☄️ Rising：** 近 12 个月活跃；`SKILL.md`（或等价契约）清晰；可复现安装/加载；方向对齐 portable skills。
- **必备信息：** 技能解决什么任务、是否遵循 `SKILL.md`（或注明等价格式）、链接、分区、⭐/☄️。
- **拒收：** 仅有营销页、无技能契约文件、实为 MCP server 列表或 prompt dump、与 Skills 主题越界。
- 欢迎 PR；分区不准先开 issue。

---

## 目录 · Table of Contents

- [Method · 规范与官方生态 Spec & Official](#method--规范与官方生态-spec--official)
- [Method · 可移植 Skill 包 Portable Packs](#method--可移植-skill-包-portable-packs)
- [Method · Skill 市场与目录 Marketplaces](#method--skill-市场与目录-marketplaces)
- [Method · 编写 / 校验 / 脚手架 Authoring Tools](#method--编写--校验--脚手架-authoring-tools)
- [Method · Runtime 加载与组合 Loaders & Composition](#method--runtime-加载与组合-loaders--composition)
- [Domain · 编码 / 研究 / 办公 / 运维](#domain--编码--研究--办公--运维)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & 互链](#related-awesome--互链)
- [License](#license)

---

## Method · 规范与官方生态 Spec & Official

权威规范、参考实现、官方文档与示例 skill。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | 开放 Agent Skills 规范与文档站源码；AAIF 托管目标 | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | `SKILL.md` frontmatter / 目录契约（canonical） | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | 总览与 progressive disclosure 模型 | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Anthropic 参考 skill 树（`skill-creator`、docx/pdf/pptx/xlsx 等）；标准指向 agentskills.io | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | 中立治理主页（Agent Skills 捐赠至 Agentic AI Foundation） | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | 捐赠叙事与采纳背景 | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | 宿主发现路径（`.cursor/skills/`、`.agents/skills/` 等） | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | 官方编写指南（文件夹 + `SKILL.md`） | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | 产品 / API 向总览 | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · 可移植 Skill 包 Portable Packs

可复制到多宿主的技能目录：含 `SKILL.md`、可选 scripts/assets、声明依赖（工具/MCP/二进制）。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Vercel 官方可移植包（React/Next 实践、部署等）；`npx skills` 主安装目标之一 | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | 可安装的 agentic skills + 软件交付方法论，采用信号强 | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | 面向编码 agent 的生产级工程技能包 | https://github.com/addyosmani/agent-skills |

**收录门槛：** 至少有可识别的技能清单文件（`SKILL.md` 或文档中声明的等价物）+ 可复现的加载步骤。纯「提示词.md」不收。

---

## Method · Skill 市场与目录 Marketplaces

发现、安装、版本与评分（若有）。本仓与下列列表 **互链对等**，不整仓镜像条目。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | 社区领先的 Agent Skills awesome（多宿主、大量技能条目）— **对等列表**，择优互链 | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | 面向 `npx skills` 的发现 / 安装排行榜 UI | https://www.skills.sh |

---

## Method · 编写 / 校验 / 脚手架 Authoring Tools

从任务描述生成 `SKILL.md`、lint 权限与路径、测试技能是否被正确加载。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | 安装前扫描 agent skills（注入、外泄、供应链风险） | https://github.com/NVIDIA/SkillSpector |

> 更多 authoring / optimizer（如 SkillOpt、SkillCorpus）见后续波次；技能级验收互链 `awesome-agent-eval`。

---

## Method · Runtime 加载与组合 Loaders & Composition

宿主如何发现 skill、热加载、权限沙箱、多 skill 编排（仍属 Skills，不是通用 Orchestrator 仓）。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — 跨多 agent 的开放安装 CLI；与 skills.sh 配套 | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | 宿主 + 包安装 cookbook | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Cursor / Claude skill 发现** | 产品内约定目录与加载方式（见 Spec 区文档行） | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · 编码 / 研究 / 办公 / 运维

### Coding

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | 设计品味 / 艺术指导类技能（含浏览器核对） | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | 从想法或代码库生成架构图的 agent skill | https://github.com/tt-a1i/archify |

> 工程向 portable pack 亦见 [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)、[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)（Portable Packs 区）。

### Research / Science

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | 大规模科学技能库；宣称兼容 Agent Skills 标准 | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | 跨 Reddit/X/YT/HN/Web 的近期信息综合研究技能 | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + 开放格式技能（Markdown / Bases / Canvas） | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills（办公示例）** | 官方参考树中的 docx / pdf / pptx / xlsx 等示例技能 | https://github.com/anthropics/skills |

### Ops / Data

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | 多阶段安全审计技能，产出机器可读 findings | https://github.com/cloudflare/security-audit-skill |
| ☄️ | **yoruuuchan/chatgpt-mcp-connect** | MCP 服务器接入 ChatGPT 的可复现配方（Streamable HTTP、stdio 桥、OAuth 2.1、Cloudflare、Tailscale Funnel） | https://github.com/yoruuuchan/chatgpt-mcp-connect |

---

## Contrast · vs MCP / Prompts / Plugins

| 容易混淆 | 差异 | 应投递 |
|---|---|---|
| MCP server 列表 | 协议端点与工具 schema，不是技能说明书 | `awesome-agent-mcp` |
| Prompt library | 无加载契约、无资源/权限模型 | 不收 |
| IDE 插件市场 | 扩展宿主 UI/API，未必是 Agent Skill | 除非同时提供 `SKILL.md` 包 |
| Memory 框架 | 存状态，不定义「会做什么」 | `awesome-agent-mem` |
| 多 agent 编排框架 | Orchestrator；技能只是可被调用的单元 | 暂不进 8 条出门仓 |

---

## Related Awesome & 互链

| 主题仓（拟定） | 关系 |
|---|---|
| `awesome-agent-mcp` | Skill 常声明依赖的 MCP servers |
| `awesome-agent-mem` | Skill 可读写的记忆后端 |
| `awesome-agent-cli` | 终端内加载 skill 的 runner |
| `awesome-agent-sandbox` | 技能脚本的执行隔离 |
| `awesome-agent-eval` | 技能级验收与轨迹评测 |
| `awesome-agent-rsi` | 自改进流程可产出/修订 skill |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 对等社区列表（不镜像） |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — 列表内容可自由复用。

## Disclaimer

本列表与 Anthropic、Cursor、OpenAI、Vercel、NVIDIA 及其他厂商/项目 **无隶属关系**；收录与 ⭐/☄️ **不构成背书**。条目须符合可加载技能契约（`SKILL.md` 或等价）；星标数量 alone 不是排序依据。

## Maintainers

- ThinkFlowLab / hs（出门 Awesome）

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
