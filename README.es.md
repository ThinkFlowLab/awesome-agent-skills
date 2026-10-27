# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Ecosistema Agent Skills curado** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> Lista curada de **Agent Skills** (paquetes de capacidades que un agente puede cargar) — **no** es una librería de prompts, **no** es un directorio de servidores MCP.

**En alcance:** especificaciones e implementaciones Anthropic Agent Skills / `SKILL.md`, packs de skills portables, marketplaces/directorios, herramientas de autoría y validación, prácticas de composición y distribución.  
**Fuera de alcance:** dumps genéricos de prompts / jailbreaks, páginas amarillas MCP (→ `awesome-agent-mcp`), megapacks de frameworks agent, tiendas de plugins sin paquete de skill cargable.

**Marcadores:** ⭐ Establecido / ampliamente adoptado · ☄️ En ascenso / a vigilar  
**Estructura:** Method Family × Domain  
**Idiomas:** edición en español; el chino es primario en [README.md](README.md). Nombres de proyecto y enlaces se mantienen en inglés.

### Skills ≠ MCP ≠ Mem (leer primero)

| Concepto | Qué es | ¿Este repo? |
|---|---|---|
| **Skill** | Paquete de capacidades cargable (a menudo `SKILL.md`, scripts, assets) | ✅ Aquí |
| **MCP** | **Protocolo** de herramientas/contexto y server/client | ❌ → repo mcp |
| **Mem** | Estado y recuerdo (memoria a largo plazo, session) | ❌ → repo mem |
| **Prompt pack** | Dump estático de prompts sin contrato de skill cargable | ❌ Rechazado |

Un Skill puede **llamar** herramientas MCP o leer/escribir Mem; lo listamos bajo Skills y anotamos la dependencia.

---

## Reglas de contribución

- **⭐ Established:** Spec o impl citada por varias partes; docs sólidas; ejemplos ejecutables o uso en producción claro; público ~≥ 6 meses o estándar de facto.
- **☄️ Rising:** Activo en los últimos 12 meses; `SKILL.md` (o contrato equivalente) claro; install/load reproducible; alineado con portable skills.
- **Requerido:** Qué tarea resuelve, si sigue `SKILL.md` (o nota equivalente), enlace, sección, ⭐/☄️.
- **Rechazo:** Solo marketing, sin archivo de contrato, en realidad lista MCP o dump de prompts, fuera de tema Skills.
- PRs bienvenidos; abre un issue si la sección no está clara.

---

## Tabla de contenidos

- [Method · Spec & Official](#method--spec--official)
- [Method · Portable Packs](#method--portable-packs)
- [Method · Marketplaces](#method--marketplaces)
- [Method · Authoring Tools](#method--authoring-tools)
- [Method · Loaders & Composition](#method--loaders--composition)
- [Domain · Coding / Research / Office / Ops](#domain--coding--research--office--ops)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & enlaces cruzados](#related-awesome--enlaces-cruzados)
- [License](#license)

---

## Method · Spec & Official

Especificaciones autoritativas, implementaciones de referencia, docs oficiales y skills de ejemplo.

| Marca | Proyecto | En una frase | Enlace |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | Especificación abierta Agent Skills y código del sitio de docs; objetivo de stewardship AAIF | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | Contrato frontmatter / directorio de `SKILL.md` (canonical) | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | Resumen y modelo de progressive disclosure | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Árbol de skills de referencia de Anthropic (`skill-creator`, docx/pdf/pptx/xlsx, etc.); apunta a agentskills.io | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | Inicio de gobernanza neutral (Agent Skills donado a Agentic AI Foundation) | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | Narrativa de la donación y contexto de adopción | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | Rutas de descubrimiento del host (`.cursor/skills/`, `.agents/skills/`, etc.) | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | Guía oficial de autoría (carpeta + `SKILL.md`) | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | Resumen orientado a producto / API | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · Portable Packs

Directorios de skills copiables entre hosts: `SKILL.md`, scripts/assets opcionales, deps declaradas (herramientas/MCP/binarios).

| Marca | Proyecto | En una frase | Enlace |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Packs portables oficiales de Vercel (prácticas React/Next, deploy, etc.); uno de los destinos principales de `npx skills` | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | Skills agenticos instalables + metodología de entrega de software; fuerte señal de adopción | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | Packs de ingeniería de producción para agentes de código | https://github.com/addyosmani/agent-skills |

**Umbral:** Manifiesto de skill reconocible (`SKILL.md` o equivalente documentado) + pasos de carga reproducibles. Los puros «prompts.md» se rechazan.

---

## Method · Marketplaces

Descubrimiento, instalación, versiones y valoraciones (si hay). Este repo **enlaza como par** — no espejamos catálogos enteros.

| Marca | Proyecto | En una frase | Enlace |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | Awesome de Agent Skills líder en la comunidad (multi-host, muchas entradas) — **lista par**, enlaces cruzados selectivos | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | UI de descubrimiento / ranking de instalación para `npx skills` | https://www.skills.sh |

---

## Method · Authoring Tools

Generar `SKILL.md` desde una descripción de tarea, lint de permisos/rutas, probar que los skills cargan bien.

| Marca | Proyecto | En una frase | Enlace |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | Escáner preinstalación de agent skills (inyección, exfiltración, riesgo de supply chain) | https://github.com/NVIDIA/SkillSpector |

> Más authoring / optimizers (SkillOpt, SkillCorpus, etc.) en oleadas posteriores; la aceptación a nivel skill enlaza con `awesome-agent-eval`.

---

## Method · Loaders & Composition

Cómo los hosts descubren skills, hot-load, sandboxes de permisos, orquestación multi-skill (sigue siendo Skills — no un repo Orchestrator genérico).

| Marca | Proyecto | En una frase | Enlace |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — CLI abierta de instalación multi-agente; acompaña a skills.sh | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | Cookbook de instalación host + packs | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Descubrimiento Cursor / Claude skills** | Directorios de descubrimiento y convenciones de carga in-product (ver filas Spec) | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · Coding / Research / Office / Ops

### Coding

| Marca | Pack de skills | En una frase | Enlace |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | Skills de gusto de diseño / dirección artística (incl. comprobaciones en navegador) | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | Skill de agente que genera diagramas de arquitectura desde ideas o codebases | https://github.com/tt-a1i/archify |

> Los packs portables orientados a ingeniería también están en [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) y [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) (Portable Packs).

### Research / Science

| Marca | Pack de skills | En una frase | Enlace |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | Gran biblioteca de skills científicas; afirma compatibilidad con el estándar Agent Skills | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | Skill de investigación de info reciente en Reddit/X/YT/HN/Web | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| Marca | Pack de skills | En una frase | Enlace |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + skills de formatos abiertos (Markdown / Bases / Canvas) | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills (ejemplos office)** | Ejemplos oficiales del árbol de referencia: docx / pdf / pptx / xlsx, etc. | https://github.com/anthropics/skills |

### Ops / Data

| Marca | Pack de skills | En una frase | Enlace |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | Skill de auditoría de seguridad multi-etapa con findings legibles por máquina | https://github.com/cloudflare/security-audit-skill |
| ☄️ | **yoruuuchan/chatgpt-mcp-connect** | Recetas reproducibles para conectar servidores MCP locales/alojados a ChatGPT (Streamable HTTP, puentes stdio, OAuth 2.1, Cloudflare, Tailscale Funnel) | https://github.com/yoruuuchan/chatgpt-mcp-connect |

---

## Contrast · vs MCP / Prompts / Plugins

| Fácil de confundir | Diferencia | Enviar a |
|---|---|---|
| Listas de servidores MCP | Endpoints de protocolo y schemas de herramientas, no manuales de skill | `awesome-agent-mcp` |
| Prompt library | Sin contrato de carga, sin modelo de recurso/permiso | Rechazado |
| Mercados de plugins IDE | Extienden UI/API del host; puede no ser Agent Skill | Solo si también ofrecen un pack `SKILL.md` |
| Frameworks Memory | Guardan estado; no definen «qué sé hacer» | `awesome-agent-mem` |
| Orquestación multi-agente | Orchestrator; los skills son solo unidades invocables | No en los 8 repos de lanzamiento |

---

## Related Awesome & enlaces cruzados

| Repo temático (previsto) | Relación |
|---|---|
| `awesome-agent-mcp` | Servidores MCP que los Skills suelen declarar como deps |
| `awesome-agent-mem` | Backends de memoria que los Skills pueden leer/escribir |
| `awesome-agent-cli` | Runners de terminal que cargan skills |
| `awesome-agent-sandbox` | Aislamiento de ejecución de scripts de skill |
| `awesome-agent-eval` | Aceptación a nivel skill y evaluación de trayectorias |
| `awesome-agent-rsi` | Bucles de auto-mejora que producen/revisan skills |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | Lista comunitaria par (sin espejo) |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — el contenido de la lista es de libre reutilización.

## Disclaimer

Esta lista **no está afiliada** con Anthropic, Cursor, OpenAI, Vercel, NVIDIA ni otros vendors/proyectos; la inclusión y ⭐/☄️ **no son endorsements**. Las entradas deben cumplir un contrato de skill cargable (`SKILL.md` o equivalente); el número de estrellas alone no es clave de ordenación.

## Maintainers

- ThinkFlowLab / hs (Awesome de lanzamiento)

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
