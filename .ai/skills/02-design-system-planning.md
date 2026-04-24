# Skill 02 — Design System Planning

## 1. Purpose

This skill is used to create a safe, structured design-system implementation plan for the YaksuDerma Shopify Dawn-based theme.

This skill comes after:

```text
01-theme-audit.md
```

Codex must use this skill before making CSS, typography, button, color, spacing, card, homepage, collection, or product page design changes.

This is a planning skill only.

Do not edit files unless the user explicitly requests implementation after reviewing the plan.

## 2. Required Context Files

Before starting design-system planning, Codex must read:

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
.ai/skills/01-theme-audit.md
```

Codex should use these files to understand:

- YaksuDerma’s brand direction
- Final color direction
- Product catalog complexity
- Navigation structure
- Product card requirements
- Mobile-first requirements
- Content safety rules
- Custom component requirements
- External reference usage rules

## 3. Design System Planning Goal

The goal is to translate YaksuDerma’s brand and UX requirements into a practical Shopify Dawn implementation plan.

Codex should identify:

1. Which design foundations should be changed first
2. Which Dawn CSS variables or settings should be preserved
3. Where new design tokens should live
4. How colors should be implemented
5. How typography should be improved
6. How spacing should be standardized
7. How buttons should be improved
8. How cards should be improved
9. How mobile behavior should be protected
10. Which changes are low-risk vs high-risk
11. What should be implemented first

## 4. YaksuDerma Design Direction

The design should feel:

- Clean
- Modern
- Trustworthy
- Korean-inspired
- Water-inspired
- Soft clinical
- Retail-friendly
- Fair-price but premium
- Warm and helpful
- Organized for technical products
- Mobile-first

The design should not feel:

- Cheap
- Aggressive
- Overdesigned
- Cold
- Crowded
- Marketplace-like
- Medical-claim-heavy
- Generic Dawn default
- Like a cold B2B distributor portal

## 5. Color Planning

Codex must plan around the approved color direction in `.ai/design-system.md`.

Core direction:

```text
Soft turquoise
Aqua
Muted medical blue-green
Trust blue
Warm sand / soft beige
Clean neutrals
```

Color goals:

1. Trust
2. Authenticity
3. Warm helpfulness
4. Product clarity
5. Fair-price but not cheap perception

Codex should identify:

- Existing Dawn color settings
- Existing CSS variables
- Where custom color tokens should be added
- Which elements should use teal/aqua
- Which elements should use trust blue
- Which elements should use warm beige
- Which elements should remain neutral
- Which color changes are safest first

Codex must avoid:

- Neon turquoise
- Saturated blue
- Heavy black sections
- Aggressive red sale labels
- Strong orange CTA buttons
- Random gradients
- Too many competing colors
- Marketplace-style discount colors

## 6. Typography Planning

Codex must plan typography improvements that support:

- Long technical product names
- Retail-friendly readability
- Premium but accessible visual tone
- Mobile readability
- Clear hierarchy

Codex should inspect:

```text
assets/base.css
theme settings
typography variables
product card title styles
collection heading styles
homepage heading styles
product page heading styles
```

Codex should plan:

- Heading hierarchy
- Body text readability
- Product title readability
- Card title line-height
- Mobile font sizes
- Button typography
- Badge typography
- Section heading consistency

Avoid:

- Too many font sizes
- Too many font weights
- Overly decorative fonts
- Tiny mobile text
- Product card titles that become unreadable
- Overly luxury typography that hurts clarity

## 7. Spacing Planning

Codex must plan spacing improvements that make the store feel calm and premium.

Codex should inspect:

- Section padding
- Product grid gaps
- Product card internal spacing
- Header height
- Footer spacing
- Homepage section rhythm
- Mobile spacing
- Product page spacing
- Collection page spacing

Codex should plan consistent spacing tokens or conventions based on `.ai/design-system.md`.

Avoid:

- Random margins
- Overcrowded product grids
- Huge empty spaces on mobile
- Desktop-first spacing squeezed into mobile
- Section rhythm inconsistency

## 8. Button Planning

Codex must plan a button system.

Button types:

```text
Primary CTA
Secondary CTA
Text link
Product card link/button
Add-to-cart button
Support/Contact CTA
Wholesale inquiry CTA
```

Button design should feel:

- Clear
- Calm
- Premium
- Tap-friendly
- Not aggressive
- Not marketplace-like

Codex should plan:

- Button colors
- Border radius
- Padding
- Hover states
- Focus states
- Mobile tap size
- Add-to-cart button treatment
- CTA hierarchy

Avoid:

- Red/orange aggressive CTAs
- Too many button colors
- Tiny buttons
- Hard-to-see secondary buttons
- Inconsistent button radius

## 9. Product Card Planning

Product cards are critical.

YaksuDerma products include long technical names such as:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
J-Cain Cream 10.56% 500g
Rejuran Healer
```

Product card planning must consider:

- Product title wrapping
- Dynamic Shopify price display
- Product image ratio
- Optional badges
- Mobile two-column grid
- Clean borders
- Soft hover states
- Fair-price but not cheap perception
- Product-family consistency
- No hardcoded product data

Codex should identify:

- Current product card files
- Current price snippet
- Current image handling
- Current title behavior
- Which changes should happen in product card phase vs design foundation phase

Do not redesign product cards fully in this planning phase.

## 10. Collection Page Planning

Codex should plan how the design system supports collection pages.

Collection pages must preserve:

- Shopify filtering
- Shopify sorting
- Pagination
- Product URLs
- Dynamic product prices
- Collection data

Design-system planning should consider:

- Collection header style
- Product grid spacing
- Filter/sidebar/mobile filter appearance
- Product card consistency
- Category title mapping

Navigation label to page title mapping:

```text
Toxins → Botulinum Toxins
Fillers → Dermal & Body Fillers
Skin Boosters → Skin Boosters & Exosomes
Fat Dissolvers → Mesotherapy & Contouring
Collagen Stimulators → Collagen Stimulators
Accessories → Clinical Accessories & IV Therapy
```

## 11. Product Page Planning

Codex should plan how the design system supports product pages.

Product pages must preserve:

- Product form logic
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Selling plan logic if present
- App blocks
- Shopify product data

Design-system planning should consider:

- Product title hierarchy
- Product media spacing
- Price visibility
- Add-to-cart button style
- Accordion style
- Support/authenticity block style
- Related products style
- Product family comparison table style
- Mobile product page layout

Do not modify product page logic in this planning phase.

## 12. Custom Component Planning

Use `.ai/custom-components.md`.

Design system should support future components such as:

- Product family comparison tables
- Unit comparison tables
- Related products
- Authenticity / certificate blocks
- Product page accordions
- Wholesale inquiry blocks
- Before / after visual modules, only if verified and approved

Planning should define general styling principles for these components:

- Light borders
- Clean table headers
- Mobile stacked cards if needed
- Dynamic Shopify data
- Editable section settings or metafields
- No hardcoded prices
- No medical claims

## 13. Reference Site Usage

Codex may use `.ai/reference-sites.md` and `.ai/reference-site-links.md`.

Use references only for:

- General UX principles
- Product grid clarity
- Mobile layout inspiration
- Trust-section placement
- Homepage section rhythm
- Product page information hierarchy

Do not copy:

- Exact layout
- Exact text
- Images
- Code
- Claims
- Brand identity
- Medical/regulatory language

## 14. Files to Inspect

Codex should inspect actual repo files before planning.

Likely files:

```text
assets/base.css
assets/component-card.css
assets/component-price.css
assets/component-button.css
assets/section-main-product.css
assets/component-menu-drawer.css
assets/component-mega-menu.css
sections/header.liquid
sections/footer.liquid
sections/image-banner.liquid
sections/featured-collection.liquid
sections/main-product.liquid
sections/main-collection-product-grid.liquid
snippets/card-product.liquid
snippets/price.liquid
config/settings_schema.json
templates/index.json
templates/collection.json
templates/product.json
```

Codex must verify actual file names because Dawn versions may vary.

## 15. Planning Risk Levels

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

- Adding color tokens
- Adjusting section spacing
- Improving border radius
- Light button styling
- Typography refinements

### Medium Risk

- Product card markup adjustments
- Header layout spacing
- Collection grid layout changes
- Custom section additions

### High Risk

- Product form logic
- Variant picker logic
- Cart drawer logic
- Filtering/sorting logic
- JavaScript behavior

### Do Not Touch Yet

- Checkout
- App blocks
- Hardcoded product prices
- Unverified certificates
- Medical claims
- Before/after claims

## 16. What Codex Must Not Do During Planning

During this planning task, Codex must not:

- Edit files
- Create CSS
- Create Liquid sections
- Rewrite templates
- Change product cards
- Change product pages
- Modify navigation
- Add custom components
- Migrate old theme elements
- Hardcode products
- Hardcode prices
- Add claims
- Copy reference sites

This is a planning skill only.

## 17. Required Output Format

Codex must output the plan in this structure:

```text
# Design System Planning — YaksuDerma

## 1. Files Inspected

List the files inspected and why they matter.

## 2. Current Design Foundation Summary

Explain current Dawn colors, typography, spacing, buttons, cards, layout patterns, and theme settings.

## 3. YaksuDerma Design Gaps

Explain where Dawn does not yet match YaksuDerma.

## 4. Recommended Design Tokens

Suggest color, spacing, radius, shadow, and typography token strategy.

## 5. Typography Plan

Explain heading, body, product title, badge, and button typography changes.

## 6. Color Plan

Explain where to use turquoise/aqua, medical blue-green, trust blue, warm beige, and neutrals.

## 7. Spacing and Layout Plan

Explain section rhythm, product grid spacing, card spacing, mobile spacing.

## 8. Button Plan

Explain primary, secondary, text link, add-to-cart, and support CTA styles.

## 9. Product Card Foundation Plan

Explain foundation changes needed before full card redesign.

## 10. Collection/Product Page Foundation Plan

Explain shared layout foundations.

## 11. Custom Component Styling Plan

Explain how comparison tables, accordions, trust blocks, and related products should look.

## 12. Risk Assessment

List low, medium, high, and do-not-touch areas.

## 13. Implementation Phases

Break into small phases.

## 14. First Safe Implementation Step

Recommend exactly one implementation step.
```

## 18. Recommended Implementation Phases

Codex should propose phases similar to this:

```text
Phase 1 — Design tokens and global foundations
Phase 2 — Typography and section spacing
Phase 3 — Buttons and CTA hierarchy
Phase 4 — Product card foundation
Phase 5 — Header/footer visual polish
Phase 6 — Collection/product shared layout foundation
Phase 7 — Custom component styling support
```

Do not implement all phases at once.

## 19. Example User Prompt

Use this prompt with Codex:

```text
Read:

- .ai/codex-instructions.md
- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/navigation-brief.md
- .ai/design-system.md
- .ai/custom-components.md
- .ai/content-rules.md
- .ai/reference-sites.md
- .ai/reference-site-links.md
- .ai/skills/02-design-system-planning.md

Analyze the clean Dawn theme and create a premium design-system implementation plan for YaksuDerma.

Do not edit files yet.

The direction is:
- Modern
- Clean
- Korean-inspired
- Trustworthy
- Product-first
- Soft turquoise / aqua / medical blue-green
- Trust blue
- Warm sand / beige support sections
- Fair-price but not cheap
- Mobile-first
- Suitable for long technical product names

Identify:
1. Which CSS files should be changed
2. Which Dawn variables/settings should be preserved
3. Which design tokens should be added or adapted
4. How buttons should be updated
5. How product cards should be updated
6. How section spacing should be improved
7. How mobile layout should be protected
8. Risks
9. Recommended first implementation task
```

## 20. Final Reminder

This skill is for planning the design system, not implementing it.

Main principle:

> Plan the visual system carefully before changing CSS or Liquid. The design system must make Dawn feel like YaksuDerma without breaking Shopify functionality.
