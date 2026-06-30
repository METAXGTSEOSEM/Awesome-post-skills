<p align="center">
  <img src="https://img.shields.io/badge/Codex-Skills-2563EB?style=for-the-badge&logo=openai&logoColor=white" alt="Codex Skills" />
  <img src="https://img.shields.io/badge/B2B%20SEO-Content%20Writer-059669?style=for-the-badge" alt="B2B SEO" />
  <img src="https://img.shields.io/badge/EEAT%20%2B%20GEO-Optimized-7C3AED?style=for-the-badge" alt="EEAT + GEO" />
</p>

<h1 align="center">🚀 Awesome Post Skills</h1>
<p align="center"><strong>Production-grade Codex agent skills for content marketing, SEO, and beyond.</strong></p>

<p align="center">
  <a href="#-available-skills"><strong>Skills</strong></a> ·
  <a href="#-quick-start"><strong>Quick Start</strong></a> ·
  <a href="#-skill-collection"><strong>Collection</strong></a> ·
  <a href="#-roadmap"><strong>Roadmap</strong></a> ·
  <a href="#-contributing"><strong>Contributing</strong></a>
</p>

---

## 🧠 What Is This?

A curated collection of **[Codex](https://github.com/openai/codex)** agent skills — modular, self-contained instruction packs that transform the general-purpose Codex agent into a specialized content production machine.

Each skill is a folder containing a `SKILL.md` (the agent's operating manual) plus optional templates, scripts, and reference assets. Drop them into Codex and it instantly knows how to execute complex, multi-step workflows.

> **Think of it as:** SOP-as-Code. Your content playbooks, machine-readable.

---

## 🎯 Available Skills

| # | Skill | Description | Highlights |
|---|---|---|---|
| 1 | [`b2b-seo-content-writer`](./skills/b2b-seo-content-writer/) | End-to-end B2B SEO article production | 12-step SOP · 8 cluster types · EEAT · GEO · Schema |

---

### 🔍 `b2b-seo-content-writer` — Deep Dive

```text
$b2b-seo-content-writer
```

The flagship skill. Follows a battle-tested 12-step production pipeline:

```
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
Step 10  Images + External Links + Internal Links
Step 11  Schema Markup (Article / FAQPage / HowTo / ImageObject)
Step 12  Keyword Record Archive (CSV tracking)
```

**What you get at the end:** A publish-ready article with SEO-optimized structure, EEAT trust signals, GEO-friendly summaries, schema markup JSON, a keyword tracking record, and a full internal/external link plan.

---

## ⚡ Quick Start

### Prerequisites
- [Codex CLI](https://github.com/openai/codex) or Codex Desktop installed
- Codex configured with your API key

### Install a skill

```bash
# Via the skill-installer (recommended)
$skill-installer install METAXGTSEOSEM/Awesome-post-skills --skill b2b-seo-content-writer

# Or clone the repo and point Codex to it
git clone https://github.com/METAXGTSEOSEM/Awesome-post-skills.git
```

### Use a skill

Just invoke the skill name in your Codex conversation:

```
$b2b-seo-content-writer
```

Or describe what you need naturally — Codex auto-detects matching skills:

> *"Write a heavy-duty scissor lift buying guide for my B2B warehouse audience, with EEAT and schema markup."*

---

## 📦 Skill Collection

| Skill | Status | Category | Dependencies |
|---|---|---|---|
| `b2b-seo-content-writer` | ✅ Stable | Content Production | — |
| *More coming soon* | 🔜 Planned | — | — |

---

## 🗺️ Roadmap

Planned skills for this collection:

- [ ] **`wp-seo-auditor`** — Automated WordPress SEO audit with actionable fix list
- [ ] **`geo-content-optimizer`** — Generative Engine Optimization for AI-powered search (ChatGPT, Perplexity, Gemini)
- [ ] **`keyword-cluster-planner`** — Build topic clusters and content calendars from SEMrush/Ahrefs data
- [ ] **`linkedin-b2b-post-writer`** — B2B LinkedIn content with hook frameworks and engagement patterns
- [ ] **`google-ads-copy-generator`** — RSA headlines, descriptions, and extensions with A/B variant logic
- [ ] **`schema-markup-factory`** — Generate complete JSON-LD schema packages for any page type
- [ ] **`product-page-rewriter`** — B2B product page copy optimization with UX writing principles

> Have an idea? [Open an issue](https://github.com/METAXGTSEOSEM/Awesome-post-skills/issues/new) or submit a PR.

---

## 🤝 Contributing

### Skill Structure

Every skill lives under `skills/<skill-name>/` and follows this layout:

```
skills/<skill-name>/
├── SKILL.md              # Required: YAML frontmatter + markdown instructions
├── agents/
│   └── openai.yaml       # UI metadata (display name, color, prompt)
└── assets/               # Optional: templates, CSVs, reference docs
    ├── template-1.md
    ├── template-2.md
    └── data-template.csv
```

### Adding a New Skill

1. Fork this repo
2. Create `skills/<your-skill>/SKILL.md` with YAML frontmatter:
   ```yaml
   ---
   name: your-skill-name
   description: What it does and when Codex should use it. Be specific.
   ---
   ```
3. Add `agents/openai.yaml` for UI metadata
4. Add any template/asset files in `assets/`
5. Validate: `python quick_validate.py skills/<your-skill>/`
6. Open a PR 🎉

### Guidelines
- **Concise is key** — Codex is already smart. Only add context it doesn't have.
- **Imperative form** — Write SKILL.md in imperative/infinitive style. "Do X", not "You should do X".
- **Test your skill** — Run through a real task end-to-end before submitting.

---

## 📄 License

MIT © [METAXGTSEOSEM](https://github.com/METAXGTSEOSEM)

---

<p align="center">
  <sub>Built with ❤️ for content marketers who ship.</sub>
</p>