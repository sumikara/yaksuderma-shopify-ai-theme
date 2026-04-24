# Skill 01 — Clean Dawn Theme Audit

## 1. Purpose

This skill is used to audit the clean Shopify Dawn theme before any redesign or implementation work begins.

Codex must use this skill before making design, CSS, Liquid, section, snippet, template, or UX changes.

The goal is to understand the current Dawn architecture and identify the safest path for transforming it into the YaksuDerma Shopify theme.

This is an audit skill only.

Do not edit files unless the user explicitly requests implementation after the audit.

## 2. Required Context Files

Before starting the audit, Codex must read:

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
.ai/migration-notes.md
.ai/prompt-playbook.md
```

Codex should use these files to understand:

- YaksuDerma’s brand direction
- Product catalog complexity
- Final navigation labels
- Design-system goals
- Custom component needs
- Content safety rules
- Reference site usage rules
- Migration principles

## 3. Audit Goal

The audit should answer:

1. How is the current Dawn theme structured?
2. Which files control homepage, product pages, collection pages, header, footer, product cards, and global styles?
3. Which parts of Dawn are safe to customize first?
4. Which parts are risky and should be preserved carefully?
5. Where should the YaksuDerma design system be applied?
6. What is the safest redesign order?
7. What should Codex avoid touching too early?

## 4. Key Areas to Inspect

Codex should inspect the actual repository before making conclusions.

Focus on:

### Theme Architecture

- `layout/theme.liquid`
- `templates/*.json`
- `sections/*.liquid`
- `snippets/*.liquid`
- `assets/*.css`
- `assets/*.js`
- `config/settings_schema.json`
- `config/settings_data.json`
- `locales/*.json`

### Homepage

Likely files:

```text
templates/index.json
sections/image-banner.liquid
sections/featured-collection.liquid
sections/multicolumn.liquid
sections/rich-text.liquid
sections/*.liquid
```

Audit for:

- Current homepage section flow
- Reusable existing sections
- Whether new custom sections may be needed
- Whether homepage content is editable from Shopify theme editor
- Safe places to add YaksuDerma category showcase, trust bar, and support blocks

### Header and Navigation

Likely files:

```text
sections/header.liquid
snippets/header-drawer.liquid
snippets/header-mega-menu.liquid
snippets/header-dropdown-menu.liquid
assets/component-menu-drawer.css
assets/component-mega-menu.css
```

Audit for:

- Desktop menu behavior
- Mobile drawer behavior
- Search icon
- Cart icon
- Account icon if present
- Dropdown / mega menu support
- Whether final navigation can be managed from Shopify admin

Final visible navigation from `.ai/navigation-brief.md`:

```text
Home
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
About
```

Codex must not replace this with a generic “Shop” navigation unless explicitly requested.

### Product Cards

Likely files:

```text
snippets/card-product.liquid
snippets/price.liquid
assets/component-card.css
assets/component-price.css
```

Audit for:

- Product title rendering
- Dynamic price rendering
- Product image handling
- Product URL handling
- Badge logic
- Vendor/secondary text
- Long product name handling
- Mobile readability

Important:

YaksuDerma has long technical product names such as:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
J-Cain Cream 10.56% 500g
Rejuran Healer
```

Product cards must support long names without looking crowded.

### Collection Pages

Likely files:

```text
templates/collection.json
sections/main-collection-product-grid.liquid
sections/main-collection-banner.liquid
snippets/facets.liquid
assets/component-facets.css
```

Audit for:

- Product grid
- Filtering
- Sorting
- Pagination
- Collection header
- Mobile collection layout
- Product card density
- Whether collection descriptions are shown safely

Must preserve:

- Shopify filtering
- Shopify sorting
- Pagination
- Product URLs
- Dynamic prices
- Collection data

### Product Pages

Likely files:

```text
templates/product.json
sections/main-product.liquid
snippets/product-media-gallery.liquid
snippets/product-variant-picker.liquid
snippets/buy-buttons.liquid
assets/section-main-product.css
```

Audit for:

- Product form
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Product media gallery
- Product description
- Accordions
- App blocks
- Product recommendations
- Metafield support
- Product page extensibility for custom components

Must preserve:

- Product form logic
- Variant logic
- Add-to-cart behavior
- Dynamic checkout buttons
- Selling plan logic if present
- App blocks

### Custom Component Potential

Use `.ai/custom-components.md`.

Audit where these could be added safely:

- Product family comparison table
- Product unit comparison table
- Related products module
- Authenticity / certificate block
- Shipping & availability block
- Wholesale inquiry block
- Before / after visual block, only if verified and approved

Do not implement custom components during audit.

### CSS / Design System

Likely files:

```text
assets/base.css
assets/component-card.css
assets/component-price.css
assets/component-button.css
assets/section-main-product.css
assets/component-menu-drawer.css
assets/component-mega-menu.css
```

Audit for:

- Existing Dawn variables
- Button styling
- Card styling
- Section spacing
- Typography scale
- Color system
- Mobile breakpoints
- CSS duplication risks
- Best place to introduce YaksuDerma design tokens

### JavaScript

Likely files:

```text
assets/global.js
assets/product-form.js
assets/cart-notification.js
assets/cart-drawer.js
assets/facets.js
```

Audit only.

Do not recommend unnecessary JavaScript.

Prefer CSS-first and Shopify-native solutions.

## 5. YaksuDerma-Specific Audit Criteria

Evaluate the clean Dawn theme against YaksuDerma’s needs:

### Brand Fit

Does current Dawn support:

- Clean white space?
- Soft turquoise / aqua / medical blue-green accents?
- Trust blue and warm beige support sections?
- Premium but accessible visual tone?
- Korean-inspired clean beauty mood?
- Professional but retail-friendly product discovery?

### Catalog Fit

Does current Dawn support:

- Large product catalog?
- Long product names?
- Multiple product families?
- Unit-based product names?
- Product family comparison?
- Dynamic price display?
- Collection-first browsing?
- Search-first browsing?

### Navigation Fit

Can Dawn support the final menu:

```text
Home
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
About
```

with optional dropdowns:

```text
Fillers
  Dermal Fillers
  Body Fillers
```

```text
Accessories
  Numbing Creams
  IV Therapy
  Dissolvers
  Clinical Accessories
```

### Trust Fit

Can Dawn support:

- Authenticity sections?
- Certificate information where verified?
- Contact/support blocks?
- Wholesale inquiry path?
- Shipping/availability notes?
- Warm support messaging?

### Mobile Fit

Does Dawn currently support:

- Readable mobile header?
- Clear mobile menu?
- Product card readability?
- Mobile product grid?
- Product page conversion?
- Comparison table potential?

## 6. What Codex Must Not Do During Audit

During this audit, Codex must not:

- Edit files
- Create new sections
- Rewrite CSS
- Change templates
- Change Liquid logic
- Remove Dawn functionality
- Modify checkout
- Remove app blocks
- Hardcode products
- Hardcode prices
- Invent claims
- Add reference site code
- Migrate old theme elements

This skill is for analysis only.

## 7. Required Output Format

Codex must output the audit in this structure:

```text
# Clean Dawn Theme Audit — YaksuDerma

## 1. Files Inspected

List the files inspected and why each matters.

## 2. Current Theme Structure Summary

Explain how homepage, product pages, collection pages, header, footer, product cards, CSS, and JS are currently organized.

## 3. Dawn Strengths for YaksuDerma

List what Dawn already does well for this project.

## 4. Gaps / Redesign Opportunities

List what needs improvement for YaksuDerma.

## 5. Risky Areas

Identify files or logic that must be changed carefully.

## 6. Design System Opportunities

Explain where colors, typography, spacing, buttons, cards, and section rhythm can be improved.

## 7. Product Discovery Opportunities

Explain how navigation, product cards, collection pages, search, and product pages can better support the catalog.

## 8. Custom Component Opportunities

List possible future custom components but do not implement them.

## 9. Files Likely Affected in Future Phases

Group by phase:
- Design system
- Homepage
- Product cards
- Collection page
- Product page
- Mobile pass
- Custom components
- Migration

## 10. Recommended Implementation Order

Give the safest order of work.

## 11. First Safe Next Step

Recommend exactly one next step.
```

## 8. Risk Labels

Use these risk labels:

```text
Low
Medium
High
Do not touch yet
Needs user confirmation
```

Examples:

```text
Low risk:
Changing section spacing or button border radius.

Medium risk:
Changing product card markup.

High risk:
Changing product form logic, cart drawer logic, variant picker, or filtering logic.

Do not touch yet:
Checkout, app blocks, unverified certificate claims, hardcoded product data.
```

## 9. Audit Quality Rules

A good audit should be:

- Specific to the actual repo
- Specific to Dawn
- Specific to YaksuDerma
- Practical
- Prioritized
- Clear about risks
- Clear about next steps
- Free of unnecessary implementation
- Free of generic advice

A poor audit is:

- Generic
- Too broad
- Not file-specific
- Not Shopify-aware
- Not mobile-aware
- Not aware of product/cart/variant risk
- Not aligned with YaksuDerma’s briefs

## 10. Example User Prompt

Use this prompt with Codex:

```text
Read the project context files and .ai/skills/01-theme-audit.md.

Analyze this clean Dawn Shopify theme repository.

Focus on:
- Theme architecture
- Homepage structure
- Header and navigation files
- Collection page structure
- Product page structure
- Product card/snippet structure
- Main CSS files
- Theme settings
- Section reuse
- Snippets
- Mobile layout foundations
- Product/cart/variant logic that must not be broken
- Areas where YaksuDerma’s design system can be safely applied

Do not edit files.

Produce a baseline audit with:

1. Files inspected
2. Theme structure summary
3. Important Dawn files and what they control
4. Redesign opportunities
5. Risky areas not to touch carelessly
6. Files likely affected in future phases
7. Recommended implementation order
8. First safe next step
```

## 11. Final Reminder

This skill is the foundation for the entire project.

Main principle:

> Understand the clean Dawn architecture before redesigning anything. Audit first, plan second, implement only after approval.
