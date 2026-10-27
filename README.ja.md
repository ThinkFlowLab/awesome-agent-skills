# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Agent Skills エコシステム精選** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> **Agent Skills**（エージェントが読み込める能力パッケージ）のキュレーションリスト — プロンプト集でも MCP サーバ一覧でもありません。

**対象（収録）：** Anthropic Agent Skills / `SKILL.md` 仕様と実装、移植可能な skill パック、skill マーケット/ディレクトリ、作成・検証ツール、skill の組み合わせと配布の実践。  
**対象外：** 汎用プロンプト / jailbreak 集、MCP サーバ黄頁（→ `awesome-agent-mcp`）、agent フレームワーク一式、読み込み可能な技能パッケージと無関係なプラグインストア。

**マーク：** ⭐ 成熟 / 広く採用 · ☄️ 上昇中 / 注目  
**構成：** Method Family × Domain  
**言語：** 日本語版；主言語は [中文 README.md](README.md)。プロジェクト名とリンクは英語のまま。

### Skills ≠ MCP ≠ Mem（先に読む）

| 概念 | 何か | 本リポジトリ？ |
|---|---|---|
| **Skill** | 読み込み可能な能力説明パッケージ（多くは `SKILL.md`、スクリプト、資源） | ✅ ここ |
| **MCP** | ツール/コンテキストの **プロトコル** と server/client | ❌ → mcp リポ |
| **Mem** | 状態と想起（長期記憶、session） | ❌ → mem リポ |
| **Prompt pack** | 静的プロンプト集、読み込み可能な技能契約なし | ❌ 不収録 |

Skill は MCP ツールを **呼び出したり** Mem を読み書きしたりできる；収録は Skills に含め、依存を注記する。

---

## 貢献 / 収録ルール

- **⭐ Established：** 仕様または実装が多方に引用；文書が充実；実行可能な例または明確な本番利用；公開約 ≥ 6 か月または事実上の標準。
- **☄️ Rising：** 直近 12 か月で活発；`SKILL.md`（または等価契約）が明確；再現可能なインストール/読み込み；portable skills に沿う。
- **必須情報：** スキルが解くタスク、`SKILL.md` 準拠か（等価形式を注記）、リンク、区分、⭐/☄️。
- **却下：** マーケ専用ページ、技能契約ファイルなし、実質 MCP サーバ一覧やプロンプトダンプ、Skills テーマ外。
- PR 歓迎；区分が不明なら先に issue。

---

## 目次

- [Method · Spec & Official](#method--spec--official)
- [Method · Portable Packs](#method--portable-packs)
- [Method · Marketplaces](#method--marketplaces)
- [Method · Authoring Tools](#method--authoring-tools)
- [Method · Loaders & Composition](#method--loaders--composition)
- [Domain · Coding / Research / Office / Ops](#domain--coding--research--office--ops)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & 相互リンク](#related-awesome--相互リンク)
- [License](#license)

---

## Method · Spec & Official

権威ある仕様、参考実装、公式ドキュメント、サンプル skill。

| マーク | プロジェクト | 一言 | リンク |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | オープンな Agent Skills 仕様とドキュメントサイトのソース；AAIF 管理の対象 | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | `SKILL.md` frontmatter / ディレクトリ契約（canonical） | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | 概要と progressive disclosure モデル | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Anthropic 参考 skill ツリー（`skill-creator`、docx/pdf/pptx/xlsx など）；規格は agentskills.io を指す | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | 中立ガバナンスのホーム（Agent Skills を Agentic AI Foundation へ寄付） | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | 寄付の経緯と採用背景 | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | ホストの発見パス（`.cursor/skills/`、`.agents/skills/` など） | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | 公式作成ガイド（フォルダ + `SKILL.md`） | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | 製品 / API 向け概要 | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · Portable Packs

複数ホストにコピーできる技能ディレクトリ：`SKILL.md`、任意の scripts/assets、依存宣言（ツール/MCP/バイナリ）。

| マーク | プロジェクト | 一言 | リンク |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Vercel 公式の移植可能パック（React/Next 実践、デプロイなど）；`npx skills` の主要インストール先の一つ | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | インストール可能な agentic skills + ソフト交付方法論；採用シグナルが強い | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | コーディング agent 向け本番級エンジニアリング技能パック | https://github.com/addyosmani/agent-skills |

**収録基準：** 識別可能な技能マニフェスト（`SKILL.md` または文書で宣言された等価物）+ 再現可能な読み込み手順。純粋な「prompts.md」は不可。

---

## Method · Marketplaces

発見、インストール、バージョン、評価（あれば）。本リポは下記リストと **対等に相互リンク** し、カタログ全体はミラーしない。

| マーク | プロジェクト | 一言 | リンク |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | コミュニティ主導の Agent Skills awesome（多ホスト・多数エントリ）— **対等リスト**、厳選して相互リンク | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | `npx skills` 向け発見 / インストール順位 UI | https://www.skills.sh |

---

## Method · Authoring Tools

タスク記述から `SKILL.md` を生成、権限/パスの lint、スキルが正しく読み込まれるかのテスト。

| マーク | プロジェクト | 一言 | リンク |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | インストール前に agent skills をスキャン（注入・漏洩・サプライチェーンリスク） | https://github.com/NVIDIA/SkillSpector |

> 追加の authoring / optimizer（SkillOpt、SkillCorpus など）は後続波；技能レベルの受入は `awesome-agent-eval` と相互リンク。

---

## Method · Loaders & Composition

ホストが skill をどう発見し、ホットロードし、権限サンドボックスし、複数 skill を編成するか（なお Skills — 汎用 Orchestrator リポではない）。

| マーク | プロジェクト | 一言 | リンク |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — 複数 agent 向けオープンインストール CLI；skills.sh と連携 | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | ホスト + パック導入 cookbook | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Cursor / Claude skill 発見** | 製品内の発見ディレクトリと読み込み規約（Spec 区のドキュメント行を参照） | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · Coding / Research / Office / Ops

### Coding

| マーク | スキルパック | 一言 | リンク |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | デザインテイスト / アートディレクション系スキル（ブラウザ確認含む） | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | アイデアやコードベースからアーキテクチャ図を生成する agent skill | https://github.com/tt-a1i/archify |

> エンジニアリング向け portable pack は [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)、[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)（Portable Packs）も参照。

### Research / Science

| マーク | スキルパック | 一言 | リンク |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | 大規模な科学スキルライブラリ；Agent Skills 標準互換を主張 | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | Reddit/X/YT/HN/Web 横断の直近情報リサーチスキル | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| マーク | スキルパック | 一言 | リンク |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + オープン形式スキル（Markdown / Bases / Canvas） | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills（オフィス例）** | 公式参考ツリーの docx / pdf / pptx / xlsx などのサンプルスキル | https://github.com/anthropics/skills |

### Ops / Data

| マーク | スキルパック | 一言 | リンク |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | 多段階セキュリティ監査スキル；機械可読な findings を出力 | https://github.com/cloudflare/security-audit-skill |
| ☄️ | **yoruuuchan/chatgpt-mcp-connect** | ローカル/ホスト型 MCP サーバを ChatGPT に接続する再現可能なレシピ（Streamable HTTP、stdio ブリッジ、OAuth 2.1、Cloudflare、Tailscale Funnel） | https://github.com/yoruuuchan/chatgpt-mcp-connect |

---

## Contrast · vs MCP / Prompts / Plugins

| 混同しやすいもの | 違い | 送り先 |
|---|---|---|
| MCP server 一覧 | プロトコル端点とツール schema。技能マニュアルではない | `awesome-agent-mcp` |
| Prompt library | 読み込み契約なし、資源/権限モデルなし | 不収録 |
| IDE プラグイン市場 | ホスト UI/API を拡張；必ずしも Agent Skill ではない | `SKILL.md` パックも提供する場合のみ |
| Memory フレームワーク | 状態を保存し「何ができるか」は定義しない | `awesome-agent-mem` |
| 多 agent 編成フレームワーク | Orchestrator；技能は呼び出される単位に過ぎない | 最初の 8 出門リポには含めない |

---

## Related Awesome & 相互リンク

| テーマリポ（予定） | 関係 |
|---|---|
| `awesome-agent-mcp` | Skill が依存として宣言しがちな MCP servers |
| `awesome-agent-mem` | Skill が読み書きしうる記憶バックエンド |
| `awesome-agent-cli` | 端末で skill を読み込む runner |
| `awesome-agent-sandbox` | 技能スクリプトの実行隔離 |
| `awesome-agent-eval` | 技能レベルの受入と軌跡評価 |
| `awesome-agent-rsi` | skill を生成/改訂しうる自己改善フロー |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 対等なコミュニティリスト（ミラーしない） |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — リスト内容は自由に再利用可。

## Disclaimer

本リストは Anthropic、Cursor、OpenAI、Vercel、NVIDIA その他のベンダー/プロジェクトと **無関係**；収録と ⭐/☄️ は **推薦を意味しない**。エントリは読み込み可能な技能契約（`SKILL.md` または等価）を満たす必要があり、star 数 alone は並び順の根拠ではない。

## Maintainers

- ThinkFlowLab / hs（出門 Awesome）

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
