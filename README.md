# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> **Agent Skills 生态精选** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> Curated list for **Agent Skills** (capability packages agents can load) — **not** a prompt library, **not** an MCP server directory.

**In scope（收）：** Anthropic Agent Skills / `SKILL.md` 规范与实现、可移植 skill 包、skill 市场/目录、编写与校验工具、skill 组合与分发实践。  
**Out of scope（不收）：** 通用 prompt / jailbreak 合集、MCP server 黄页（→ `awesome-agent-mcp`）、agent 框架全家桶、与「可加载技能包」无关的插件商店。

**标记：** ⭐ 成熟 / 广泛采用 · ☄️ 上升中 / 值得盯  
**结构：** Method Family × Domain  
**语言：** 中文说明为主；项目名与链接保留英文

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
| ⭐ 示例 | **Anthropic Agent Skills** | Agent Skills / `SKILL.md` 官方说明与约定 | https://www.anthropic.com （文档入口以官网为准） |
| ⭐ 示例 | **Claude / Cursor Skill 约定** | 宿主如何发现与加载 skill 目录 | _填各产品文档实链_ |
| ☄️ 示例 | **Agent Skills 开放讨论 / RFC** | 跨宿主可移植技能契约社区草案 | _填实链_ |
| 示例 | **官方 example skills** | hello-world、domain 示例包 | _填 repo_ |
| 示例 | _（占位）SKILL.md schema_ | 字段、权限、资源约定 | URL |

> 表中 **「示例」** 为骨架占位；开仓后换成核实过的规范与文档链接。

---

## Method · 可移植 Skill 包 Portable Packs

可复制到多宿主的技能目录：含 `SKILL.md`、可选 scripts/assets、声明依赖（工具/MCP/二进制）。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ 示例 | **awesome-cursor-skills 类合集** | 社区 skill 包索引（若遵循 SKILL.md） | _填实链_ |
| 示例 | **docx / pptx / spreadsheet skills** | 办公文档类可加载技能（本 bot 生态亦有） | _填实链_ |
| 示例 | **browser / search skills** | 浏览与检索类 portable pack | _填实链_ |
| 示例 | **git / PR review skills** | 源码工作流技能包 | _填实链_ |
| 示例 | _（占位）org-skills-monorepo_ | 某组织的标准技能单仓 | URL |

**收录门槛：** 至少有可识别的技能清单文件（`SKILL.md` 或文档中声明的等价物）+ 可复现的加载步骤。纯「提示词.md」不收。

---

## Method · Skill 市场与目录 Marketplaces

发现、安装、版本与评分（若有）。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ 示例 | **Skill registry / directory** | 可搜索的 skill 目录 | _填实链_ |
| 示例 | **GitHub topic: agent-skills** | 用 topic/标签发现技能仓 | https://github.com/topics/ |
| 示例 | **宿主应用内 skill 商店** | 产品内发现与一键启用 | _产品页_ |
| 示例 | _（占位）Private skill catalog_ | 企业内部技能目录 | URL |

---

## Method · 编写 / 校验 / 脚手架 Authoring Tools

从任务描述生成 `SKILL.md`、lint 权限与路径、测试技能是否被正确加载。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ☄️ 示例 | **skill-creator / skill-authoring** | 编写与评审可复用 Agent Skill | _填实链（如各 org 的 skill-creator）_ |
| 示例 | **SKILL.md linter** | 校验 frontmatter、路径、危险权限 | URL |
| 示例 | **skill init CLI** | 脚手架生成标准目录结构 | URL |
| 示例 | **eval harness for skills** | 技能级验收（互链 awesome-agent-eval） | URL |
| 示例 | _（占位）_ | 从演示录像归纳 skill（learn-from-demonstration 类） | URL |

---

## Method · Runtime 加载与组合 Loaders & Composition

宿主如何发现 skill、热加载、权限沙箱、多 skill 编排（仍属 Skills，不是通用 Orchestrator 仓）。

| 标记 | 项目 | 一句话 | 链接 |
|---|---|---|---|
| ⭐ 示例 | **Cursor / Claude 内置 skill loader** | 约定目录与触发方式 | _产品文档_ |
| ☄️ 示例 | **Open skill runtime** | 开源宿主对 SKILL.md 的加载器 | _填实链_ |
| 示例 | **Skill + MCP bridge** | 技能声明所需 MCP server | 互链 mcp 仓 |
| 示例 | _（占位）Skill composition graph_ | 多技能依赖与冲突解决 | URL |

---

## Domain · 编码 / 研究 / 办公 / 运维

### Coding

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| 示例 | **PR review skill** | 按仓库规范审 PR | URL |
| 示例 | **test-generation skill** | 按 CI 层级补测 | URL |
| 示例 | _（占位）_ | monorepo 迁移技能 | URL |

### Research / Science

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| 示例 | **literature-search skill** | 文献检索与引用规范 | URL |
| 示例 | **citation-reviewer skill** | 核对引用是否张冠李戴 | URL |
| 示例 | _（占位）_ | 实验记录技能 | URL |

### Office / Docs

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| 示例 | **docx / pptx / sheets skills** | 办公文档生成与修改 | URL |
| 示例 | _（占位）_ | 会议纪要 → 任务技能 | URL |

### Ops / Data

| 标记 | 技能包 | 一句话 | 链接 |
|---|---|---|---|
| 示例 | **runbook skill** | 受控排障步骤包 | URL |
| 示例 | _（占位）_ | 数仓查询技能（声明只读） | URL |

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

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — 列表内容可自由复用。

## Disclaimer

本列表与 Anthropic、Cursor、OpenAI 及其他厂商/项目 **无隶属关系**；收录与 ⭐/☄️ **不构成背书**。标 **「示例」** 的行为草稿占位，发布前须逐条核实链接与是否符合 `SKILL.md`（或等价）契约。

## Maintainers

- ThinkFlowLab / hs（出门 Awesome）

**Last updated:** 2026-10-26 (Asia/Shanghai) · draft skeleton only · **repo not published**
