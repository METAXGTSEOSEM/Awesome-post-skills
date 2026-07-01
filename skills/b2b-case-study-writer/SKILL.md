---
name: b2b-case-study-writer
description: Generate B2B industrial case study/project reference pages optimized for Google rankings, GEO, EEAT, and RankMath SEO score (90+/100). Produces case study title (3 variants), meta description, project snapshot table, client background, challenge analysis, branded solution, MD-formatted spec table, image placement plan, and schema markup. Use when user needs to write a B2B case study, create a project reference page, or document a customer installation for SEO.
---

# B2B Case Study Writer

Generate B2B industrial case study pages optimized for Google ranking, GEO, EEAT, and RankMath score 90+/100.

## Step 0: Variable Collection (MANDATORY -- Run Before Anything Else)

Before writing a single word, you MUST collect these variables from the user. If the user does not provide any item, use `[placeholder]` and ask the user to fill it later. Never hardcode any brand name, URL, or keyword into the skill -- every value comes from this step.

| Variable | Required? | Description | If Not Provided |
|---|---|---|---|
| `{Brand}` | Yes | Company/brand name | Ask again. Cannot proceed without it. |
| `{BrandFull}` | No | Full legal company name | Default to `{Brand}` |
| `{SiteURL}` | Yes | Full site URL (e.g., `https://example.com`) | Ask again. Needed for breadcrumbs, internal links, schema. |
| `{CaseArchiveURL}` | No | Case studies archive page URL | Default to `{SiteURL}/case/` |
| `{TargetKeyword}` | Yes | Primary keyword for this case | Ask the user to provide or approve your suggestion. |
| `{SecondaryKeywords}` | No | 6-10 secondary keywords | Generate from user input + Google top results analysis. |
| `{CompetitorURLs}` | No | Up to 5 competitor URLs for gap analysis | Skip. Mention to user that competitive insight was not available. |
| `{CaseData}` | Yes | All known project data: client name/industry/location/product/specs/year | Use `[placeholder]` for anything not yet known. Never invent. |

**After collection**: Display all variables in a summary table and ask user to confirm before proceeding to Step 1.

---

## What This Skill Generates (Variable Blocks)

Only generate these blocks. Fixed template blocks -- general FAQ (7 questions), related products, inquiry CTA, certification wall, customer logo wall -- already exist in the user''s template and must NOT be generated.

| # | Block | Format |
|---|---|---|
| 1 | SEO Metadata | Keyword plan + Title variants + URL + Meta Description + Image Alt |
| 2 | Project Snapshot | MD table |
| 3 | Client Background | 1 paragraph |
| 4 | Challenge | 3-4 specific pain points |
| 5 | {Brand} Solution | 2-3 paragraphs with engineering detail |
| 6 | Technical Spec Table | MD table |
| 7 | Image Plan | File names, Alt text, placement |
| 8 | Schema Markup | JSON-LD |

---

## Output Format & Rules

### Block-Level Bilingual Output

- **English block first**, then Chinese translation immediately below. Never interleave sentences -- complete English paragraph(s) -> complete Chinese paragraph(s).
- Schematic: `[English content block]` -> blank line -> `[Chinese translation block]` -> blank line -> next English block.

### Strict Half-Width Punctuation

- **100% English half-width punctuation everywhere** -- including Chinese translations, tables, lists, and parenthetical text.
- Allowed: `.` `,` `:` `;` `?` `!` `-` `--` `(` `)` `[` `]` `"` `"`
- Banned: any full-width punctuation characters (`, ` `,` `:` `;` `"` `"` `''` `''` `(` `)` `[` `]`)
- This rule is absolute. There are no exceptions, even in the Chinese translation sections.

### No AI Transitional Fluff

- Banned words and patterns: "furthermore", "moreover", "in addition", "additionally", "besides", "in conclusion", "to summarize", "in summary", "overall", "all in all"
- Replace with: direct cause-and-effect engineering logic. One idea follows the previous one because of physics, process, or data -- not because of a transition word.

### No Marketing Hype or AI-Speak

- Banned patterns: "cost-effective", "high ROI", "time-saving", "best-in-class", "industry-leading", "unparalleled", "revolutionary", "game-changing", exaggerated claims without physical evidence.
- Replace with: specific physical benefits. Example: instead of "improved safety", write "the dual-channel safety circuit cut emergency stop response to under 50 ms, removing the spinal injury exposure during manual pipe rotation."

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
| 7 | Project Gallery | Image placeholder guide -- describe what real engineering photos should be inserted (user uploads later) |

### Segmented Output Control

- **Output only the section currently requested.** Never generate the entire case study in one response.
- After each section, pause and wait for the user''s next instruction (e.g., "Section 2" or "Next: Challenge").
- This prevents model attention decay and character truncation.

### Link Directory (End of Article)

At the very end of the complete case study, output a bilingual link directory table summarizing every internal and external link used:

| Anchor Text (EN) | Anchor Text (zhong wen) | URL | Type |
|---|---|---|---|
| [English anchor] | [Chinese anchor] | [URL] | Internal / External |

### Live Link Verification

- **External links**: You must search live / fetch the official standards body website (e.g., asme.org, iso.org, bsigroup.com) to find the actual canonical URL. Never fabricate a link, a virtual page, or a 404-prone URL. Return only the real, active, permanent canonical URL.
- **Format**: `[Natural English anchor text] = Real official URL`
- **Internal links**: Construct from `{SiteURL}` and `{CaseArchiveURL}` variables. If the user provides competitor URLs in Step 0, inspect them for structural insight. If `{SiteURL}` was not provided, skip internal links -- never guess.

---

## Core Writing Principles

### 1. Target Audience

Write for three personas simultaneously:
- **Procurement Manager**: Needs to know industry match, timeline, and whether `{Brand}` can deliver
- **Engineer**: Needs technical detail -- specs, materials, safety, how it works
- **Business Owner**: Needs business impact -- why this investment made sense

All three must find their answer on the page without scrolling past irrelevant content.

### 2. Output Language Rule

- **All interactions with the user**: Chinese
- **All generated content (deliverables)**: English first, then Chinese translation block below.
- **This is a bilingual output rule, not a translation agency rule** -- do not add "Translation:" labels. Just output English block, blank line, Chinese block. Naturally.

### 3. International Site Perspective

- Write for an international B2B audience. Do not use Chinese punctuation, Chinese formatting conventions, or region-specific references.
- All punctuation must be English half-width, even in Chinese blocks.
- Industry terminology uses international standard units and nomenclature.

### 4. Search Intent Awareness

- Analyze the search intent behind `{TargetKeyword}` before writing. What does a real buyer typing this keyword actually want to know?
- Structure content to answer the questions a procurement engineer would ask in order: "Can they handle my industry?" -> "How did they solve a similar problem?" -> "What did they actually build?" -> "Do the specs match my requirements?"

---

## Step-by-Step SOP

### Step 1: Confirm Variables

Display all Step 0 variables in a summary table. Ask user to confirm or revise. Do not proceed until confirmed.

### Step 2: Keyword Map & Competitor Gap

- Analyze top 10 Google results for `{TargetKeyword}`. Extract: common H2 topics, content length, schema types used, image count, internal link density.
- Run competitor content gap: what do competitor case study pages cover that creates an opportunity for differentiation.
- Build a RankMath keyword placement map: where `{TargetKeyword}` goes (H1, first 100 words, one H2, meta description, URL slug, 2-3 image Alt texts) and where each `{SecondaryKeywords}` goes.
- Lock the brand position: This is `{Brand}`''s case study. Never mimic competitor tone or structure. Compete on engineering depth, not on claims.

### Step 3: SEO Block

Generate:
- **Primary Keyword**: `{TargetKeyword}`
- **Secondary Keywords**: `{SecondaryKeywords}` list
- **URL Slug**: `{CaseURL}` -- constructed from `{SiteURL}` + `/case/` + hyphen-case slug (<=75 chars, primary keyword present)
- **Image Alt Plan**: keywords mapped to each expected image position

### Step 4: Case Title (H1)

Generate 3 title variants:

| Style | Formula | Example |
|---|---|---|
| **Result-Driven** | `How [Client Industry] Solved [Problem] with [Product] -- {Brand}` | How a Saudi Pressure Vessel Plant Eliminated Crane Flipping Risks with a Custom Hydraulic Upender |
| **Spec-Driven** | `[Key Spec] [Product] for [Application] -- {Brand} Project Reference` | 20-Ton Custom Hydraulic 90-Degree Upender for Large-Diameter Pipe -- {Brand} Project Reference |
| **Process-Driven** | `[Application] [Product]: A {Brand} Engineering Case Study` | Large-Diameter Pipe Rotation Upender: A {Brand} Engineering Case Study |

Also generate:
- **URL slug**
- **Meta Description** (<=160 characters, benefit-driven summary with a real data point)
- **H1** (close match to chosen SEO Title)

### Step 5: Meta Description

<=160 characters. Include:
1. What the project was (product + industry)
2. The key problem solved
3. A data point or concrete result
4. Implicit CTA

### Step 6: Project Snapshot Table

MD table. 3 seconds for a buyer to determine industry match.

| Field | Value |
|---|---|
| Client | [Name or anonymous descriptor] |
| Industry | [Industry] |
| Location | [Country/Region] |
| Product | [{Brand} Product Model + Name] |
| Key Spec | [1 most important spec] |
| Project Year | YYYY |

### Step 7: Client Background

1 paragraph. Answer: "Who is this client and what do they do?"

Keep it factual. Industry, scale, what they manufacture or handle. Do not praise the client -- the reader wants to self-identify, not read a testimonial.

### Step 8: Challenge

3-4 specific pain points. Each must be a concrete problem with business consequences, not a generic complaint.

Format each as:
```
**Pain Point Title**: What was happening, why it was dangerous/inefficient/costly.
```

Bad: "The client needed a better solution."
Good: "Tilting 20-ton cylindrical loads using overhead crane slings was unstable -- the straps shifted along the smooth curved metal, presenting extreme risks of sudden slippage. On three recorded occasions in the 12 months before this project, the load shifted mid-lift, one resulting in a 4-hour production halt."

### Step 9: {Brand} Solution

2-3 paragraphs. Answer: "What did {Brand} build, and what engineering decisions made it work?"

Include:
- Product model and configuration
- Key customizations (materials, dimensions, features)
- Engineering rationale -- WHY each decision was made (and what failure mode it prevents)
- Safety and compliance considerations

No marketing language. Describe the machine like an engineer would to another engineer. For every design decision, explain what problem would occur without it.

### Step 10: Technical Specification Table

MD table. Key parameters only -- not the full datasheet.

| Parameter | Value | Unit |
|---|---|---|
| [Key spec 1] | [Value] | [Unit] |
| [Key spec 2] | [Value] | [Unit] |
| ... | ... | ... |

Sort logically: capacity/dimensions -> performance -> power -> safety/certifications.

### Step 11: Image Plan

For each image the user has or needs, specify:

| # | File Name | Alt Text | Insert After |
|---|---|---|---|
| 1 | `keyword-descriptor.jpg` | [Equipment structure description with keyword] | [Section name, paragraph position] |

Image Alt text rule: describe the equipment structure, not generic labels. "{Brand} HU-20T-V hydraulic upender with integrated V-groove platform and L-shaped retention walls" -- not "case study image 1".

### Step 12: Schema Markup

Generate JSON-LD blocks using `{Brand}`, `{BrandFull}`, `{SiteURL}`, `{CaseURL}` variables:

**Article Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[Title]",
  "author": { "@type": "Organization", "name": "{BrandFull}" },
  "datePublished": "[YYYY-MM-DD]",
  "dateModified": "[YYYY-MM-DD]",
  "publisher": {
    "@type": "Organization",
    "name": "{BrandFull}",
    "logo": { "@type": "ImageObject", "url": "{SiteURL}/wp-content/uploads/logo.png" }
  },
  "image": { "@type": "ImageObject", "url": "{SiteURL}/wp-content/uploads/case/[slug]/main.jpg" }
}
```

**FAQ Schema**: Use the 7 general FAQs from the user''s fixed template.

**BreadcrumbList Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "{SiteURL}/" },
    { "@type": "ListItem", "position": 2, "name": "Case Studies", "item": "{CaseArchiveURL}" },
    { "@type": "ListItem", "position": 3, "name": "[Title]", "item": "{CaseURL}" }
  ]
}
```

### Step 13: Quality Check

- [ ] All keywords placed per RankMath map (Step 2)
- [ ] URL slug <=75 characters, hyphen-case, primary keyword present
- [ ] SEO Title <=60 characters, primary keyword at front
- [ ] Meta Description <=160 characters, includes real data point
- [ ] H1 contains primary keyword
- [ ] Primary keyword in first 100 words
- [ ] Image file names follow `keyword-descriptor.jpg` format
- [ ] Image Alt text describes equipment structure (not generic labels)
- [ ] Spec table is MD-formatted with consistent units
- [ ] No AI cliche openings or exaggerated claims
- [ ] No marketing hype words (cost-effective, high ROI, best-in-class, etc.)
- [ ] No fabricated numbers -- `[placeholder]` used where data is unavailable
- [ ] Flesch Reading Ease >=60
- [ ] Content >=900 words
- [ ] >=3 internal links with descriptive anchors
- [ ] >=2 external links to authoritative sources
- [ ] All external links verified as active (no 404)
- [ ] English punctuation only throughout
- [ ] English -> Chinese block delivery respected
- [ ] All `{Variable}` placeholders resolved before final output
