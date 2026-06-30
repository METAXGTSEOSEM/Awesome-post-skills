<p align="center">
<img src="https://img.shields.io/badge/B2B%20SEO-Content%20Writer-059669?style=for-the-badge" alt="B2B SEO" />
  <img src="https://img.shields.io/badge/EEAT%20%2B%20GEO-Optimized-7C3AED?style=for-the-badge" alt="EEAT + GEO" />
  <img src="https://img.shields.io/badge/Codex-6C47FF?style=for-the-badge&logo=openai&logoColor=white" alt="Codex" />
  <img src="https://img.shields.io/badge/Copilot-000000?style=for-the-badge&logo=githubcopilot&logoColor=white" alt="Copilot" />
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white" alt="Cursor" />
  <img src="https://img.shields.io/badge/Windsurf-0EA5E9?style=for-the-badge&logo=codeium&logoColor=white" alt="Windsurf" />
  <img src="https://img.shields.io/badge/Aider-FF6B35?style=for-the-badge&logo=python&logoColor=white" alt="Aider" />
  <img src="https://img.shields.io/badge/Cline-E34F26?style=for-the-badge&logo=visualstudiocode&logoColor=white" alt="Cline" />`n  <img src="https://img.shields.io/badge/CC_Switch-FF5722?style=for-the-badge&logo=robot&logoColor=white&labelColor=1A1A2E" alt="CC-Switch" />
</p>

<h1 align="center">🚀 Awesome Post Skills</h1>
<p align="center">
  <strong>Production-grade AI agent skills for content marketing, SEO, and growth.</strong><br />
  <sub>Works with any agent that supports markdown-based instruction files — not just Codex.</sub>
</p>

<p align="center">
  <a href="#-what-is-this"><strong>About</strong></a> ·
  <a href="#-available-skills"><strong>Skills</strong></a> ·
  <a href="#-platform-compatibility"><strong>Compatibility</strong></a> ·
  <a href="#-quick-start"><strong>Quick Start</strong></a> ·
  <a href="#-skill-collection"><strong>Collection</strong></a> ·
  <a href="#-roadmap"><strong>Roadmap</strong></a> ·
  <a href="#-faq"><strong>FAQ</strong></a> ·
  <a href="#-contributing"><strong>Contributing</strong></a>
</p>

---

## 🧠 What Is This?

A curated collection of **agent skills** — modular, self-contained instruction packs that transform any capable AI coding agent into a specialized content production machine.

Each skill is a plain Markdown folder. No SDKs. No lock-in. Just `.md` files, YAML metadata, and optional templates. Drop them into your agent of choice and it instantly knows how to execute complex, multi-step workflows.

### 💡 The Philosophy

Every great content team has SOPs — Standard Operating Procedures. Style guides. Checklists. Templates. This repo turns those playbooks into **machine-readable instructions** that AI agents can follow with surgical precision.

> **SOP-as-Code.** Your content playbooks, executable.

### 🤖 Supported Agents

These skills follow a universal pattern — YAML frontmatter + Markdown body. They work with any agent platform that supports file-based instruction injection:

| Agent | How to Use | Notes |
|---|---|---|
| **[Codex](https://github.com/openai/codex)** | `$skill-name` or auto-detect | Native `$skill` syntax; full `SKILL.md` + `openai.yaml` support |
| **[GitHub Copilot](https://github.com/features/copilot)** | `.github/copilot-instructions.md` | Copy `SKILL.md` content into instructions file |
| **[Claude Code](https://docs.anthropic.com/en/docs/claude-code)** | `CLAUDE.md` or `/instructions` | Paste into project-level or user-level CLAUDE.md |
| **[Cursor](https://cursor.com/)** | `.cursor/rules/` or `.cursorrules` | Drop `SKILL.md` content into a rule file with glob pattern |
| **[Windsurf](https://codeium.com/windsurf)** | `.windsurfrules` | Same approach — paste skill instructions |
| **[Aider](https://aider.chat/)** | `--read` flag or `.aider.conf.yml` | Point to `SKILL.md` via config |
| **[Cline](https://github.com/cline/cline)** (VS Code) | `.clinerules` | Paste skill content; supports project & user-level |
| **CC-Switch** | Custom instructions panel | Paste into system prompt / custom instructions — works with all models, model-agnostic |
| **[Amazon Q Developer](https://aws.amazon.com/q/developer/)** | `.amazonq/rules/` | Custom instructions via rules directory |
| **Any MCP-compatible agent** | Load as resource | Treat `SKILL.md` as an MCP resource |

> 💡 **Universal principle**: If your agent can read a Markdown file and follow instructions within it, it can use these skills. The `SKILL.md` file is the single source of truth — copy it, reference it, or symlink it.

---

## 🎯 Available Skills

| # | Skill | Category | Description |
|---|---|---|---|
| 1 | [`b2b-seo-content-writer`](./skills/b2b-seo-content-writer/) | Content Production | 12-step B2B SEO article pipeline with EEAT, GEO & Schema |

---

### 🔍 `b2b-seo-content-writer` — Deep Dive

A battle-tested 12-step production pipeline for B2B articles that rank and convert:

```text
Step 1   Cluster Title Research
   ↓     (8 cluster types: Educational · Buying Guide · Comparison ·
   ↓      Specifications · Application Scenarios · Process/Quality ·
   ↓      Certification/Compliance · Procurement/Supplier)
Step 2   Competitor Outline → Own Outline
Step 3   SEMrush Keyword Mining
Step 4   GPT EEAT Material (factory/project perspective)
Step 5   Internal Link Plan + External Reference Sources
Step 6   Submit Outline to AI
Step 7   Keyword Placement + EEAT Markup Instructions
Step 8   GEO Article Generation (≥2500 words, ≥3 summary types)
Step 9   WordPress Preview QA (9-point checklist)
Step 10  Images + External Links + Internal Links (6-image plan)
Step 11  Schema Markup (Article / FAQPage / HowTo / ImageObject)
Step 12  Keyword Record Archive (CSV tracking)
```

**What you get:** A publish-ready article with SEO structure, EEAT trust signals, GEO-friendly summaries, 4× schema JSON-LD blocks, a keyword tracking record, and a full internal/external link plan. See the [skill README](./skills/b2b-seo-content-writer/) for details.

---

## 📋 Platform Compatibility

All skills use the standard **YAML frontmatter + Markdown body** format. Here's how to adapt for different agents:

### Codex (Native)
```bash
# Install via skill-installer
$skill-installer install METAXGTSEOSEM/Awesome-post-skills --skill b2b-seo-content-writer

# Or invoke directly
$b2b-seo-content-writer
```

### Claude Code / Cursor / Windsurf / Copilot
Just copy the `SKILL.md` content. The agent reads it as custom instructions:
```bash
# Example: add to Claude Code
cat skills/b2b-seo-content-writer/SKILL.md >> CLAUDE.md
```

### Aider
```bash
aider --read skills/b2b-seo-content-writer/SKILL.md
```

### Any Agent (Universal)
```
1. Open skills/b2b-seo-content-writer/SKILL.md
2. Copy the entire file
3. Paste into your agent's custom instructions / system prompt / rules file
4. Done.
```

---

## ⚡ Quick Start

### Prerequisites
- Any AI coding agent (Codex, Copilot, Claude Code, Cursor, Windsurf, Aider, Cline, etc.)
- For Codex specifically: [Codex CLI](https://github.com/openai/codex) or Codex Desktop

### Option A: Codex (Recommended for full experience)

```bash
# Install via skill-installer
$skill-installer install METAXGTSEOSEM/Awesome-post-skills --skill b2b-seo-content-writer

# Or clone the full repo
git clone https://github.com/METAXGTSEOSEM/Awesome-post-skills.git
```

### Option B: Any Agent (Universal)

```bash
# Clone the repo
git clone https://github.com/METAXGTSEOSEM/Awesome-post-skills.git

# Copy the skill you need into your agent's instructions
cat Awesome-post-skills/skills/b2b-seo-content-writer/SKILL.md >> ~/your-agent-instructions.md
```

### Usage

```
$b2b-seo-content-writer
```

> *"Write a heavy-duty scissor lift buying guide for my B2B warehouse audience, with EEAT and schema markup."*

The agent will walk you through the 12-step pipeline — collecting prerequisites, researching titles, analyzing competitors, mining keywords, generating EEAT content, and producing the final article with all metadata.

---

## 📦 Skill Collection

| Skill | Status | Category | Key Deliverables |
|---|---|---|---|
| `b2b-seo-content-writer` | ✅ Stable | Content Production | Article, Schema JSON, Keyword CSV, Link Plan |
| *More coming soon* | 🔜 Planned | — | — |

---

## 🗺️ Roadmap

| # | Skill | Category | Status |
|---|---|---|---|
| 1 | `wp-seo-auditor` | SEO Audit | 🔜 Planned |
| 2 | `geo-content-optimizer` | GEO / AI Search | 🔜 Planned |
| 3 | `keyword-cluster-planner` | Keyword Research | 🔜 Planned |
| 4 | `linkedin-b2b-post-writer` | Social / B2B | 🔜 Planned |
| 5 | `google-ads-copy-generator` | PPC / Advertising | 🔜 Planned |
| 6 | `schema-markup-factory` | Technical SEO | 🔜 Planned |
| 7 | `product-page-rewriter` | Conversion / CRO | 🔜 Planned |
| 8 | `email-drip-campaign-builder` | Email Marketing | 💡 Idea |
| 9 | `landing-page-ab-test-designer` | CRO / Testing | 💡 Idea |
| 10 | `competitor-content-gap-analyzer` | Competitive Intel | 💡 Idea |

> Have an idea? [Open an issue](https://github.com/METAXGTSEOSEM/Awesome-post-skills/issues/new) or submit a PR.

---

## ❓ FAQ

### Do I need Codex to use these skills?
No. The skills are plain Markdown files with YAML metadata. Any AI coding agent that supports custom instructions, rules files, or system prompt injection can use them. See the [Platform Compatibility](#-platform-compatibility) table above.

### What if my agent doesn't support `$skill-name` syntax?
Just paste the `SKILL.md` content into your agent's instructions file (`.cursorrules`, `CLAUDE.md`, `.clinerules`, etc.). The workflow instructions work the same way — the `$` syntax is just a Codex-native shortcut.

### Can I mix skills?
Yes. Each skill is self-contained and handles one domain. You can load multiple skills at once, though be mindful of context window limits. For agents with large contexts (200K+ tokens), loading 2-3 skills is perfectly fine.

### How is this different from prompts or templates?
Prompts are one-shot. Templates are fill-in-the-blank. Skills are **complete operating procedures** — they guide the agent through multi-step decision trees, enforce quality checkpoints, and produce multiple interdependent deliverables in sequence.

### Can I contribute my own skill?
Absolutely. See [Contributing](#-contributing) below. The format is deliberately simple: one folder, one `SKILL.md`, optional assets. No build step. No framework.

---

## 🤝 Contributing

### Skill Structure

```
skills/<skill-name>/
├── SKILL.md              # Required: YAML frontmatter + markdown workflow
├── agents/
│   └── openai.yaml       # UI metadata (Codex-specific; optional for other agents)
├── assets/               # Templates, CSVs, reference docs (optional)
│   ├── template-1.md
│   └── data-template.csv
├── scripts/              # Executable helpers (optional)
└── references/           # Domain knowledge docs (optional)
```

### Adding a New Skill

1. Fork this repo
2. Create `skills/<your-skill>/SKILL.md` with YAML frontmatter:
   ```yaml
   ---
   name: your-skill-name
   description: What it does and when agents should use it. Include trigger keywords.
   ---
   ```
3. Add `agents/openai.yaml` for Codex UI metadata (optional but recommended)
4. Add templates, CSVs, or reference files in `assets/`
5. Add a row to the [Skill Collection](#-skill-collection) table in this README
6. Validate: `python quick_validate.py skills/<your-skill>/` (if using skill-creator tools)
7. Open a PR 🎉

### Guidelines
- **Concise is key** — Agents are already smart. Only add context they don't already have.
- **Imperative form** — "Do X", not "You should do X". Instructions are commands.
- **Platform-agnostic** — Avoid agent-specific syntax in `SKILL.md`. The instructions should work when copied into any agent's custom rules.
- **Chunk your steps** — Each step should produce a discrete deliverable. Avoid mega-steps that mix research, writing, and QA.
- **Test before PR** — Run through a real task end-to-end with at least one agent platform.

---

## ⭐ Star History

If this repo helps you, give it a star! It helps others discover it.

[![Star History Chart](https://api.star-history.com/svg?repos=METAXGTSEOSEM/Awesome-post-skills&type=Date)](https://star-history.com/#METAXGTSEOSEM/Awesome-post-skills&Date)

---

## 📄 License

MIT © [METAXGTSEOSEM](https://github.com/METAXGTSEOSEM)

---

<p align="center">
  <sub>Built for anyone who writes content that ranks. AI is the assistant — you're the editor.</sub>
</p>