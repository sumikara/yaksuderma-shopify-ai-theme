# Skill 09 — Theme Check & Validation Fix

## 1. Purpose

This skill is used to validate the YaksuDerma Shopify Dawn-based theme after implementation work.

Use this skill after changes to:

- CSS
- Liquid
- JSON templates
- Sections
- Snippets
- Product cards
- Collection pages
- Product pages
- Mobile UX
- Custom components
- Navigation
- Footer
- Theme settings

The goal is to catch syntax problems, broken Shopify logic, invalid schemas, accessibility issues, mobile risks, and accidental hardcoded content before pushing or publishing the theme.

This skill should be used after every meaningful implementation batch.

## 2. Required Context Files

Before validation, Codex must read:

```text
.ai/codex-instructions.md
.ai/brand-brief.md
.ai/store-brief.md
.ai/catalog-brief.md
.ai/navigation-brief.md
.ai/design-system.md
.ai/custom-components.md
.ai/content-rules.md
.ai/prompt-playbook.md
.ai/skills/09-theme-check-fix.md
```

If validating a specific area, Codex should also read the related skill file.

Examples:

```text
.ai/skills/04-homepage-redesign.md
.ai/skills/05-product-card-redesign.md
.ai/skills/06-collection-page-redesign.md
.ai/skills/07-product-page-redesign.md
.ai/skills/08-mobile-ux-pass.md
```

## 3. Validation Goal

Codex should check whether the theme is still:

- Shopify-compatible
- Liquid-valid
- JSON-valid
- Schema-valid
- Mobile-safe
- Accessible
- Performance-conscious
- Content-safe
- Dynamic-data-safe
- Aligned with YaksuDerma’s design system

The validation pass should identify issues clearly and propose safe fixes.

## 4. Validation Methods

Codex should use the best available validation method.

### If Shopify Theme Check is available

Run theme validation if the environment supports it.

Possible command:

```text
shopify theme check
```

or equivalent environment-specific validation.

### If Theme Check is not available

Perform a manual validation review.

Codex should explain:

```text
Theme Check was not available in this environment, so I performed a manual validation review.
```

Manual validation must still check Liquid, JSON, schemas, Shopify logic, mobile risks, and content safety.

## 5. Liquid Validation Checklist

Check for:

- Liquid syntax errors
- Unclosed tags
- Incorrect `{% if %}`, `{% for %}`, `{% case %}` structures
- Missing `{% endif %}`, `{% endfor %}`, `{% endcase %}`
- Invalid filters
- Invalid object references
- Unsafe assumptions about metafields
- Invalid section/block references
- Broken render/include references
- Missing snippets
- Incorrect variable names
- Logic that may fail when data is blank

Special attention:

- Product form
- Variant picker
- Price snippet
- Product cards
- Collection loops
- Facets/filtering
- Custom components
- Product family tables
- Header/menu snippets

## 6. JSON Template Validation Checklist

Check:

- Valid JSON syntax
- Valid section IDs
- Valid section types
- No trailing commas
- No broken references to deleted sections
- Proper template structure
- Valid block configuration
- No invalid nesting
- No hardcoded product/collection data unless explicitly approved

Likely files:

```text
templates/index.json
templates/product.json
templates/collection.json
templates/page.json
templates/*.json
```

## 7. Section Schema Validation Checklist

Check section schemas for:

- Valid JSON inside `{% schema %}`
- Valid setting types
- Valid block types
- Required labels
- No duplicate IDs inside same schema
- Reasonable defaults
- Theme editor usability
- No unsafe hardcoded claims
- Product/collection picker settings where needed
- Image picker settings where needed
- Text fields for editable content
- Safe default copy

Likely files:

```text
sections/*.liquid
```

## 8. CSS Validation Checklist

Check CSS for:

- Syntax errors
- Invalid selectors
- Overly broad selectors
- Duplicate conflicting rules
- Excessive `!important`
- Broken media queries
- Horizontal overflow risk
- Mobile spacing issues
- Poor contrast risk
- Product card layout breaks
- Collection grid layout breaks
- Product page mobile layout breaks
- Custom component table overflow
- Header/menu layout issues

CSS should remain:

- Maintainable
- Scoped where possible
- Aligned with `.ai/design-system.md`
- Not copied from external sites
- Not overly aggressive

## 9. JavaScript Validation Checklist

Check JavaScript only if changed or affected.

Codex should avoid unnecessary JS.

Check for:

- Syntax errors
- Console-breaking errors
- Broken event listeners
- Broken product form behavior
- Broken cart drawer behavior
- Broken search behavior
- Broken filters/facets behavior
- Broken variant picker behavior
- Broken mobile menu behavior
- Heavy scripts
- Unnecessary custom JS
- Accessibility issues in interactive components

High-risk files may include:

```text
assets/global.js
assets/product-form.js
assets/cart-drawer.js
assets/cart-notification.js
assets/facets.js
```

Do not modify JavaScript unless needed and explicitly approved.

## 10. Shopify Logic Preservation Checklist

Confirm these still work:

- Product title dynamic rendering
- Product price dynamic rendering
- Product media rendering
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Cart drawer/page
- Search
- Collection filtering
- Collection sorting
- Pagination
- Product recommendations
- App blocks
- Theme editor sections/blocks

High-risk areas:

```text
Product form
Variant picker
Cart drawer
Facets/filtering
Search
Dynamic checkout
App blocks
```

## 11. Dynamic Data Safety Checklist

Confirm Codex did not hardcode:

- Product prices
- Product inventory
- Product URLs
- Product images
- Product names, unless used only as documentation/example text
- Collection data
- Certificate claims
- Regulatory claims
- Availability claims
- Shipping guarantees

Product data should come from Shopify objects such as:

```text
product.title
product.price
product.featured_image
product.url
product.available
collection.products
product.metafields
section.settings
block.settings
```

## 12. Content Safety Checklist

Check for risky or invented content.

Codex must not add:

- Medical claims
- Treatment promises
- Dosage instructions
- Injection instructions
- Regulatory approvals
- Certificate claims unless verified
- Country-specific legal claims
- Safety guarantees
- Guaranteed shipping claims
- Before/after claims
- “Cheapest” claims
- Fake urgency

Safe content should follow:

```text
.ai/content-rules.md
```

## 13. Navigation Validation Checklist

Confirm navigation still follows:

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

Check:

- Header menu not replaced by generic “Shop” unless requested
- Search preserved
- Cart preserved
- Mobile drawer preserved
- Dropdowns work if used
- Menu labels are readable
- Mobile menu is tap-friendly
- Footer links are structured and not overloaded

Navigation should remain Shopify admin/menu compatible where possible.

## 14. Homepage Validation Checklist

Check homepage for:

- Hero readability
- Trust/authenticity bar
- Category showcase
- Featured collection/products dynamic data
- Why YaksuDerma section
- Support block
- Optional wholesale inquiry
- Mobile section rhythm
- No medical claims
- No hardcoded prices
- Theme editor usability

## 15. Product Card Validation Checklist

Check product cards for:

- Dynamic product title
- Dynamic price
- Dynamic image
- Product URL
- Long title wrapping
- Image ratio
- Badge truthfulness
- Mobile readability
- Collection grid compatibility
- Featured collection compatibility
- Search/recommendation compatibility
- No hardcoded prices
- No fake badges

## 16. Collection Page Validation Checklist

Check collection pages for:

- Collection title
- Collection description
- Product grid
- Product cards
- Filters
- Sorting
- Pagination
- Active filters
- Mobile filter drawer
- Dynamic prices
- No broken collection data
- SEO-safe category language
- No medical claims

## 17. Product Page Validation Checklist

Check product pages for:

- Product title
- Dynamic price
- Product media gallery
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Product description
- Accordions
- Related products
- Product comparison components if present
- Authenticity/support blocks
- Mobile layout
- No app block removal
- No product form breakage
- No hardcoded prices
- No medical claims

## 18. Custom Component Validation Checklist

If custom components exist, check:

### Product Family Comparison Tables

- Prices are dynamic
- Product links are dynamic
- Product names are dynamic or selected through product pickers/metafields
- Mobile layout does not break
- No medical claim columns
- No dosage/treatment columns

### Authenticity / Certificate Blocks

- Claims are neutral unless verified
- No invented certificate names
- No invented approvals
- Content is editable where possible

### Before / After Blocks

- Disabled by default unless approved
- No guaranteed result claims
- Images user-provided and verified
- Captions safe
- Mobile layout safe

### Related Products

- Not framed as medical instructions
- Product data dynamic
- No “must use together” wording

## 19. Mobile Validation Checklist

Check mobile for:

- Header height
- Mobile menu readability
- Search access
- Cart access
- Hero text
- Category cards
- Product cards
- Collection grid
- Filters/sorting
- Product page hierarchy
- Add-to-cart visibility
- Button tap size
- Accordions
- Comparison tables
- Footer readability
- No horizontal overflow
- No text overflow
- No image distortion

## 20. Accessibility Validation Checklist

Check:

- Color contrast
- Heading hierarchy
- Link text clarity
- Button focus states
- Keyboard navigation where applicable
- Alt text support
- Form labels
- Accordion behavior
- Tap target size
- Not relying only on color
- Product price readability
- Menu accessibility

## 21. Performance Validation Checklist

Check for:

- Unnecessary JavaScript
- Heavy animations
- Large custom scripts
- Excessive CSS duplication
- Heavy sliders
- Unoptimized image usage
- Layout shifts
- Too many custom components at once
- External libraries added without need

Prefer:

- CSS-first
- Shopify-native
- Minimal JS
- Existing Dawn patterns
- Dynamic Shopify data

## 22. Risk Labels

Use these risk labels:

```text
Low
Medium
High
Critical
Needs user confirmation
```

Examples:

### Low

- Minor CSS issue
- Copy typo
- Spacing inconsistency

### Medium

- Mobile product card issue
- Schema default problem
- Product grid layout issue

### High

- Product form risk
- Variant picker issue
- Filtering/sorting issue
- Cart drawer issue

### Critical

- Theme cannot load
- Liquid syntax error
- JSON template invalid
- Add-to-cart broken
- Product prices hardcoded incorrectly
- Checkout-related modification

## 23. Fix Rules

When fixing issues:

- Fix only the identified issue.
- Do not redesign unrelated sections.
- Do not make broad CSS rewrites.
- Do not introduce new claims.
- Do not change Shopify logic unless necessary and approved.
- Keep fixes small and reviewable.
- Explain every changed file.

If an issue is high-risk, Codex should propose a fix plan before editing.

## 24. Validation Output Format

Codex must output:

```text
# Theme Check & Validation — YaksuDerma

## 1. Validation Method

Theme Check used / Manual validation used.

## 2. Files Inspected

List files inspected.

## 3. Issues Found

Table:

| Issue | File | Severity | Why It Matters | Recommended Fix |
|---|---|---|---|---|

## 4. Shopify Logic Review

Confirm product/cart/variant/search/filtering/sorting/pagination/app-block status.

## 5. Dynamic Data Review

Confirm no product prices/data were hardcoded.

## 6. Content Safety Review

Confirm no medical/regulatory/certificate/shipping claims were invented.

## 7. Mobile Review

Summarize mobile risks.

## 8. Accessibility Review

Summarize accessibility risks.

## 9. Performance Review

Summarize performance risks.

## 10. Recommended Fix Order

Prioritized fix list.

## 11. Safe Next Step

Recommend exactly one next step.
```

## 25. Fix Output Format

When fixes are approved and implemented, Codex must output:

```text
# Theme Check Fix Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. Issues Fixed

List each fixed issue.

## 3. What Was Not Changed

Confirm unrelated code was not changed.

## 4. Shopify Logic Preserved

Confirm product/cart/variant/search/filtering/sorting/pagination/app-block status.

## 5. Risk Level

Low / Medium / High / Critical.

## 6. Test Steps

List Shopify preview tests.

## 7. Follow-Up Tasks

Recommend next step.
```

## 26. Example Validation Prompt

Use this prompt with Codex:

```text
Read .ai/skills/09-theme-check-fix.md.

Run Shopify theme validation if available.

If theme check is not available in the environment, perform a manual validation review.

Check:
- Liquid syntax
- JSON template validity
- Section schema validity
- Translation/key issues
- Broken references
- Product form integrity
- Cart/search/filtering logic
- App block preservation
- Accessibility concerns
- CSS duplication or conflicts
- Mobile layout risks
- Content safety
- Hardcoded product data or prices

Do not make broad redesign changes.

Output:
1. Validation method used
2. Issues found
3. Severity
4. Recommended fixes
5. Files affected
6. Whether implementation is safe
```

## 27. Example Fix Prompt

Use this after approving specific fixes:

```text
Fix only the approved theme validation issues.

Approved issues:
[Paste approved issue list.]

Read:
- .ai/skills/09-theme-check-fix.md
- Relevant skill file for the affected area

Rules:
- Do not redesign unrelated areas.
- Do not modify checkout.
- Do not remove app blocks.
- Do not hardcode product prices.
- Do not add medical or regulatory claims.
- Preserve Shopify product/cart/variant/search/filtering/sorting/pagination logic.
- Explain every changed file.

Output:
1. Files changed
2. Issues fixed
3. Shopify logic preserved
4. Risk level
5. Shopify preview test steps
```

## 28. Final Reminder

Theme validation is a safety gate.

Main principle:

> Validate after every meaningful implementation batch. Fix small, preserve Shopify logic, keep data dynamic, and never introduce risky content while fixing technical issues.
