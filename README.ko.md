# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Agent Skills 생태계 큐레이션** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> **Agent Skills**(에이전트가 로드할 수 있는 능력 패키지) 큐레이션 목록 — 프롬프트 라이브러리도, MCP 서버 디렉터리도 아닙니다.

**범위(수):** Anthropic Agent Skills / `SKILL.md` 규격과 구현, 이식 가능한 skill 팩, skill 마켓/디렉터리, 작성·검증 도구, skill 조합·배포 실무.  
**범위 밖:** 일반 프롬프트 / jailbreak 모음, MCP 서버 황페이지(→ `awesome-agent-mcp`), agent 프레임워크 일괄, 로드 가능한 스킬 패키지와 무관한 플러그인 스토어.

**표시:** ⭐ 성숙 / 널리 채택 · ☄️ 상승 중 / 주목  
**구조:** Method Family × Domain  
**언어:** 한국어판; 주 언어는 [中文 README.md](README.md). 프로젝트명과 링크는 영어 유지.

### Skills ≠ MCP ≠ Mem (먼저 읽기)

| 개념 | 무엇인가 | 이 저장소? |
|---|---|---|
| **Skill** | 로드 가능한 능력 설명 패키지(보통 `SKILL.md`, 스크립트, 자원) | ✅ 여기 |
| **MCP** | 도구/컨텍스트 **프로토콜** 과 server/client | ❌ → mcp 저장소 |
| **Mem** | 상태와 회상(장기 기억, session) | ❌ → mem 저장소 |
| **Prompt pack** | 정적 프롬프트 모음, 로드 가능 스킬 계약 없음 | ❌ 미수 |

Skill은 MCP 도구를 **호출**하거나 Mem을 읽고 쓸 수 있음; 수록은 Skills에 두고 의존성을 명시.

---

## 기여 / 수록 규칙

- **⭐ Established:** 규격·구현이 다수에 인용; 문서 충실; 실행 예 또는 명확한 프로덕션 사용; 공개 약 ≥ 6개월 또는 사실상 표준.
- **☄️ Rising:** 최근 12개월 활발; `SKILL.md`(또는 등가 계약) 명확; 재현 가능한 설치/로드; portable skills에 부합.
- **필수 정보:** 스킬이 푸는 과제, `SKILL.md` 준수 여부(등가 형식 명시), 링크, 구역, ⭐/☄️.
- **거절:** 마케팅만 있는 페이지, 스킬 계약 파일 없음, 실질 MCP 서버 목록·프롬프트 덤프, Skills 주제 이탈.
- PR 환영; 구역이 애매하면 먼저 issue.

---

## 목차

- [Method · Spec & Official](#method--spec--official)
- [Method · Portable Packs](#method--portable-packs)
- [Method · Marketplaces](#method--marketplaces)
- [Method · Authoring Tools](#method--authoring-tools)
- [Method · Loaders & Composition](#method--loaders--composition)
- [Domain · Coding / Research / Office / Ops](#domain--coding--research--office--ops)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & 상호 링크](#related-awesome--상호-링크)
- [License](#license)

---

## Method · Spec & Official

권위 있는 규격, 참고 구현, 공식 문서, 예시 skill.

| 표시 | 프로젝트 | 한 줄 | 링크 |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | 오픈 Agent Skills 스펙 및 문서 사이트 소스; AAIF 관리 대상 | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | `SKILL.md` frontmatter / 디렉터리 계약(canonical) | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | 개요와 progressive disclosure 모델 | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Anthropic 참고 skill 트리(`skill-creator`, docx/pdf/pptx/xlsx 등); 표준은 agentskills.io | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | 중립 거버넌스 홈(Agent Skills를 Agentic AI Foundation에 기부) | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | 기부 서사와 채택 배경 | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | 호스트 발견 경로(`.cursor/skills/`, `.agents/skills/` 등) | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | 공식 작성 가이드(폴더 + `SKILL.md`) | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | 제품 / API 지향 개요 | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · Portable Packs

여러 호스트에 복사 가능한 스킬 디렉터리: `SKILL.md`, 선택 scripts/assets, 의존 선언(도구/MCP/바이너리).

| 표시 | 프로젝트 | 한 줄 | 링크 |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Vercel 공식 이식 가능 팩(React/Next 실무, 배포 등); `npx skills` 주요 설치 대상 중 하나 | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | 설치 가능한 agentic skills + 소프트웨어 전달 방법론; 채택 신호 강함 | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | 코딩 agent용 프로덕션급 엔지니어링 스킬 팩 | https://github.com/addyosmani/agent-skills |

**수록 기준:** 식별 가능한 스킬 매니페스트(`SKILL.md` 또는 문서상 등가물) + 재현 가능한 로드 절차. 순수 「prompts.md」는 거절.

---

## Method · Marketplaces

발견, 설치, 버전, 평점(있으면). 이 저장소는 아래 목록과 **대등하게 상호 링크**하며 전체 카탈로그를 미러하지 않음.

| 표시 | 프로젝트 | 한 줄 | 링크 |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | 커뮤니티 선도 Agent Skills awesome(다중 호스트, 다수 항목) — **대등 목록**, 선별 상호 링크 | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | `npx skills`용 발견 / 설치 순위 UI | https://www.skills.sh |

---

## Method · Authoring Tools

과제 설명에서 `SKILL.md` 생성, 권한/경로 lint, 스킬이 올바르게 로드되는지 테스트.

| 표시 | 프로젝트 | 한 줄 | 링크 |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | 설치 전 agent skills 스캔(주입, 유출, 공급망 위험) | https://github.com/NVIDIA/SkillSpector |

> 추가 authoring / optimizer(SkillOpt, SkillCorpus 등)는 이후 웨이브; 스킬 수준 수락은 `awesome-agent-eval`과 상호 링크.

---

## Method · Loaders & Composition

호스트가 skill을 어떻게 발견·핫로드·권한 샌드박스·다중 skill 편성하는지(여전히 Skills — 일반 Orchestrator 저장소 아님).

| 표시 | 프로젝트 | 한 줄 | 링크 |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — 다중 agent용 오픈 설치 CLI; skills.sh와 연동 | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | 호스트 + 팩 설치 cookbook | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Cursor / Claude skill 발견** | 제품 내 발견 디렉터리와 로드 규약(Spec 구역 문서 행 참고) | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · Coding / Research / Office / Ops

### Coding

| 표시 | 스킬 팩 | 한 줄 | 링크 |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | 디자인 취향 / 아트 디렉션 스킬(브라우저 확인 포함) | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | 아이디어나 코드베이스에서 아키텍처 다이어그램을 생성하는 agent skill | https://github.com/tt-a1i/archify |

> 엔지니어링 지향 portable pack은 [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills), [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)(Portable Packs)도 참고.

### Research / Science

| 표시 | 스킬 팩 | 한 줄 | 링크 |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | 대규모 과학 스킬 라이브러리; Agent Skills 표준 호환 주장 | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | Reddit/X/YT/HN/Web 횡단 최근 정보 리서치 스킬 | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| 표시 | 스킬 팩 | 한 줄 | 링크 |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + 개방 형식 스킬(Markdown / Bases / Canvas) | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills（오피스 예시）** | 공식 참고 트리의 docx / pdf / pptx / xlsx 등 예시 스킬 | https://github.com/anthropics/skills |

### Ops / Data

| 표시 | 스킬 팩 | 한 줄 | 링크 |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | 다단계 보안 감사 스킬; 기계 가독 findings 산출 | https://github.com/cloudflare/security-audit-skill |

---

## Contrast · vs MCP / Prompts / Plugins

| 혼동하기 쉬운 것 | 차이 | 보낼 곳 |
|---|---|---|
| MCP server 목록 | 프로토콜 엔드포인트와 도구 schema; 스킬 매뉴얼 아님 | `awesome-agent-mcp` |
| Prompt library | 로드 계약 없음, 자원/권한 모델 없음 | 미수 |
| IDE 플러그인 마켓 | 호스트 UI/API 확장; Agent Skill이 아닐 수 있음 | `SKILL.md` 팩도 제공할 때만 |
| Memory 프레임워크 | 상태를 저장하며 「무엇을 하는가」는 정의하지 않음 | `awesome-agent-mem` |
| 다중 agent 오케스트레이션 | Orchestrator; 스킬은 호출 단위일 뿐 | 첫 8개 출문 저장소에 미포함 |

---

## Related Awesome & 상호 링크

| 테마 저장소(예정) | 관계 |
|---|---|
| `awesome-agent-mcp` | Skill이 의존으로 자주 선언하는 MCP servers |
| `awesome-agent-mem` | Skill이 읽고 쓸 수 있는 기억 백엔드 |
| `awesome-agent-cli` | 터미널에서 skill을 로드하는 runner |
| `awesome-agent-sandbox` | 스킬 스크립트 실행 격리 |
| `awesome-agent-eval` | 스킬 수준 수락 및 궤적 평가 |
| `awesome-agent-rsi` | skill을 생성/개정할 수 있는 자기 개선 흐름 |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 대등 커뮤니티 목록(미러 없음) |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — 목록 내용은 자유롭게 재사용 가능.

## Disclaimer

이 목록은 Anthropic, Cursor, OpenAI, Vercel, NVIDIA 및 기타 벤더/프로젝트와 **무관**하며; 수록과 ⭐/☄️는 **추천이 아님**. 항목은 로드 가능한 스킬 계약(`SKILL.md` 또는 등가)을 충족해야 하며, star 수만으로는 정렬하지 않음.

## Maintainers

- ThinkFlowLab / hs (출문 Awesome)

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
