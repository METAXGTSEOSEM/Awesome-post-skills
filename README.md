<p align="center">
  <img src="https://img.shields.io/badge/Codex-6C47FF?style=flat-square&logo=openai&logoColor=white" alt="Codex" />
  <img src="https://img.shields.io/badge/Copilot-181717?style=flat-square&logo=github&logoColor=white" alt="Copilot" />
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Cursor-000000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor" />
  <img src="https://img.shields.io/badge/Windsurf-0EA5E9?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiByeD0iNCIgZmlsbD0iIzBFQTVFOSIvPjwvc3ZnPg==&logoColor=white" alt="Windsurf" />
  <img src="https://img.shields.io/badge/Aider-FF6B35?style=flat-square&logoColor=white" alt="Aider" />
  <img src="https://img.shields.io/badge/Cline-FF6B6B?style=flat-square&logo=visualstudio&logoColor=white" alt="Cline" />
</p>

<pre align="center">
╔══════════════════════════════════════════════════════════╗
║                                                          ║
║   █████╗ ██╗    ██╗███████╗███████╗ ██████╗ ███╗   ███╗███████╗
║  ██╔══██╗██║    ██║██╔════╝██╔════╝██╔═══██╗████╗ ████║██╔════╝
║  ███████║██║ █╗ ██║█████╗  ███████╗██║   ██║██╔████╔██║█████╗
║  ██╔══██║██║███╗██║██╔══╝  ╚════██║██║   ██║██║╚██╔╝██║██╔══╝
║  ██║  ██║╚███╔███╔╝███████╗███████║╚██████╔╝██║ ╚═╝ ██║███████╗
║  ╚═╝  ╚═╝ ╚══╝╚══╝ ╚══════╝╚══════╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝
║                                                          ║
║           ██████╗  ██████╗ ███████╗████████╗             ║
║           ██╔══██╗██╔═══██╗██╔════╝╚══██╔══╝             ║
║           ██████╔╝██║   ██║███████╗   ██║                ║
║           ██╔═══╝ ██║   ██║╚════██║   ██║                ║
║           ██║     ╚██████╔╝███████║   ██║                ║
║           ╚═╝      ╚═════╝ ╚══════╝   ╚═╝                ║
║                                                          ║
║              ███████╗██╗  ██╗██╗██╗     ██╗             ║
║              ██╔════╝██║ ██╔╝██║██║     ██║             ║
║              ███████╗█████╔╝ ██║██║     ██║             ║
║              ╚════██║██╔═██╗ ██║██║     ██║             ║
║              ███████║██║  ██╗██║███████╗███████╗        ║
║              ╚══════╝╚═╝  ╚═╝╚═╝╚══════╝╚══════╝        ║
║                                                          ║
╚══════════════════════════════════════════════════════════╝
</pre>

<p align="center">
  <strong>Production-grade AI agent skills for content marketing, SEO, and growth.</strong><br />
  <sub>Plain Markdown. No lock-in. Works with any agent that reads instructions.</sub>
</p>

<p align="center">
  <a href="#-what-is-this">About</a> ·
  <a href="#-skills">Skills</a> ·
  <a href="#-compatibility">Compatibility</a> ·
  <a href="#-quick-start">Quick Start</a> ·
  <a href="#-roadmap">Roadmap</a> ·
  <a href="#-faq">FAQ</a> ·
  <a href="#-contributing">Contributing</a>
</p>

---

## 🧠 What Is This?

A curated collection of **agent skills** — modular instruction packs that turn AI coding agents into specialized content production machines.

> **SOP-as-Code.** Your content playbooks, executable by machines.

No SDKs. No vendor lock-in. Just `.md` files with YAML metadata. Copy them. Fork them. Paste them anywhere.

---

## 🧰 Skills

| # | Skill | What It Does | →
|---|---|---|---|
| 1 | `b2b-seo-content-writer` | 12-step B2B SEO article pipeline · EEAT · GEO · Schema · 8 cluster types | [📂](./skills/b2b-seo-content-writer/) |

### `b2b-seo-content-writer`

```
Step 1   Cluster Title Research (8 cluster types)
Step 2   Competitor Outline → Own Outline
Step 3   SEMrush Keyword Mining
Step 4   GPT EEAT Material (factory/project POV)
Step 5   Internal Link Plan + External Sources
Step 6   Submit Outline to AI
Step 7   Keyword Placement + EEAT Markers
Step 8   GEO Article (≥2500 words, ≥3 summary types)
Step 9   WordPress Preview QA (9-point checklist)
Step 10  Images + Links (6-image plan)
Step 11  Schema Markup (Article / FAQPage / HowTo / ImageObject)
Step 12  Keyword Record Archive (CSV)
```

Delivers: publish-ready article + 4× schema JSON-LD + keyword CSV + link plan.

---

## 🔌 Compatibility

| Agent | How to Use |
|---|---|
| **Codex** | `$b2b-seo-content-writer` or auto-detect |
| **Claude Code** | Paste into `CLAUDE.md` |
| **Copilot** | Paste into `.github/copilot-instructions.md` |
| **Cursor** | Paste into `.cursor/rules/` |
| **Windsurf** | Paste into `.windsurfrules` |
| **Aider** | `aider --read SKILL.md` |
| **Cline** | Paste into `.clinerules` |

> If the agent can read a Markdown file, it can use these skills. No special syntax required.

---

## ⚡ Quick Start

```bash
git clone https://github.com/METAXGTSEOSEM/Awesome-post-skills.git
```

**Codex native:**
```
$skill-installer install METAXGTSEOSEM/Awesome-post-skills --skill b2b-seo-content-writer
```

**Any other agent:**
```
Copy skills/b2b-seo-content-writer/SKILL.md → your agent's instructions file.
Done.
```

---

## 🗺️ Roadmap

| Skill | Category | Status |
|---|---|---|
| `wp-seo-auditor` | SEO Audit | 🔜 |
| `geo-content-optimizer` | GEO / AI Search | 🔜 |
| `keyword-cluster-planner` | Keyword Research | 🔜 |
| `linkedin-b2b-post-writer` | Social / B2B | 🔜 |
| `google-ads-copy-generator` | PPC / Ads | 🔜 |
| `schema-markup-factory` | Technical SEO | 🔜 |
| `product-page-rewriter` | CRO / Copy | 🔜 |
| `email-drip-campaign-builder` | Email | 💡 |
| `landing-page-ab-test-designer` | CRO | 💡 |
| `competitor-content-gap-analyzer` | Competitive Intel | 💡 |

---

## ❓ FAQ

**Do I need Codex?**
No. These are plain `.md` files. Paste into any agent's instruction file and go.

**How is this different from prompts?**
Prompts are one-shot. Skills are full SOPs — multi-step decision trees with checkpoints and multiple deliverables.

**Can I mix skills?**
Yes, if your agent has enough context window. 2-3 skills at once is fine with 200K+ tokens.

**Can I contribute?**
Absolutely. See below.

---

## 🤝 Contributing

```
skills/<name>/
├── SKILL.md          # Required: YAML frontmatter + markdown workflow
├── agents/
│   └── openai.yaml   # Optional: Codex UI metadata
└── assets/           # Optional: templates, CSVs
```

1. Fork → 2. Add `skills/<name>/SKILL.md` → 3. PR

**Rules:**
- **Keep it concise.** Agents are already smart. Only add context they lack.
- **Imperative form.** "Do X", not "You should do X."
- **Platform-agnostic.** Instructions must work when pasted into any agent.
- **One deliverable per step.** Don't bundle research + writing + QA into one mega-step.

---

## 📄 License

MIT · [METAXGTSEOSEM](https://github.com/METAXGTSEOSEM)