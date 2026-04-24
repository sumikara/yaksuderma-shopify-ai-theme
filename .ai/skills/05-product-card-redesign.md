# Skill 05 — Product Card Redesign

## 1. Purpose

This skill is used to plan and implement YaksuDerma product card improvements.

Product cards are one of the most important UI components in this Shopify theme because YaksuDerma has:

- A large technical product catalog
- Long product names
- Unit-based products
- Multiple product families
- Different price points
- Products that must feel original, trustworthy, and professionally presented

This skill comes after:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
04-homepage-redesign.md
```

Product cards should be planned carefully before collection page redesign, because product cards appear across the store.

Codex must plan before implementation.

Do not edit files unless the user explicitly requests implementation after reviewing the product card plan.

## 2. Required Context Files

Before product card work, Codex must read:

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
```

Codex should use these files to understand:

- Product catalog complexity
- Long product name requirements
- Dynamic Shopify data rules
- Color and design system
- Badge rules
- Price display rules
- Mobile grid requirements
- Content safety boundaries
- Reference site usage rules

## 3. Product Card Goal

Product cards should help customers quickly understand and compare products.

They should feel:

- Clean
- Trustworthy
- Professional
- Retail-friendly
- Easy to scan
- Mobile-friendly
- Premium but accessible
- Not cheap
- Not marketplace-like

Product cards should support:

- Exact product names
- Long technical names
- Dynamic Shopify prices
- Product images
- Product URLs
- Optional badges
- Product family consistency
- Mobile two-column browsing where appropriate

## 4. Product Card Must Not Feel Like

Avoid product cards that feel:

- Cheap
- Crowded
- Discount-first
- Marketplace-like
- Hard to scan
- Too technical
- Too tiny on mobile
- Overloaded with badges
- Overly decorative
- Fake luxury
- Generic Dawn default

## 5. Product Data Rules

Codex must not hardcode:

- Product titles
- Product prices
- Product URLs
- Product images
- Product availability
- Product descriptions
- Product badges unless controlled by data/settings
- Product claims
- Certificate claims

Product cards must use Shopify dynamic data.

Use or preserve:

```text
product.title
product.price
product.featured_image
product.url
product.available
product.compare_at_price
product.vendor, if used
product.metafields, if available and approved
snippets/price.liquid
```

Prices must come from Shopify dynamic product data.

Reference prices in `.ai/catalog-brief.md` are planning context only.

## 6. Product Name Requirements

YaksuDerma product cards must handle long and technical names such as:

```text
Botulax 100 Units
Botulax 200 Units
Botulax 300 Units
Revolax Deep with Lidocaine
Neuramis Deep Lidocaine
J-Cain Cream 10.56% 500g
S-Cain Cream 10.56% 500g
Liporase inj. / Hyaluronidase
Rejuran Healer
Botanic EXO Vegan Skin Booster
```

Product titles should:

- Remain exact
- Remain readable
- Wrap gracefully
- Avoid visual clutter
- Avoid tiny font sizes
- Avoid being cut too aggressively
- Preserve SEO and product clarity

Allowed:

- CSS line clamp if necessary
- Better line-height
- More consistent title spacing
- Mobile-specific adjustments

Avoid:

- Rewriting product names
- Shortening product names manually
- Hiding important unit information
- Turning names into marketing slogans

## 7. Product Image Requirements

Product card images should:

- Look clean and consistent
- Avoid bad cropping
- Support product packaging images
- Use consistent image containers
- Preserve Shopify image logic
- Load efficiently
- Work on mobile

Recommended aspect ratio direction:

```text
1:1 or 4:5
```

Codex should inspect actual product image behavior before choosing.

Avoid:

- Cropping product packaging too tightly
- Stretching images
- Distorting product images
- Tiny product images inside huge cards
- Inconsistent image heights
- Heavy image effects

## 8. Price Display Requirements

Price should be:

- Visible
- Clean
- Calm
- Trustworthy
- Easy to compare
- Not aggressive
- Not suspicious

Use dynamic Shopify price rendering.

Preferred:

- Clear price below title
- Calm charcoal or muted teal text
- Sale/compare-at price handled by Shopify price snippet
- No red-heavy styling unless necessary and subtle

Avoid:

- Oversized red prices
- Flash-sale styling
- Marketplace discount emphasis
- Hardcoded price text
- Fake discount badges
- “Cheapest” language

## 9. Badge System

Product cards may support subtle badges, but only when truthful and data-backed.

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
- Do not show “Bestseller” unless confirmed.
- Do not show “Certified” unless certificate details are provided.
- Do not show regulatory badges unless verified.
- Keep badges subtle.
- Avoid more than 1–2 badges per card.
- Badges should be data-driven or configurable.

Possible data sources:

```text
product.tags
product.metafields.custom.badges
product.metafields.custom.product_origin
product.metafields.custom.professional_use_note
theme editor settings
```

## 10. Product Card Content Hierarchy

Recommended product card hierarchy:

```text
1. Product image
2. Optional badge row
3. Product title
4. Optional short metadata line, only if useful
5. Dynamic price
6. Optional CTA / quick link
```

Optional metadata line examples:

```text
Korean-origin product
Product family: Botulax
Professional product category
```

Do not add metadata unless it is data-backed or configurable.

Avoid:

- Long product descriptions inside cards
- Medical claims inside cards
- Treatment use claims
- Dosage/use instructions
- Too many lines of text

## 11. CTA Rules

Product card CTA can be:

```text
View Product
View Details
Quick View, only if already supported safely
Add to Cart, only if Dawn logic supports it safely
```

Preferred first phase:

```text
View Product
```

or no visible button if card click behavior is clear.

Be careful with `Add to Cart` on cards because product variants may exist.

Avoid:

- Adding quick add if variant logic is not handled safely
- Breaking product form logic
- Adding custom cart JavaScript
- Aggressive CTA copy
- “Buy Now!!!”

## 12. Mobile Product Card Requirements

Mobile is a priority.

Product cards must work in mobile collection grids.

Mobile requirements:

- Product title readable
- Price visible
- Image not cropped badly
- Cards not too narrow
- Badges not overcrowded
- Buttons tappable if shown
- No horizontal overflow
- Good spacing between cards
- Product names wrap gracefully

Mobile grid direction:

```text
Two-column grid is preferred if readable.
One-column layout is acceptable if product cards become too crowded.
```

Codex should inspect actual mobile breakpoints before implementing.

## 13. Accessibility Requirements

Product cards should support:

- Clear link target
- Sufficient text contrast
- Focus states
- Image alt text from Shopify data
- Readable price text
- Tap-friendly targets
- Not relying only on color to communicate sale/badge status

Do not remove existing accessible Dawn behavior without reason.

## 14. Performance Requirements

Product card changes should avoid unnecessary complexity.

Prefer:

- CSS improvements
- Existing Shopify image handling
- Existing Dawn snippets
- Minimal Liquid changes
- No heavy JavaScript
- No external libraries

Avoid:

- Heavy hover effects
- Animation libraries
- Custom image loaders
- Complex JS quick add unless needed
- Duplicated product markup

## 15. Design System Requirements

Product cards must follow `.ai/design-system.md`.

Use:

- White product card background
- Light border
- Subtle radius
- Minimal shadow
- Soft hover state
- Charcoal product title
- Calm price styling
- Optional subtle teal/trust-blue badges
- Consistent internal spacing

Avoid:

- Heavy shadows
- Red/orange discount-first styling
- Neon accents
- Overly glossy effects
- Card designs that clash with YaksuDerma’s calm identity

## 16. Reference Site Usage

Codex may use:

```text
.ai/reference-sites.md
.ai/reference-site-links.md
```

Use references for:

- Product grid clarity
- Long product title layout
- Mobile product card spacing
- Clean beauty e-commerce product cards
- Professional supplier product card organization

Do not copy:

- Exact layout
- Exact text
- Images
- Product claims
- Code
- Brand identity
- Competitor pricing strategy

## 17. Files Likely Involved

Codex must inspect actual repo files.

Likely files:

```text
snippets/card-product.liquid
snippets/price.liquid
assets/component-card.css
assets/component-price.css
assets/base.css
sections/featured-collection.liquid
sections/main-collection-product-grid.liquid
sections/product-recommendations.liquid
templates/collection.json
templates/index.json
```

Do not assume every file exists.

Dawn version may vary.

## 18. What Codex Must Preserve

Codex must preserve:

- Product URL
- Dynamic product title
- Dynamic product image
- Dynamic price snippet
- Compare-at price logic
- Availability logic if present
- Product badge logic if present
- Product card links
- Collection grid compatibility
- Featured collection compatibility
- Search results compatibility
- Product recommendations compatibility

Product card snippets are reused across the store, so changes may have wide impact.

## 19. What Codex Must Not Do

During product card work, Codex must not:

- Hardcode product prices
- Hardcode product names
- Hardcode product URLs
- Hardcode product badges
- Remove dynamic price snippet
- Break product links
- Add unverified badges
- Add medical claims
- Add treatment claims
- Add certificate claims
- Add quick add without safe variant handling
- Rewrite all product card logic at once
- Copy competitor product cards exactly

## 20. Planning Output Format

Before editing files, Codex must output:

```text
# Product Card Redesign Plan — YaksuDerma

## 1. Files Inspected

List product card-related files inspected.

## 2. Current Product Card Structure

Explain how Dawn currently renders product cards.

## 3. Current Problems / Opportunities

Explain what needs improvement for YaksuDerma.

## 4. Product Data Preservation

Explain what data remains dynamic.

## 5. Recommended Product Card Layout

Describe proposed image/title/price/badge/CTA hierarchy.

## 6. Mobile Strategy

Explain mobile grid and card behavior.

## 7. Badge Strategy

Explain if badges should be used and how they should be data-backed.

## 8. Files Likely Affected

List files.

## 9. Risks

List risk levels.

## 10. Implementation Phases

Break into small phases.

## 11. First Safe Implementation Step

Recommend exactly one safe next action.
```

## 21. Implementation Output Format

When implementation is requested, Codex must output:

```text
# Product Card Redesign Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. What Changed

Explain product card markup/style changes.

## 3. Dynamic Data Preserved

Confirm product title, price, image, URL, and availability remain dynamic.

## 4. Design System Alignment

Explain how changes follow `.ai/design-system.md`.

## 5. Mobile Behavior

Explain mobile product card behavior.

## 6. Accessibility

Explain focus/contrast/link behavior.

## 7. Risk Level

Low / Medium / High.

## 8. Shopify Preview Test Steps

List test steps.

## 9. Follow-Up Tasks

Recommend next step.
```

## 22. Suggested Implementation Phases

Product card improvements should be implemented in phases:

```text
Phase 1 — CSS-only readability, spacing, radius, border, hover
Phase 2 — Product title behavior and mobile readability
Phase 3 — Product image container consistency
Phase 4 — Badge foundation, only if data-backed/configurable
Phase 5 — CTA/quick link refinement
Phase 6 — Collection/homepage/search context testing
```

Do not implement all phases at once unless explicitly requested.

## 23. Risk Labels

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

- Product card spacing
- Border radius
- Light border
- Hover state
- Title line-height
- Price spacing

### Medium Risk

- Product image container markup
- Product card title clamp
- Badge rendering changes
- CTA changes

### High Risk

- Quick add logic
- Product form integration
- JavaScript behavior
- Replacing product card snippet entirely

### Do Not Touch Yet

- Checkout
- Cart logic
- Hardcoded product prices
- Unverified badges
- Medical claims

## 24. Example Planning Prompt

Use this prompt with Codex:

```text
Read:

- .ai/catalog-brief.md
- .ai/design-system.md
- .ai/content-rules.md
- .ai/custom-components.md
- .ai/skills/05-product-card-redesign.md

Analyze the current Dawn product card structure.

Focus on:
- Long technical product names
- Dynamic Shopify price
- Product image ratio
- Optional badges
- Mobile two-column readability
- Product card spacing
- Fair-price but not cheap perception
- Avoiding marketplace-like product cards
- Preserving product links and Shopify data

Do not edit files yet.

Output:
1. Files inspected
2. Current product card structure
3. Problems/opportunities
4. Recommended product card design
5. Data that must remain dynamic
6. Files likely affected
7. Mobile risks
8. First safe implementation step
```

## 25. Example Implementation Prompt

Use this prompt after approving the product card plan:

```text
Implement the approved product card redesign in a small, reviewable change.

Read:
- .ai/design-system.md
- .ai/catalog-brief.md
- .ai/content-rules.md
- .ai/skills/05-product-card-redesign.md

Requirements:
- Preserve Shopify product URLs.
- Preserve dynamic product titles.
- Preserve dynamic prices.
- Preserve image logic.
- Preserve availability logic if present.
- Do not hardcode product data.
- Improve long product title readability.
- Improve product image consistency.
- Improve spacing, borders, and hover state.
- Keep mobile grid readable.

Output:
1. Files changed
2. What changed
3. Why it changed
4. How product data remains dynamic
5. Mobile behavior
6. Risk level
7. Shopify preview test steps
```

## 26. Final Reminder

Product cards are reused across homepage, collections, search results, recommendations, and related products.

Main principle:

> Make product cards clean, readable, trustworthy, mobile-friendly, and dynamic — without hardcoding product data or making the catalog feel like a cheap marketplace.
