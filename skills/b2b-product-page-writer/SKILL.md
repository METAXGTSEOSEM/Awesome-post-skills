---
name: b2b-product-page-writer
description: Generate B2B industrial product page content optimized for Google rankings and RankMath SEO scoring. Covers product title (3 variants), short description, features (feature → benefit), application scenarios, MD-formatted spec tables, FAQ, schema markup, and full keyword placement (primary/secondary/LSI in title, URL slug, meta description, H1, image file names, image Alt text). Use when user needs to write a B2B product page, create product descriptions for industrial equipment, or optimize an existing product page for SEO/RankMath.
---

# B2B Product Page Writer

Generate B2B industrial product page content optimized for Google ranking and RankMath SEO score. Only generates **variable content blocks** — the user already has fixed template blocks for certifications, CTA, related products, and downloads.

## Prerequisites

Collect from the user:
- **Product name** and **category**
- **Product specifications/parameters** (dimensions, capacity, materials, power, etc.)
- **Core application scenarios** (3-5 industries or use cases)
- **Key selling points** (what makes this product different)
- **Existing certifications** (ISO, CE, ANSI, etc.)
- **Competitor product page URLs** (3-5)
- **Website domain** (for URL slug suggestions)

## Blocks Generated (What You Output)

The fixed template blocks (certifications, CTA, related products, downloads) are already handled — do NOT generate them.

Only generate these 7 variable blocks:

| # | Block | Format |
|---|---|---|
| 1 | Title | 3 SEO variants |
| 2 | Short Description | 120-160 characters |
| 3 | Features | 5-8 feature → benefit pairs |
| 4 | Application Scenarios | 3-5 scenarios with 1-sentence description each |
| 5 | Spec Table | MD table |
| 6 | FAQ | 6-8 Q&A (50% product + 50% purchase) |
| 7 | Schema Markup | JSON-LD |

---

## Step 1: Product Info Collection

If any of these are missing, ask the user:
- Complete spec parameters (value + unit for each)
- Certification list (standard names + numbers)
- Competitor product page URLs

---

## Step 2: Competitor Product Page Analysis

Analyze 3-5 competitor product pages for the same/similar product:
- Extract their Title tag format, H1, and URL structure
- Extract their feature list structure (how many features, benefit-style or spec-style)
- Check if they have FAQ, application scenarios, spec tables
- Note their keyword patterns in headings and body text

Output: brief comparison table showing what competitors do well and where they fall short.

---

## Step 3: Keyword Research & Placement Plan

### Primary Keyword (1)

The main product keyword buyers search for. Derived from product name + key attribute:
- Pattern: `[Product Type]` or `[Attribute] [Product Type]` or `[Product Type] for [Application]`
- Example: "Heavy-duty scissor lift" / "Hydraulic dock leveler" / "Vertical reciprocating conveyor for warehouses"

### Secondary Keywords (5-8)

Long-tail variations buyers use at different purchase stages:
- Pattern: `[Primary] + [spec]` / `[Primary] + [application]` / `[Primary] + [certification]`
- Examples: "heavy-duty scissor lift 5000kg" / "hydraulic dock leveler CE certified" / "industrial lift table for automotive"

### LSI / Semantic Keywords (5-10)

Related terms Google expects to see in context:
- Material terms, standard names, industry terms, synonym variations

### RankMath Keyword Placement Map

| Placement Target | Keyword | Notes |
|---|---|---|
| **URL slug** | Primary keyword (hyphen-case) | Keep ≤ 75 characters, include core product term |
| **SEO Title / Meta Title** | Primary keyword at front | ≤ 60 characters total; format: `[Primary] — [Brand] [Secondary]` |
| **Meta Description** | Primary + 1 secondary | ≤ 160 characters; include value proposition + CTA hint |
| **H1** | Primary keyword | Exact or close match to SEO title |
| **First paragraph** | Primary keyword within first 25 words | Google counts this heaviest |
| **At least one H2** | Primary or top secondary keyword | Reinforces topic relevance |
| **Body text** | Secondary + LSI keywords distributed naturally | Density: primary 0.5-2%, secondaries 0.3-1% |
| **Image file names** | Primary keyword as prefix | Format: `keyword-descriptor.jpg` |
| **Image Alt text** | Primary or secondary keyword | Descriptive with product context, no stuffing |

### RankMath Scoring Strategy

To maximize RankMath SEO score, ensure:
- Primary keyword in: SEO Title (at start), Meta Description, URL, H1, first 100 words, one H2, one image Alt
- Readability: Flesch Reading Ease ≥ 60, active voice, short sentences
- Content length: ≥ 900 words for product pages (RankMath minimum; B2B target ≥ 1500)
- Keyword density: primary 0.5-2.0%, no stuffing
- Internal links: ≥ 3 with descriptive anchors
- External links: ≥ 2 to authoritative sources
- No consecutive sentences starting with the same word
- Transition words used in ≥ 30% of sentences
- Image Alt on every image, image file names SEO-friendly

---

## Step 4: Title Generation

Generate 3 title variants for A/B testing:

| Type | Pattern | Example | Best For |
|---|---|---|---|
| **SEO-First** | `[Primary Keyword] — [Brand]` | Heavy Duty Scissor Lift — Gradin | Search visibility, exact match CTR |
| **Scenario-Driven** | `[Primary] for [Application/Industry] — [Brand]` | Industrial Scissor Lift for Warehouse Logistics — Gradin | Capturing scenario intent, higher commercial intent |
| **Spec-Driven** | `[Key Spec] [Product Type] — [Brand]` | 5000kg Heavy Duty Hydraulic Scissor Lift — Gradin | Long-tail spec searches, qualified traffic |

Also generate the corresponding:
- **URL slug** (hyphen-case, ≤ 75 chars, primary keyword included)
- **Meta Description** (≤ 160 chars, primary keyword + value proposition)
- **H1** (close match to chosen SEO Title)

---

## Step 5: Short Description

120-160 characters. Include:
1. What the product is (category)
2. Key differentiating spec or feature
3. Primary application or target audience
4. Implicit CTA or value signal

Example:
```
Heavy-duty hydraulic scissor lift with 5000kg capacity and double-pantograph design for warehouse mezzanine access. CE certified, built with Q345B steel for 10-year service life.
```

---

## Step 6: Features (Feature → Benefit)

5-8 items. Each must be a feature → benefit pair, not a flat spec list.

Format: `**Feature**: Benefit statement explaining why this matters to the buyer.`

| Feature | → | Benefit (Why it matters) |
|---|---|---|
| 5000kg load capacity | → | Handles palletized goods, machinery parts, and steel stillages without capacity anxiety |
| Double pantograph design | → | Reaches 4.2m mezzanine height from a low collapsed profile, fitting standard warehouse floor plans |
| Q345B structural steel frame | → | 20% higher yield strength than standard steel — extends frame life under daily cyclic loading |
| CE certified + ISO 9001 factory | → | Meets EU import requirements and ensures consistent manufacturing quality |
| 125% overload static tested | → | Every unit proof-tested before shipment — no surprises at installation |

---

## Step 7: Application Scenarios

3-5 scenarios. Each: **Industry/Use Case** + 1-sentence description of how the product fits.

Format:
```
- **Automotive Parts Warehousing**: Heavy pallet loads with frequent lift cycles — the double-pantograph design handles 30+ cycles/day without hydraulic overheating.
- **Steel Coil Handling**: Compact platform with reinforced decking lifts coils up to 5000kg for production line feeding.
```

---

## Step 8: Technical Specification Table

Generate as a **Markdown table**. Format: Parameter | Value | Unit.

Rules:
- Sort rows logically: capacity/dimensions first → performance → materials → electrical → certifications
- Use consistent units throughout (metric preferred for B2B)
- Include safety and certification rows at the bottom

| Parameter | Value | Unit |
|---|---|---|
| Rated Load Capacity | 5000 | kg |
| Max Lift Height | 4200 | mm |
| Collapsed Height | 650 | mm |
| Platform Size (L×W) | 2500 × 3500 | mm |
| Lifting Speed | 80 | mm/s |
| Motor Power | 5.5 | kW |
| Power Supply | 380V / 50Hz / 3-Phase | — |
| Hydraulic Oil Capacity | 40 | L |
| Safety Standard | CE / ISO 9001 | — |
| Structural Steel Grade | Q345B | — |

---

## Step 9: FAQ

6-8 questions. 50% product questions, 50% purchase/delivery questions.

Product questions (3-4):
- What is the maximum load this product can handle continuously?
- What safety features come standard?
- Does this require a pit for installation?
- What maintenance schedule is recommended?

Purchase questions (3-4):
- What is the MOQ for this product?
- What is the typical lead time from order to delivery?
- Do you offer OEM/ODM customization?
- What certifications are included with the product?

Each Q&A: 2-4 sentences. Factual, no marketing fluff.

---

## Step 10: Schema Markup + Quality Check

### Schema Markup

Generate these JSON-LD blocks:

**Product Schema**:
```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "[Product Name]",
  "description": "[Short Description]",
  "sku": "[SKU]",
  "brand": { "@type": "Brand", "name": "[Brand Name]" },
  "category": "[Category]",
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
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://[domain]/" },
    { "@type": "ListItem", "position": 2, "name": "Products", "item": "https://[domain]/products/" },
    { "@type": "ListItem", "position": 3, "name": "[Product Name]", "item": "https://[domain]/products/[slug]/" }
  ]
}
```

### Quality Check Checklist

- [ ] All keywords placed per RankMath map (Step 3)
- [ ] URL slug ≤ 75 characters, hyphen-case, primary keyword present
- [ ] Meta Title ≤ 60 characters, primary keyword at front
- [ ] Meta Description ≤ 160 characters
- [ ] H1 contains primary keyword
- [ ] Primary keyword in first 100 words of description
- [ ] Image file names follow `keyword-descriptor.jpg` format
- [ ] Image Alt text on every image with keyword context
- [ ] Spec table is MD-formatted with consistent units
- [ ] FAQ has 6-8 Q&As, balanced product/purchase split
- [ ] No AI cliché openings or fluff phrases
- [ ] Flesch Reading Ease ≥ 60
- [ ] Content ≥ 900 words (RankMath minimum)
- [ ] ≥ 3 internal links with descriptive anchors
- [ ] ≥ 2 external links to authoritative sources
- [ ] Transition words in ≥ 30% of sentences