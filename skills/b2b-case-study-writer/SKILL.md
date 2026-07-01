---
name: b2b-case-study-writer
description: Generate B2B industrial case study/project reference pages optimized for Google rankings, GEO, EEAT, and RankMath SEO score (90+/100). Produces case study title (3 variants), meta description, project snapshot table, client background, challenge analysis, Gradin solution, MD-formatted spec table, image placement plan, and schema markup. Use when user needs to write a B2B case study, create a project reference page, or document a customer installation for SEO.
---

# B2B Case Study Writer

Generate B2B industrial case study pages optimized for Google ranking, GEO, EEAT, and RankMath score 90+/100.

## What This Skill Generates (Variable Blocks)

Only generate these blocks. Fixed template blocks — general FAQ (7 questions), related products, inquiry CTA, certification wall, customer logo wall — already exist in the user's template and must NOT be generated.

| # | Block | Format |
|---|---|---|
| 1 | SEO Metadata | Keyword plan + Title variants + URL + Meta Description + Image Alt |
| 2 | Project Snapshot | MD table |
| 3 | Client Background | 1 paragraph |
| 4 | Challenge | 3-4 specific pain points |
| 5 | Gradin Solution | 2-3 paragraphs with engineering detail |
| 6 | Technical Spec Table | MD table |
| 7 | Image Plan | File names, Alt text, placement |
| 8 | Schema Markup | JSON-LD |

---

## Output Format & Rules

### Block-Level Bilingual Output

- **English block first**, then Chinese translation immediately below. Never interleave sentences — complete English paragraph(s) → complete Chinese paragraph(s).
- Schematic: `[English content block]` → blank line → `[Chinese translation block]` → blank line → next English block.

### Strict Half-Width Punctuation

- **100% English half-width punctuation everywhere** — including Chinese translations, tables, lists, and parenthetical text.
- ✅ Allowed: `.` `,` `:` `;` `?` `!` `-` `—` `(` `)` `[` `]` `"` `"`
- ❌ Banned: `,` `.` `:` `;` `"` `"` `'` `'` `(` `)` `[` `]`
- This rule is absolute. There are no exceptions, even in the Chinese translation sections.

### No AI Transitional Fluff

- ❌ Banned words and patterns: "furthermore", "moreover", "in addition", "additionally", "besides", "in conclusion", "to summarize", "in summary", "overall", "all in all"
- ✅ Replace with: direct cause-and-effect engineering logic. One idea follows the previous one because of physics, process, or data — not because of a transition word.

### Case Study Standard Structure

Content must follow this fixed section order:

| Section # | Section Name | Description |
|---|---|---|
| 1 | SEO Block | Keywords, Title, URL, Meta Description, Image Alt plan |
| 2 | Case Title | H1 headline |
| 3 | Project Overview | Project snapshot table + 1-paragraph summary |
| 4 | Challenge | Physical space & technical constraints (3-4 specific pain points) |
| 5 | Solution | Custom design solution (2-3 paragraphs, engineering detail) |
| 6 | Technical Specifications | Full MD table with parameters, values, units |
| 7 | Project Gallery | Image placeholder guide — describe what real engineering photos should be inserted (user uploads later) |

### Segmented Output Control

- **Output only the section currently requested.** Never generate the entire case study in one response.
- After each section, pause and wait for the user's next instruction (e.g., "Section 2" or "Next: Challenge").
- This prevents model attention decay and character truncation.

### Link Directory (End of Article)

At the very end of the complete case study, output a bilingual link directory table summarizing every internal and external link used:

| Anchor Text (EN) | Anchor Text (中文) | URL | Type |
|---|---|---|---|
| [English anchor] | [Chinese anchor] | [URL] | Internal / External |

### Live Link Verification

- **External links**: You must search live / fetch the official standards body website (e.g., asme.org, iso.org, bsigroup.com) to find the actual canonical URL. Never fabricate a link, a virtual page, or a 404-prone URL. Return only the real, active, permanent canonical URL.
- **Format**: `[Natural English anchor text] = Real official URL`
- **Internal links**: Ask the user for their website URL structure and competitor URLs. If the user provides them, inspect the pages to generate correct internal links with proper anchor text. If not provided, skip internal links — never guess.

---
## Core Writing Principles

### 1. Target Audience

Write for three personas simultaneously:
- **Procurement Manager**: Needs to know industry match, timeline, and whether Gradin can deliver
- **Engineer**: Needs technical detail — specs, materials, safety, how it works
- **Business Owner**: Needs business impact — why this investment made sense

All three must find their answer on the page without scrolling past irrelevant content.

### 2. Output Language Rule

- **All interactions with the user**: Chinese
- **All generated content (deliverables)**: English first, immediately followed by Chinese translation
- **Image file names and Alt text**: English only
- **Schema markup**: English only

### 3. No AI-Sounding Content, No Exaggerated Claims

- No AI cliché openings or overly polished transitions
- No vague superlatives ("industry-leading", "state-of-the-art")
- No fake urgency ("Don't miss out!")
- No fabricated numbers or client names — use `[placeholder]` when real data is unavailable
- Under-promise, over-deliver. Write like an engineer explaining work to a peer.

### 4. International Website Standards

- English punctuation only — even in Chinese translations (`.` `,` `:` `;` — never `，` `。` `：`)
- Metric units with imperial in parentheses: "5000 kg (11,023 lbs)"
- ISO date format: YYYY-MM-DD
- No region-specific assumptions unless the case is explicitly in that region

---

## Workflow

### Step 1: Collect Case Information

Collect from the user. If any field is missing, ask before proceeding:

- **Client name** (or anonymous descriptor: "a European automotive parts manufacturer")
- **Client industry** and **location** (country/region)
- **Product model and name** supplied by Gradin
- **Key technical specifications** (capacity, dimensions, power, materials, etc.)
- **The problem** the client faced before Gradin (3-4 specific pain points)
- **How Gradin solved it** (product configuration, engineering decisions, customizations)
- **Project timeline** (year completed)
- **Available images** (how many, what they show)
- **Competitor case study URLs** (3-5 for analysis)

### Step 2: SEO Keyword Research & Placement Plan

#### Primary Keyword (1)

Derived from: product type + case study intent.
Pattern: `[Product Type] case study` / `[Product Type] for [Industry]` / `[Industry] [Product Type] project`

#### Secondary Keywords (6-10)

Based on Google top results, industry terminology, applications, specifications, and buyer intent:

| Source | Example Keywords |
|---|---|
| Industry terms | "pressure vessel upender", "pipe tilter Dammam" |
| Application | "hydraulic tilting solution for steel fabrication" |
| Specification | "20-ton pipe upender", "90-degree hydraulic tilter" |
| Buyer intent | "custom upender manufacturer", "industrial tilting equipment supplier" |
| GEO / semantic | "safe pipe handling", "overhead crane alternative", "workpiece rotation solution" |

#### RankMath SEO Placement Map

| Placement | Keyword | Rule |
|---|---|---|
| **SEO Title** | Primary at front | ≤ 60 characters |
| **URL slug** | Primary keyword (hyphen-case) | ≤ 75 characters |
| **Meta Description** | Primary + benefit-driven summary | ≤ 160 characters, include real data point |
| **H1** | Primary keyword | Close match to SEO Title |
| **First paragraph** | Primary keyword within first 25 words | Google weighting |
| **At least one H2** | Primary or top secondary keyword | Topic reinforcement |
| **Body text** | Secondary + LSI keywords distributed naturally | Density: primary 0.5-2% |
| **Image file names** | Primary keyword as prefix | `keyword-descriptor.jpg` |
| **Image Alt text** | Equipment structure descriptions | Descriptive with keyword context |

#### RankMath Scoring Strategy

To achieve 90+/100:
- Primary keyword in: SEO Title (at start), Meta Description, URL, H1, first 100 words, one H2, one image Alt
- Readability: Flesch Reading Ease ≥ 60
- Content length: ≥ 900 words
- Internal links: ≥ 3 with descriptive anchors
- External links: ≥ 2 to authoritative sources
- No consecutive sentences starting with the same word
- Transition words in ≥ 30% of sentences

### Step 3: Competitor Case Study Analysis

Analyze 3-5 competitor case study pages:
- Title format and structure
- How they present the client (named vs anonymous)
- Depth of technical detail
- Use of images and diagrams
- Presence of FAQ or schema markup

Output: brief gap analysis — what competitors do well, what they miss.

### Step 4: Title Generation

Generate 3 title variants:

| Type | Pattern | Example |
|---|---|---|
| **SEO-First** | `[Product] Case Study: [Key Result] for [Industry Client]` | 20-Ton Hydraulic Pipe Upender Case Study: Safe 90° Tilting for Pressure Vessel Manufacturer |
| **Industry-Driven** | `How [Industry Client] Solved [Problem] with [Product] — [Brand]` | How a Saudi Pressure Vessel Plant Eliminated Crane Flipping Risks with a Custom Hydraulic Upender |
| **Spec-Driven** | `[Key Spec] [Product] for [Application] — [Brand] Project Reference` | 20-Ton Custom Hydraulic 90-Degree Upender for Large-Diameter Pipe — Gradin Project Reference |

Also generate:
- **URL slug**
- **Meta Description** (≤ 160 characters, benefit-driven summary with a real data point)
- **H1** (close match to chosen SEO Title)

### Step 5: Meta Description

≤ 160 characters. Include:
1. What the project was (product + industry)
2. The key problem solved
3. A data point or concrete result
4. Implicit CTA

Example:
```
See how our custom 20-ton hydraulic upender with integrated V-groove solved dangerous crane-tilting issues for large-diameter pressure vessels in Saudi Arabia.
```

### Step 6: Project Snapshot Table

MD table. 3 seconds for a buyer to determine industry match.

| Field | Value |
|---|---|
| Client | [Name or anonymous descriptor] |
| Industry | [Industry] |
| Location | [Country/Region] |
| Product | [Gradin Product Model + Name] |
| Key Spec | [1 most important spec] |
| Project Year | YYYY |

### Step 7: Client Background

1 paragraph. Answer: "Who is this client and what do they do?"

Keep it factual. Industry, scale, what they manufacture or handle. Do not praise the client — the reader wants to self-identify, not read a testimonial.

### Step 8: Challenge

3-4 specific pain points. Each must be a concrete problem, not a generic complaint.

Format each as:
```
**Pain Point Title**: What was happening, why it was dangerous/inefficient/costly.
```

Bad: "The client needed a better solution."
Good: "Tilting 20-ton cylindrical loads using overhead crane slings was unstable — the straps shifted along the smooth curved metal, presenting extreme risks of sudden slippage."

### Step 9: Gradin Solution

2-3 paragraphs. Answer: "What did Gradin build, and what engineering decisions made it work?"

Include:
- Product model and configuration
- Key customizations (materials, dimensions, features)
- Engineering rationale — WHY each decision was made
- Safety and compliance considerations

No marketing language. Describe the machine like an engineer would to another engineer.

### Step 10: Technical Specification Table

MD table. Key parameters only — not the full datasheet.

| Parameter | Value | Unit |
|---|---|---|
| [Key spec 1] | [Value] | [Unit] |
| [Key spec 2] | [Value] | [Unit] |
| ... | ... | ... |

Sort logically: capacity/dimensions → performance → power → safety/certifications.

### Step 11: Image Plan

For each image the user has or needs, specify:

| # | File Name | Alt Text | Insert After |
|---|---|---|---|
| 1 | `keyword-descriptor.jpg` | [Equipment structure description with keyword] | [Section name, paragraph position] |

Image Alt text rule: describe the equipment structure, not generic labels. "Gradin HU-20T-V hydraulic upender with integrated V-groove platform and L-shaped retention walls" — not "case study image 1".

### Step 12: Schema Markup

Generate JSON-LD blocks:

**Article Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[Title]",
  "author": { "@type": "Organization", "name": "Gradin" },
  "datePublished": "[YYYY-MM-DD]",
  "dateModified": "[YYYY-MM-DD]",
  "publisher": {
    "@type": "Organization",
    "name": "Gradin",
    "logo": { "@type": "ImageObject", "url": "[Logo URL]" }
  },
  "image": { "@type": "ImageObject", "url": "[Main Case Image URL]" }
}
```

**FAQ Schema**: Use the 7 general FAQs from the user's fixed template.

**BreadcrumbList Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://gradin-lifts.com/" },
    { "@type": "ListItem", "position": 2, "name": "Case Studies", "item": "https://gradin-lifts.com/case/" },
    { "@type": "ListItem", "position": 3, "name": "[Title]", "item": "[URL]" }
  ]
}
```

### Step 13: Quality Check

- [ ] All keywords placed per RankMath map (Step 2)
- [ ] URL slug ≤ 75 characters, hyphen-case, primary keyword present
- [ ] SEO Title ≤ 60 characters, primary keyword at front
- [ ] Meta Description ≤ 160 characters, includes real data point
- [ ] H1 contains primary keyword
- [ ] Primary keyword in first 100 words
- [ ] Image file names follow `keyword-descriptor.jpg` format
- [ ] Image Alt text describes equipment structure (not generic labels)
- [ ] Spec table is MD-formatted with consistent units
- [ ] No AI cliché openings or exaggerated claims
- [ ] No fabricated numbers — `[placeholder]` used where data is unavailable
- [ ] Flesch Reading Ease ≥ 60
- [ ] Content ≥ 900 words
- [ ] ≥ 3 internal links with descriptive anchors
- [ ] ≥ 2 external links to authoritative sources
- [ ] English punctuation only throughout
- [ ] English → Chinese block delivery respected