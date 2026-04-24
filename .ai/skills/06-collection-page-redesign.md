# Skill 06 — Collection Page Redesign

## 1. Purpose

This skill is used to plan and implement YaksuDerma collection page improvements.

Collection pages are critical because YaksuDerma has a large technical product catalog with many product families, long product names, unit-based products, and multiple customer discovery paths.

This skill comes after:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
04-homepage-redesign.md
05-product-card-redesign.md
```

Collection page redesign should happen after product card foundations are stable, because collection pages depend heavily on product card behavior.

Codex must plan before implementation.

Do not edit files unless the user explicitly requests implementation after reviewing the collection page plan.

## 2. Required Context Files

Before collection page work, Codex must read:

```text
.ai/codex-instructions.md
.ai/brand-brief.md
.ai/store-brief.md
.ai/catalog-brief.md
.ai/navigation-brief.md
.ai/design-system.md
.ai/custom-components.md
.ai/content-rules.md
.ai/reference-sites.md
.ai/reference-site-links.md
.ai/prompt-playbook.md
.ai/skills/05-product-card-redesign.md
.ai/skills/06-collection-page-redesign.md
```

Codex should use these files to understand:

- Collection naming and handle strategy
- Final navigation labels
- Product card requirements
- Long product name handling
- Dynamic Shopify data rules
- Filtering and sorting preservation
- Mobile grid requirements
- Content safety rules
- SEO-safe collection descriptions

## 3. Collection Page Goal

Collection pages should help customers browse YaksuDerma’s product categories clearly and confidently.

They should feel:

- Organized
- Searchable
- Filter-friendly
- Mobile-friendly
- Professional
- Trustworthy
- Retail-friendly
- Clean and premium
- Not overwhelming despite large product counts

Collection pages should support:

- Category-first product discovery
- Search-first users who land on collections
- Long technical product names
- Dynamic product prices
- Product comparison through clean product cards
- Filtering and sorting
- Pagination
- SEO-friendly category naming

## 4. Collection Page Must Not Feel Like

Avoid collection pages that feel:

- Crowded
- Marketplace-like
- Discount-first
- Too technical
- Too cold
- Confusing
- Hard to scan
- Desktop-only
- Generic Dawn default
- Like a warehouse catalog

## 5. Final Collection Structure

Collection pages should follow the product architecture from `.ai/catalog-brief.md`.

Visible navigation labels may be short, but collection page titles should be professional and SEO-friendly.

Mapping:

```text
Toxins → Botulinum Toxins
Fillers → Dermal & Body Fillers
Skin Boosters → Skin Boosters & Exosomes
Fat Dissolvers → Mesotherapy & Contouring
Collagen Stimulators → Collagen Stimulators
Accessories → Clinical Accessories & IV Therapy
```

Suggested handles:

```text
botulinum-toxins
dermal-body-fillers
skin-boosters-exosomes
mesotherapy-contouring
collagen-stimulators
clinical-accessories-iv-therapy
```

## 6. Collection Header Requirements

Collection headers should be:

- Clear
- SEO-friendly
- Short
- Trustworthy
- Not claim-heavy
- Mobile-readable
- Consistent across categories

Collection header should include:

- Full collection title
- Optional short description
- Optional trust/category note
- Product count if Dawn supports it cleanly
- Breadcrumbs if available and useful

Avoid:

- Long dense text
- Medical claims
- Treatment promises
- Dosage/injection language
- Overly promotional sales copy

## 7. Safe Collection Description Examples

Use neutral product discovery language.

### Botulinum Toxins

```text
Explore Korean-origin botulinum toxin products with clear product information, dynamic pricing, and helpful support.
```

### Dermal & Body Fillers

```text
Browse dermal and body filler selections with organized product details and clean comparison-friendly product cards.
```

### Skin Boosters & Exosomes

```text
Discover skin booster, PDRN, and exosome product categories in a clear, easy-to-browse layout.
```

### Mesotherapy & Contouring

```text
Explore lipolytic and contouring product categories with clear product discovery and support when needed.
```

### Collagen Stimulators

```text
Browse collagen stimulator and biostimulator product selections in a clean, organized collection view.
```

### Clinical Accessories & IV Therapy

```text
Find numbing creams, dissolvers, IV-related products, and support items in one organized accessories category.
```

Do not use these descriptions if they conflict with actual store content or legal requirements.

## 8. Product Grid Requirements

The product grid should:

- Use the approved product card design
- Handle long technical product names
- Preserve dynamic Shopify prices
- Preserve product URLs
- Preserve product images
- Avoid crowded layouts
- Keep product cards aligned
- Maintain good image consistency
- Work well on mobile

Grid should feel:

- Clean
- Breathable
- Product-first
- Easy to compare
- Not overly sparse
- Not overly dense

## 9. Mobile Grid Requirements

Mobile collection pages are a priority.

Mobile grid should support:

- Readable product names
- Visible prices
- Product images that are not distorted
- Clear tap targets
- No horizontal overflow
- Filter/sort usability
- Comfortable spacing
- No overcrowded badges

Preferred mobile approach:

```text
Two-column product grid if readable.
One-column layout if long titles or images become crowded.
```

Codex must inspect actual mobile behavior before choosing.

## 10. Filtering and Sorting Rules

Codex must preserve Shopify native collection filtering and sorting.

Do not break:

- Facets
- Filters
- Sort dropdown
- Active filter chips
- Pagination
- Product count
- Collection URLs
- Query parameters
- Mobile filter drawer

Likely files:

```text
snippets/facets.liquid
assets/component-facets.css
sections/main-collection-product-grid.liquid
```

Do not rewrite filtering logic unless explicitly requested and thoroughly planned.

## 11. Pagination Rules

Preserve Dawn pagination logic.

Do not replace pagination with infinite scroll unless explicitly requested.

Avoid:

- Heavy JavaScript infinite scroll
- Breaking SEO pagination
- Removing pagination controls
- Hiding product count without reason

If improving pagination UI, keep it simple and accessible.

## 12. Product Data Rules

Collection pages must use Shopify dynamic data.

Codex must not hardcode:

- Product names
- Product prices
- Product URLs
- Product images
- Product availability
- Product badges
- Product descriptions
- Product claims

Use existing Shopify data and snippets:

```text
collection.products
product.title
product.price
product.featured_image
product.url
product.available
snippets/card-product.liquid
snippets/price.liquid
```

## 13. Badge Rules on Collection Pages

Badges may be used only if truthful and data-backed.

Potential badges:

```text
Korean Origin
Original Product
Popular
Featured
Professional Use
Wholesale Inquiry Available
Bestseller
```

Rules:

- Do not invent badges.
- Do not add certificate badges unless verified.
- Do not overuse badges.
- Avoid red-heavy sale badge styling.
- Keep badges subtle and consistent.

Possible data sources:

```text
product.tags
product.metafields.custom.badges
product.metafields.custom.product_origin
theme editor settings
```

## 14. Price Display on Collection Pages

Prices should be visible but calm.

Use dynamic Shopify price rendering.

Preferred:

- Price below product title
- Calm visual emphasis
- No oversized red styling
- Compare-at price handled by existing price snippet
- Clear enough for comparison

Avoid:

- Flash-sale look
- Fake urgency
- Hardcoded prices
- Marketplace discount design

## 15. Collection Page Trust Cues

Collection pages may include subtle trust cues.

Possible trust elements:

- Short category note
- Authenticity-focused microcopy
- Contact/support link
- Product availability note
- Carefully handled orders note

Safe examples:

```text
Questions about availability? Contact us for product details.
```

```text
We prioritize original Korean-origin products and clear information.
```

Avoid:

- Certificate claims unless verified
- Fast shipping claims
- Treatment promises
- Medical usage claims

## 16. Category-Specific UX Notes

### Toxins / Botulinum Toxins

Needs:

- Strong product card clarity
- Unit names visible
- Exact product titles
- Clean price comparison

Avoid:

- “Botox deals”
- Treatment claims
- Wrinkle-removal claims

### Fillers / Dermal & Body Fillers

Needs:

- Product family clarity
- Variant-like names readable
- Potential related product logic later, such as Liporase
- Clean image/product title rhythm

Avoid:

- Injection guidance
- Treatment area claims
- “Required with” cross-sell wording

### Skin Boosters

Needs:

- Clean premium visual feel
- PDRN / exosome names readable
- Trustworthy product discovery

Avoid:

- Regeneration guarantees
- Clinical result claims

### Fat Dissolvers

Needs:

- Clear commercial label
- Collection page may use fuller title “Mesotherapy & Contouring” or “Fat Dissolvers & Contouring”
- Careful wording around contouring

Avoid:

- Weight loss promises
- Guaranteed fat loss language
- Body transformation claims

### Collagen Stimulators

Needs:

- Premium specialist feel
- Clear product family presentation
- Not merged with Fat Dissolvers unless user changes architecture

Avoid:

- Collagen production/result promises
- Clinical outcome claims

### Accessories

Needs:

- Organized support item layout
- Numbing creams, dissolvers, IV-related products grouped clearly if possible
- Supportive category language

Avoid:

- Usage instructions
- Dosage/injection instructions
- Medical protocol wording

## 17. Reference Site Usage

Codex may use:

```text
.ai/reference-sites.md
.ai/reference-site-links.md
```

Use references for:

- Product grid clarity
- Filtering/sorting UX
- Mobile product list layout
- Category header structure
- Product discovery patterns
- Professional catalog organization

Do not copy:

- Exact layout
- Text
- Product claims
- Images
- Code
- Competitor category claims

## 18. Shopify Implementation Strategy

Collection page implementation should prefer:

- Existing Dawn collection structure
- Existing product card snippet
- Existing facets/filtering logic
- Existing pagination logic
- CSS and layout improvements first
- Minimal Liquid changes
- No unnecessary JavaScript

Create custom collection sections only if Dawn’s existing sections are insufficient and after user approval.

## 19. Possible Enhancements

Codex may propose, but should not implement all at once:

```text
Improved collection banner/header
Cleaner product grid spacing
Better mobile filter/sort styling
Trust microcopy under collection header
Category-specific intro block
Better empty-state copy
Product card badge support
Product family grouping hints
```

Do not implement product family comparison tables on collection pages unless explicitly requested.

## 20. Empty State Rules

If a collection has no products or filters return no results, copy should be helpful.

Good examples:

```text
No products found in this collection.
```

```text
Try adjusting your filters or contact us for product availability.
```

```text
This category is being updated. Contact us for current availability.
```

Avoid:

```text
Nothing here.
```

```text
Sold out forever.
```

```text
You missed it.
```

## 21. Files Likely Involved

Codex must inspect actual repo files.

Likely files:

```text
templates/collection.json
sections/main-collection-product-grid.liquid
sections/main-collection-banner.liquid
snippets/facets.liquid
snippets/card-product.liquid
snippets/price.liquid
assets/component-facets.css
assets/component-card.css
assets/component-price.css
assets/base.css
locales/*.json
```

Do not assume every file exists.

Dawn version may vary.

## 22. What Codex Must Preserve

Codex must preserve:

- Collection data
- Product URLs
- Product titles
- Product images
- Dynamic prices
- Shopify filtering
- Shopify sorting
- Pagination
- Active filter state
- Product count if present
- Collection title and description logic
- Product card dynamic data
- App blocks if present

Collection page changes can affect product discovery and SEO, so changes must be careful.

## 23. What Codex Must Not Do

During collection page work, Codex must not:

- Hardcode product prices
- Hardcode product names
- Hardcode collection URLs unless approved
- Remove filters
- Remove sorting
- Break pagination
- Replace collection logic with static product lists
- Add medical claims
- Add unverified certificate claims
- Add treatment promises
- Add heavy JavaScript
- Copy competitor layouts exactly
- Make the grid look like a cheap marketplace
- Implement infinite scroll unless explicitly requested

## 24. Planning Output Format

Before editing files, Codex must output:

```text
# Collection Page Redesign Plan — YaksuDerma

## 1. Files Inspected

List collection-related files inspected.

## 2. Current Collection Page Structure

Explain how Dawn currently renders collection pages.

## 3. Current Problems / Opportunities

Explain what needs improvement for YaksuDerma.

## 4. Collection Header Plan

Explain title, description, trust note, and SEO-safe language.

## 5. Product Grid Plan

Explain grid spacing, product card usage, image/title/price behavior.

## 6. Filtering and Sorting Preservation

Explain how native filtering/sorting will be preserved.

## 7. Mobile Strategy

Explain mobile grid and filter/sort behavior.

## 8. Dynamic Data Strategy

Explain what stays dynamic.

## 9. Files Likely Affected

List files.

## 10. Risks

List risk levels.

## 11. Implementation Phases

Break into small phases.

## 12. First Safe Implementation Step

Recommend exactly one next action.
```

## 25. Implementation Output Format

When implementation is requested, Codex must output:

```text
# Collection Page Redesign Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. What Changed

Explain collection header/grid/filter/style changes.

## 3. Shopify Functionality Preserved

Confirm:
- Filtering
- Sorting
- Pagination
- Product URLs
- Dynamic prices
- Product cards
- Collection data

## 4. Design System Alignment

Explain how changes follow `.ai/design-system.md`.

## 5. Mobile Behavior

Explain mobile collection behavior.

## 6. Content Safety

Confirm no medical/certification/shipping claims were invented.

## 7. Risk Level

Low / Medium / High.

## 8. Shopify Preview Test Steps

List test steps.

## 9. Follow-Up Tasks

Recommend next step.
```

## 26. Suggested Implementation Phases

Collection page improvements should be implemented in phases:

```text
Phase 1 — Collection header and safe description styling
Phase 2 — Product grid spacing and layout polish
Phase 3 — Filter/sort mobile visual improvement
Phase 4 — Empty state and support microcopy
Phase 5 — Category-specific refinements
Phase 6 — Mobile polish
Phase 7 — Theme check / validation
```

Do not implement all phases at once unless explicitly requested.

## 27. Risk Labels

Use these risk labels:

```text
Low
Medium
High
Do not touch yet
Needs user confirmation
```

Examples:

### Low Risk

- Collection header styling
- Product grid spacing
- Empty state copy
- Filter visual spacing
- Mobile spacing

### Medium Risk

- Collection banner markup
- Facet layout changes
- Product grid column changes
- Product card snippet changes

### High Risk

- Rewriting filtering logic
- Replacing pagination
- Changing collection data loops
- Adding heavy JavaScript
- Implementing infinite scroll

### Do Not Touch Yet

- Checkout
- Product form logic
- Hardcoded product prices
- Medical claims
- Unverified certificates

## 28. Example Planning Prompt

Use this prompt with Codex:

```text
Read:

- .ai/catalog-brief.md
- .ai/navigation-brief.md
- .ai/design-system.md
- .ai/content-rules.md
- .ai/reference-sites.md
- .ai/reference-site-links.md
- .ai/skills/06-collection-page-redesign.md

Analyze the current Dawn collection page.

Focus on:
- Collection header
- Product grid
- Filtering
- Sorting
- Pagination
- Mobile layout
- Long product title readability
- Dynamic prices
- SEO-friendly category titles
- Header label to collection title mapping:
  - Toxins → Botulinum Toxins
  - Fillers → Dermal & Body Fillers
  - Skin Boosters → Skin Boosters & Exosomes
  - Fat Dissolvers → Mesotherapy & Contouring
  - Accessories → Clinical Accessories & IV Therapy

Do not edit files yet.

Output:
1. Files inspected
2. Current collection page structure
3. UX problems/opportunities
4. Recommended collection page improvements
5. What must be preserved
6. Files likely affected
7. Risks
8. First safe implementation step
```

## 29. Example Implementation Prompt

Use this prompt after approving the collection page plan:

```text
Implement the approved first phase of collection page redesign.

Requirements:
- Preserve Shopify filtering.
- Preserve Shopify sorting.
- Preserve pagination.
- Preserve product URLs.
- Preserve dynamic product prices.
- Preserve collection data.
- Improve collection header and product grid presentation.
- Improve mobile readability.
- Do not add medical claims.
- Do not hardcode product data.

Output:
1. Files changed
2. What changed
3. Preserved Shopify functionality
4. Mobile behavior
5. Risk level
6. Shopify preview test steps
7. Follow-up tasks
```

## 30. Final Reminder

Collection pages are where customers browse and compare YaksuDerma’s catalog.

Main principle:

> Make collection pages organized, mobile-friendly, filter-safe, SEO-clear, and product-card driven — without breaking Shopify filtering, sorting, pagination, or dynamic product data.
