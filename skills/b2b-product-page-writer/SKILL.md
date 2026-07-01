---
name: b2b-product-page-writer
description: Generate B2B industrial product page content optimized for Google rankings and RankMath SEO scoring. Covers product title (3 variants), short description, features (feature -> benefit), application scenarios, MD-formatted spec tables, FAQ, schema markup, and full keyword placement (primary/secondary/LSI in title, URL slug, meta description, H1, image file names, image Alt text). Use when user needs to write a B2B product page, create product descriptions for industrial equipment, or optimize an existing product page for SEO/RankMath.
---

# B2B Product Page Writer

Generate B2B industrial product page content optimized for Google ranking and RankMath SEO score. Only generates **variable content blocks** -- the user already has fixed template blocks for certifications, CTA, related products, and downloads.

## Step 0: Variable Collection (MANDATORY -- Run Before Anything Else)

Before writing a single word, you MUST collect these variables from the user. If the user does not provide any item, use `[placeholder]` and ask the user to fill it later. Never hardcode any brand name, URL, or keyword into the skill -- every value comes from this step.

| Variable | Required? | Description | If Not Provided |
|---|---|---|---|
| `{Brand}` | Yes | Company/brand name | Ask again. Cannot proceed without it. |
| `{BrandFull}` | No | Full legal company name | Default to `{Brand}` |
| `{SiteURL}` | Yes | Full site URL (e.g., `https://example.com`) | Ask again. Needed for breadcrumbs, internal links, schema. |
| `{ProductName}` | Yes | Exact product name and model | Ask the user. |
| `{ProductCategory}` | Yes | Product category for breadcrumbs and schema | Ask the user. |
| `{TargetKeyword}` | Yes | Primary keyword for this product page | Ask the user to provide or approve your suggestion. |
| `{SecondaryKeywords}` | No | 5-8 secondary long-tail keywords | Generate from user input + Google top results analysis. |
| `{LSIKeywords}` | No | 5-10 LSI/semantic related terms | Generate from Google related searches and industry terminology. |
| `{CompetitorURLs}` | No | Up to 5 competitor product page URLs | Skip. Mention to user that competitive insight was not available. |
| `{ProductSpecs}` | Yes | All known product parameters: dimensions, capacity, materials, power, certifications | Use `[placeholder]` for anything not yet known. Never invent. |
| `{AppScenarios}` | No | 3-5 core application industries or use cases | Generate from product type if not provided. |

**After collection**: Display all variables in a summary table and ask user to confirm before proceeding to Step 1.

---

## Blocks Generated (What You Output)

The fixed template blocks (certifications, CTA, related products, downloads) are already handled -- do NOT generate them.

Only generate these 7 variable blocks:

| # | Block | Format |
|---|---|---|
| 1 | Title | 3 SEO variants |
| 2 | Short Description | 120-160 characters |
| 3 | Features | 5-8 feature -> benefit pairs |
| 4 | Application Scenarios | 3-5 scenarios with 1-sentence description each |
| 5 | Spec Table | MD table |
| 6 | FAQ | 6-8 Q&A (50% product + 50% purchase) |
| 7 | Schema Markup | JSON-LD |

---

## Output Format & Rules

### Block-Level Bilingual Output

- **English block first**, then Chinese translation immediately below. Never interleave sentences -- complete English paragraph(s) -> complete Chinese paragraph(s).
- Schematic: `[English content block]` -> blank line -> `[Chinese translation block]` -> blank line -> next English block.

### Strict Half-Width Punctuation

- **100% English half-width punctuation everywhere** -- including Chinese translations, tables, lists, and parenthetical text.
- Allowed only: `,` `.` `:` `;` `?` `!` `-` `--` `(` `)` `[` `]` `"` `"` `'` `'` (English half-width only)
- Absolutely banned: any Chinese full-width punctuation marks such as `,` `.` `:` `;` `(` `)` `[` `]` `"` `"` `'` `'` `!` `?` and all other full-width characters
- This rule is absolute. There are no exceptions, even in the Chinese translation sections.

### No AI Transitional Fluff

- Banned words and patterns: "furthermore", "moreover", "in addition", "additionally", "besides", "in conclusion", "to summarize", "in summary", "overall", "all in all"
- Replace with: direct cause-and-effect engineering logic. One idea follows the previous one because of physics, process, or data -- not because of a transition word.

### No Marketing Hype or AI-Speak

- Banned patterns: "cost-effective", "high ROI", "time-saving", "best-in-class", "industry-leading", "unparalleled", "revolutionary", "game-changing", exaggerated claims without physical evidence.
- Replace with: specific physical benefits. Instead of "improved safety", write concrete measurable outcomes.

### International Site Perspective

- Write for an international B2B audience. Do not use Chinese punctuation, Chinese formatting conventions, or region-specific references.
- All punctuation must be English half-width, even in Chinese blocks.
- Industry terminology uses international standard units and nomenclature.

### Search Intent Awareness

- Analyze the search intent behind `{TargetKeyword}` before writing. What does a real buyer typing this keyword actually want to know?
- Structure content to answer the questions a procurement engineer would ask in order: "What spec range does this cover?" -> "How does it compare?" -> "Which industries use it?" -> "How do I buy it?"

### Internal Link Placement

- Short Description: embed 1 internal link to a related product or case study.
- Features block: embed 1 internal link within a feature description, linking to another product or supporting article.
- Application Scenarios: embed 1 internal link to a related case study or application page.
- Never cluster all internal links in one block. Distribute them naturally.
### Segmented Output Control

- **Output only the section currently requested.** Never generate all 7 blocks in one response.
- After each section, pause and wait for the user''s next instruction.
- This prevents model attention decay and character truncation.

### Live Link Verification

- **External links**: You must search live / fetch the official standards body website (e.g., asme.org, iso.org, bsigroup.com) to find the actual canonical URL. Never fabricate a link, a virtual page, or a 404-prone URL. Return only the real, active, permanent canonical URL.
- **Internal links**: Construct from `{SiteURL}`. Ask the user for their site structure (product pages, case studies, blog posts) to generate correct internal links with proper anchor text. Link to related products, relevant case studies, or supporting articles from within the full site -- not just this product page. If `{SiteURL}` was not provided, skip internal links -- never guess.

### Link Directory (End of Article)

At the very end of the complete product page, output a bilingual link directory table summarizing every internal and external link used:

| Anchor Text (EN) | Anchor Text (zhong wen) | URL | Type |
|---|---|---|---|
| [English anchor] | [Chinese anchor] | [URL] | Internal / External |

---

## Step-by-Step SOP

### Step 1: Confirm Variables

Display all Step 0 variables in a summary table. Ask user to confirm or revise. Do not proceed until confirmed.

### Step 2: Competitor Product Page Analysis

Analyze 3-5 competitor product pages for the same/similar product:
- Extract their Title tag format, H1, and URL structure
- Extract their feature list structure (how many features, benefit-style or spec-style)
- Check if they have FAQ, application scenarios, spec tables
- Note their keyword patterns in headings and body text

Output: brief comparison table showing what competitors do well and where they fall short.

Lock the brand position: This is `{Brand}`''s product page. Never mimic competitor tone or structure. Compete on engineering depth, not on claims.

### Step 3: Keyword Research & Placement Plan

#### Primary Keyword (1)

The main product keyword buyers search for. Derived from `{TargetKeyword}`.

#### Secondary Keywords (5-8)

Long-tail variations from `{SecondaryKeywords}`.

#### LSI / Semantic Keywords (5-10)

Related terms from `{LSIKeywords}`.

#### RankMath Keyword Placement Map

| Placement Target | Keyword | Notes |
|---|---|---|
| **URL slug** | Primary keyword (hyphen-case) | Keep <=75 characters, include core product term |
| **SEO Title / Meta Title** | Primary keyword at front | <=60 characters total; format: `[Primary] -- {Brand} [Secondary]` |
| **Meta Description** | Primary + 1 secondary | <=160 characters; include value proposition + CTA hint |
| **H1** | Primary keyword | Exact or close match to SEO title |
| **First paragraph** | Primary keyword within first 25 words | Google counts this heaviest |
| **At least one H2** | Primary or top secondary keyword | Reinforces topic relevance |
| **Body text** | Secondary + LSI keywords distributed naturally | Density: primary 0.5-2%, secondaries 0.3-1% |
| **Image file names** | Primary keyword as prefix | Format: `keyword-descriptor.jpg` |
| **Image Alt text** | Primary or secondary keyword | Descriptive with product context, no stuffing |

#### RankMath Scoring Strategy

To maximize RankMath SEO score:
- Primary keyword in URL slug, SEO title, H1, first paragraph, meta description, and at least one image Alt
- SEO title <=60 characters, meta description <=160 characters
- >=3 internal links and >=2 external links per page
- Transition words in >=30% of sentences (use cause-and-effect, not fluff)
- Content >=900 words
- Flesch Reading Ease >=60

### Step 4: Product Title

Generate 3 title variants:

| Style | Formula | Example |
|---|---|---|
| **Product-Driven** | `[Product Name] -- [Category] for [Application]` | Heavy-Duty Hydraulic Scissor Lift -- Industrial Lift Table for Warehouse Mezzanine Access |
| **Spec-Driven** | `[Key Spec] [Product Name] | [Industry Short]` | 5000kg Heavy-Duty Hydraulic Scissor Lift | Industrial |
| **Benefit-Driven** | `[Product Name]: [Key Benefit]` | Heavy-Duty Hydraulic Scissor Lift: Double-Pantograph Design, 10-Year Frame Life |

Also generate:
- **URL slug** (hyphen-case, from `{SiteURL}` + `/products/` + slug)
- **SEO Title** (<=60 characters)
- **Meta Description** (<=160 characters, benefit-driven)
- **H1** (close match to SEO Title)

### Step 5: Short Description

120-160 characters. Include:
1. What the product is (category)
2. Key differentiating spec or feature
3. Primary application or target audience
4. Implicit CTA or value signal

### Step 6: Features

Structure:

1. **One-line summary** at the top -- what this product solves in plain engineering language. Not a slogan. Not a list. One sentence capturing the core value.

2. **3 Feature items** below. Format matches Application Scenarios: `- **Label**: Description sentence.`

Each Feature = one bold label + one description sentence. 3 items total.

The 3 dimensions to cover (pick the 3 most relevant; do NOT use the same 3 for every product):

| Dimension | What It Covers | Example Labels |
|---|---|---|
| **Key Spec** | The number buyers check first | Load Capacity, 90-Degree Tilt, 4200mm Lift Height, 80mm/s Speed |
| **Differentiator** | What separates this from standard alternatives | Dual-cylinder Synchronized Drive, Compact Footprint, Tool-Free Adjustment, Modular Frame |
| **Safety/Compliance** | Certifications, safety mechanisms, standards met | CE + ISO 9001 Certified, Dual-channel Emergency Stop, Overload Protection at 125 percent |
| **Build/Components** | Materials, branded parts, structural choices | Q345B Structural Steel Frame, Siemens Motor, SKF Bearings, All-Welded Construction |
| **Operational Result** | A physical consequence of the design -- no marketing words | Zero-Drift Angle Holding, No Strap-Down Between Rotations, Single-Operator Control |

Rules:
- Labels must be derived from `{ProductSpecs}` -- never invent Siemens, SKF, or any brand unless the user provided it.
- If the user did not provide certifications or branded components, use the Safety/Compliance or Build dimensions with structural descriptions instead of brand names.
- Never write "improves efficiency", "saves time", or any hollow benefit. Every explanation must trace to a physical cause.
- Format exactly like Application Scenarios: `- **Label**: Description.` (bold label, colon, space, description sentence).

Example format (product: hydraulic upender):
```
10-ton 90-degree hydraulic tilt, replacing multi-operator crane flipping with a single-operator controlled workstation.

- **10,000 kg Rated Capacity**: Handles full-size steel coils, pipes, and fabricated weldments in a single lift without load distribution concerns.
- **Dual Synchronized Hydraulic Cylinders**: Balanced torque across the full platform width prevents twist that single-cylinder designs experience with off-center loads.
- **CE + ISO 9001 Certified**: Meets EU machinery directive import requirements with third-party audited factory quality management.
```

### Step 7: Application Scenarios

3-5 scenarios. Each: **Industry/Use Case** + 1-sentence description of how the product fits.

Format:
```
- **Industry/Use Case**: Concrete description of how this product operates in that environment.
```


**Translation rule**: When outputting the Chinese version of the Spec Table, keep the Parameter and Unit column headers in English. Only translate the Chinese annotations if needed. The Parameter names and Unit symbols are international standards and must not be translated. Example: "Rated Load Capacity" stays in English in both versions.
### Step 8: Technical Specification Table

Generate as a **Markdown table**. Format: Parameter | Value | Unit.

Rules:
- Sort rows logically: capacity/dimensions first -> performance -> materials -> electrical -> certifications
- Use consistent units throughout (metric preferred for B2B)
- Include safety and certification rows at the bottom

| Parameter | Value | Unit |
|---|---|---|
| [Spec 1] | [Value] | [Unit] |
| [Spec 2] | [Value] | [Unit] |
| ... | ... | ... |

### Step 9: FAQ

6-8 questions. 50% product questions, 50% purchase/delivery questions.

Product questions (3-4):
- Technical capability questions specific to this product type
- Safety and compliance questions
- Installation and maintenance questions

Purchase questions (3-4):
- MOQ, lead time, customization capability
- Shipping, warranty, after-sales support

Each Q&A: 2-4 sentences. Factual, no marketing fluff.

### Step 10: Schema Markup + Quality Check

### Link Directory + Schema Markup

**Output order**: Link Directory first (human-readable bilingual table) -> blank line -> Schema Markup (JSON-LD, machine-readable).

### Link Directory

### Schema Markup

Generate JSON-LD blocks using `{Brand}`, `{BrandFull}`, `{SiteURL}`, `{ProductName}`, `{ProductCategory}` variables:

**Product Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "{ProductName}",
  "description": "[Short Description]",
  "sku": "[SKU]",
  "brand": { "@type": "Brand", "name": "{BrandFull}" },
  "category": "{ProductCategory}",
  "offers": {
    "@type": "Offer",
    "availability": "https://schema.org/InStock",
    "priceValidUntil": "[Date]"
  }
}
```

**FAQ Schema** (from Step 9).

**BreadcrumbList Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "{SiteURL}/" },
    { "@type": "ListItem", "position": 2, "name": "Products", "item": "{SiteURL}/products/" },
    { "@type": "ListItem", "position": 3, "name": "{ProductName}", "item": "{SiteURL}/products/[slug]/" }
  ]
}
```

### Quality Check Checklist

- [ ] All keywords placed per RankMath map (Step 3)
- [ ] URL slug <=75 characters, hyphen-case, primary keyword present
- [ ] Meta Title <=60 characters, primary keyword at front
- [ ] Meta Description <=160 characters
- [ ] H1 contains primary keyword
- [ ] Primary keyword in first 100 words of description
- [ ] Image file names follow `keyword-descriptor.jpg` format
- [ ] Image Alt text on every image with keyword context
- [ ] Spec table is MD-formatted with consistent units
- [ ] FAQ has 6-8 Q&As, balanced product/purchase split
- [ ] No AI cliche openings or exaggerated claims
- [ ] No marketing hype words (cost-effective, high ROI, best-in-class, etc.)
- [ ] No fabricated numbers -- `[placeholder]` used where data is unavailable
- [ ] All external links verified as active (no 404)
- [ ] Flesch Reading Ease >=60
- [ ] Content >=900 words (RankMath minimum)
- [ ] >=3 internal links with descriptive anchors to related products, case studies, or blog posts
- [ ] >=2 external links to authoritative sources
- [ ] English punctuation only throughout
- [ ] English -> Chinese block delivery respected
- [ ] All `{Variable}` placeholders resolved before final output
