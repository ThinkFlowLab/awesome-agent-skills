# Awesome Agent Skills

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.en.md) · [中文](README.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Español](README.es.md)

> **Écosystème Agent Skills sélectionné** · `SKILL.md` · portable skill packs · marketplaces · authoring tools  
> Liste curatée pour les **Agent Skills** (paquets de capacités qu’un agent peut charger) — **pas** une bibliothèque de prompts, **pas** un annuaire de serveurs MCP.

**Dans le périmètre :** spécifications et implémentations Anthropic Agent Skills / `SKILL.md`, packs de skills portables, marketplaces/répertoires, outils d’écriture & validation, pratiques de composition & distribution.  
**Hors périmètre :** dumps de prompts / jailbreaks génériques, pages jaunes MCP (→ `awesome-agent-mcp`), méga-packs de frameworks agent, stores de plugins sans paquet de skill chargeable.

**Marqueurs :** ⭐ Établi / largement adopté · ☄️ En hausse / à surveiller  
**Structure :** Method Family × Domain  
**Langues :** édition française ; le chinois est primaire dans [README.md](README.md). Noms de projets et liens restent en anglais.

### Skills ≠ MCP ≠ Mem (à lire d’abord)

| Concept | Qu’est-ce que c’est | Ce dépôt ? |
|---|---|---|
| **Skill** | Paquet de capacités chargeable (souvent `SKILL.md`, scripts, assets) | ✅ Ici |
| **MCP** | **Protocole** outils/contexte et server/client | ❌ → dépôt mcp |
| **Mem** | État et rappel (mémoire long terme, session) | ❌ → dépôt mem |
| **Prompt pack** | Dump de prompts statiques sans contrat de skill chargeable | ❌ Rejeté |

Un Skill peut **appeler** des outils MCP ou lire/écrire Mem ; on le classe quand même sous Skills et on note la dépendance.

---

## Règles de contribution

- **⭐ Established :** Spec ou impl citée par plusieurs parties ; docs solides ; exemples exécutables ou usage prod clair ; public ~≥ 6 mois ou standard de fait.
- **☄️ Rising :** Actif sur 12 mois ; `SKILL.md` (ou contrat équivalent) clair ; install/load reproductible ; aligné sur les portable skills.
- **Requis :** Tâche résolue, conformité `SKILL.md` (ou note d’équivalent), lien, section, ⭐/☄️.
- **Rejet :** Page marketing seule, pas de fichier de contrat, liste MCP ou dump de prompts déguisé, hors sujet Skills.
- PR bienvenues ; ouvrez une issue si la section est ambiguë.

---

## Table des matières

- [Method · Spec & Official](#method--spec--official)
- [Method · Portable Packs](#method--portable-packs)
- [Method · Marketplaces](#method--marketplaces)
- [Method · Authoring Tools](#method--authoring-tools)
- [Method · Loaders & Composition](#method--loaders--composition)
- [Domain · Coding / Research / Office / Ops](#domain--coding--research--office--ops)
- [Contrast · vs MCP / Prompts / Plugins](#contrast--vs-mcp--prompts--plugins)
- [Related Awesome & liens croisés](#related-awesome--liens-croisés)
- [License](#license)

---

## Method · Spec & Official

Spécifications faisant autorité, implémentations de référence, docs officielles et skills d’exemple.

| Marqueur | Projet | En une phrase | Lien |
|---|---|---|---|
| ⭐ | **agentskills/agentskills** | Spécification ouverte Agent Skills et sources du site doc ; cible de stewardship AAIF | https://github.com/agentskills/agentskills |
| ⭐ | **Agent Skills Specification** | Contrat frontmatter / répertoire `SKILL.md` (canonical) | https://agentskills.io/specification |
| ⭐ | **Agent Skills home** | Vue d’ensemble et modèle de progressive disclosure | https://agentskills.io/home |
| ⭐ | **anthropics/skills** | Arbre de skills de référence Anthropic (`skill-creator`, docx/pdf/pptx/xlsx, etc.) ; pointe vers agentskills.io | https://github.com/anthropics/skills |
| ⭐ | **AAIF · Skills** | Page de gouvernance neutre (Agent Skills donné à l’Agentic AI Foundation) | https://aaif.io/projects/skills |
| ⭐ | **Anthropic donation note** | Récit du don et contexte d’adoption | https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation |
| ⭐ | **Cursor Agent Skills docs** | Chemins de découverte hôte (`.cursor/skills/`, `.agents/skills/`, etc.) | https://cursor.com/docs/skills |
| ⭐ | **Claude · create custom skills** | Guide officiel d’écriture (dossier + `SKILL.md`) | https://claude.com/docs/skills/how-to |
| ⭐ | **Claude platform · Agent Skills overview** | Vue d’ensemble produit / API | https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview |

---

## Method · Portable Packs

Répertoires de skills copiables entre hôtes : `SKILL.md`, scripts/assets optionnels, dépendances déclarées (outils/MCP/binaires).

| Marqueur | Projet | En une phrase | Lien |
|---|---|---|---|
| ⭐ | **vercel-labs/agent-skills** | Packs portables officiels Vercel (pratiques React/Next, déploiement, etc.) ; cible majeure de `npx skills` | https://github.com/vercel-labs/agent-skills |
| ⭐ | **obra/superpowers** | Skills agentiques installables + méthodologie de livraison logicielle ; fort signal d’adoption | https://github.com/obra/superpowers |
| ☄️ | **addyosmani/agent-skills** | Packs d’ingénierie production pour agents de code | https://github.com/addyosmani/agent-skills |

**Seuil :** Manifeste de skill identifiable (`SKILL.md` ou équivalent documenté) + étapes de chargement reproductibles. Les purs « prompts.md » sont rejetés.

---

## Method · Marketplaces

Découverte, installation, versions et notes (si disponibles). Ce dépôt **croise en pair** — pas de miroir de catalogues entiers.

| Marqueur | Projet | En une phrase | Lien |
|---|---|---|---|
| ⭐ | **VoltAgent/awesome-agent-skills** | Awesome Agent Skills communautaire de référence (multi-hôtes, nombreuses entrées) — **liste paire**, liens croisés sélectifs | https://github.com/VoltAgent/awesome-agent-skills |
| ⭐ | **skills.sh** | UI de découverte / classement d’installation pour `npx skills` | https://www.skills.sh |

---

## Method · Authoring Tools

Générer `SKILL.md` depuis une description de tâche, linter permissions/chemins, tester le chargement correct.

| Marqueur | Projet | En une phrase | Lien |
|---|---|---|---|
| ☄️ | **NVIDIA/SkillSpector** | Scanner pré-install des agent skills (injection, exfiltration, risque supply-chain) | https://github.com/NVIDIA/SkillSpector |

> D’autres authoring / optimizers (SkillOpt, SkillCorpus, etc.) dans des vagues ultérieures ; l’acceptation niveau skill croise `awesome-agent-eval`.

---

## Method · Loaders & Composition

Comment les hôtes découvrent les skills, hot-load, sandboxes de permissions, orchestration multi-skills (toujours Skills — pas un dépôt Orchestrator générique).

| Marqueur | Projet | En une phrase | Lien |
|---|---|---|---|
| ⭐ | **vercel-labs/skills** | **`npx skills`** — CLI d’installation ouverte multi-agents ; associé à skills.sh | https://github.com/vercel-labs/skills |
| ⭐ | **Vercel agent-skills docs** | Cookbook d’installation hôte + packs | https://vercel.com/docs/agent-resources/skills |
| ⭐ | **Découverte Cursor / Claude skills** | Répertoires de découverte et conventions de chargement in-product (voir lignes Spec) | https://cursor.com/docs/skills · https://claude.com/docs/skills/how-to |

---

## Domain · Coding / Research / Office / Ops

### Coding

| Marqueur | Pack de skills | En une phrase | Lien |
|---|---|---|---|
| ☄️ | **Leonxlnx/taste-skill** | Skills de goût design / direction artistique (incl. contrôles navigateur) | https://github.com/Leonxlnx/taste-skill |
| ☄️ | **tt-a1i/archify** | Skill agent qui génère des diagrammes d’architecture depuis idées ou codebases | https://github.com/tt-a1i/archify |

> Les packs portables orientés ingénierie figurent aussi sous [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) et [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) (Portable Packs).

### Research / Science

| Marqueur | Pack de skills | En une phrase | Lien |
|---|---|---|---|
| ⭐ | **K-Dense-AI/scientific-agent-skills** | Grande bibliothèque de skills scientifiques ; revendique la compatibilité Agent Skills | https://github.com/K-Dense-AI/scientific-agent-skills |
| ☄️ | **mvanhorn/last30days-skill** | Skill de recherche d’infos récentes sur Reddit/X/YT/HN/Web | https://github.com/mvanhorn/last30days-skill |

### Office / Docs

| Marqueur | Pack de skills | En une phrase | Lien |
|---|---|---|---|
| ☄️ | **kepano/obsidian-skills** | Obsidian CLI + skills formats ouverts (Markdown / Bases / Canvas) | https://github.com/kepano/obsidian-skills |
| ⭐ | **anthropics/skills (exemples bureautique)** | Exemples officiels de l’arbre de référence : docx / pdf / pptx / xlsx, etc. | https://github.com/anthropics/skills |

### Ops / Data

| Marqueur | Pack de skills | En une phrase | Lien |
|---|---|---|---|
| ☄️ | **cloudflare/security-audit-skill** | Skill d’audit sécurité multi-étapes avec findings machine-lisibles | https://github.com/cloudflare/security-audit-skill |
| ☄️ | **yoruuuchan/chatgpt-mcp-connect** | Recettes reproductibles pour connecter des serveurs MCP locaux/hébergés à ChatGPT (Streamable HTTP, ponts stdio, OAuth 2.1, Cloudflare, Tailscale Funnel) | https://github.com/yoruuuchan/chatgpt-mcp-connect |

---

## Contrast · vs MCP / Prompts / Plugins

| Facile à confondre | Différence | Envoyer vers |
|---|---|---|
| Listes de serveurs MCP | Endpoints de protocole & schémas d’outils, pas des manuels de skill | `awesome-agent-mcp` |
| Prompt library | Pas de contrat de chargement, pas de modèle ressource/permission | Rejeté |
| Marchés de plugins IDE | Étendent l’UI/API hôte ; pas forcément un Agent Skill | Seulement s’ils livrent aussi un pack `SKILL.md` |
| Frameworks Memory | Stockent l’état ; ne définissent pas « ce que je sais faire » | `awesome-agent-mem` |
| Orchestration multi-agents | Orchestrator ; les skills ne sont que des unités appelables | Pas dans les 8 dépôts de lancement |

---

## Related Awesome & liens croisés

| Dépôt thème (prévu) | Relation |
|---|---|
| `awesome-agent-mcp` | Serveurs MCP souvent déclarés en deps des Skills |
| `awesome-agent-mem` | Backends mémoire que les Skills peuvent lire/écrire |
| `awesome-agent-cli` | Runners terminal qui chargent des skills |
| `awesome-agent-sandbox` | Isolation d’exécution des scripts de skill |
| `awesome-agent-eval` | Acceptation niveau skill & eval de trajectoires |
| `awesome-agent-rsi` | Boucles d’auto-amélioration qui produisent/révisent des skills |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | Liste communautaire paire (pas de miroir) |

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — contenu de la liste librement réutilisable.

## Disclaimer

Cette liste **n’est pas affiliée** à Anthropic, Cursor, OpenAI, Vercel, NVIDIA ni à d’autres éditeurs/projets ; l’inclusion et ⭐/☄️ **ne constituent pas une endorsement**. Les entrées doivent respecter un contrat de skill chargeable (`SKILL.md` ou équivalent) ; le nombre d’étoiles seul n’est pas une clé de classement.

## Maintainers

- ThinkFlowLab / hs (Awesome de lancement)

**Last updated:** 2026-10-26 (Asia/Shanghai) · multilingual READMEs (zh / en / ja / ko / fr / es)
