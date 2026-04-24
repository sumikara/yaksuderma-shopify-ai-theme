# Skill 08 — Mobile UX Pass

## 1. Purpose

This skill is used to audit, plan, and implement mobile UX improvements for the YaksuDerma Shopify Dawn-based theme.

Mobile is a priority because customers may browse product categories, compare prices, inspect product pages, and contact support from mobile devices.

This skill comes after the first implementation phases for:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
04-homepage-redesign.md
05-product-card-redesign.md
06-collection-page-redesign.md
07-product-page-redesign.md
```

Use this skill after major page foundations are in place.

Codex must audit and plan before implementation.

Do not edit files unless the user explicitly requests implementation after reviewing the mobile UX audit.

## 2. Required Context Files

Before mobile UX work, Codex must read:

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
.ai/skills/08-mobile-ux-pass.md
```

Codex should use these files to understand:

- Mobile-first brand direction
- Final navigation labels
- Product card mobile requirements
- Collection page mobile requirements
- Product page mobile risks
- Custom component mobile behavior
- Content safety rules
- Reference site usage rules

## 3. Mobile UX Goal

Mobile experience should help customers:

1. Understand what YaksuDerma sells quickly.
2. Navigate to key categories easily.
3. Browse long technical product names comfortably.
4. See product images and prices clearly.
5. Use filters/sorting without friction.
6. Understand product pages.
7. Add products to cart safely.
8. Contact support when needed.
9. Browse without feeling the store is crowded or cheap.

Mobile should feel:

- Clean
- Fast
- Trustworthy
- Product-first
- Retail-friendly
- Calm
- Premium but accessible
- Easy to tap
- Easy to scan

## 4. Mobile UX Must Not Feel Like

Avoid mobile experiences that feel:

- Squeezed desktop layout
- Tiny text
- Tiny buttons
- Crowded product grid
- Hidden categories
- Hidden search/cart
- Hard to filter
- Hard to add to cart
- Overloaded with badges
- Horizontally broken
- Slow or animation-heavy
- Marketplace-like

## 5. Key Mobile Areas to Audit

Codex should inspect mobile behavior for:

### Header

- Header height
- Logo size
- Menu icon
- Search access
- Cart access
- Account icon if enabled
- Sticky header behavior if present
- Visual balance
- Tap targets

### Mobile Menu

Final navigation should be available:

```text
Home
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
About
Contact
Wholesale Inquiry
```

Optional nested menu:

```text
Fillers
  Dermal Fillers
  Body Fillers

Accessories
  Numbing Creams
  IV Therapy
  Dissolvers
  Clinical Accessories
```

Mobile menu should be:

- Easy to open
- Easy to close
- Readable
- Not too deeply nested
- Tap-friendly
- Category-first
- Search/cart preserved

### Homepage

Audit:

- Hero readability
- CTA visibility
- Category showcase cards
- Trust/authenticity bar
- Featured collection/product section
- Support block
- Wholesale inquiry block
- Section spacing
- Image cropping
- Text overflow

### Product Cards

Audit:

- Title readability
- Long name wrapping
- Price visibility
- Image ratio
- Badge crowding
- Card spacing
- Tap target size
- Two-column grid readability
- Product link behavior

### Collection Pages

Audit:

- Collection header
- Product grid
- Filter drawer
- Sort dropdown
- Active filters
- Pagination
- Product cards
- Empty state
- Mobile spacing

Must preserve:

- Filtering
- Sorting
- Pagination
- Product URLs
- Dynamic prices

### Product Pages

Audit:

- Product media gallery
- Product title
- Dynamic price
- Variant picker
- Quantity selector
- Add-to-cart button
- Dynamic checkout buttons
- Accordions
- Support/authenticity blocks
- Related products
- Product family comparison tables
- Wholesale inquiry block

Must preserve:

- Product form
- Variant logic
- Add-to-cart
- Dynamic checkout
- App blocks

### Custom Components

Audit mobile behavior for:

- Product family comparison tables
- Related product blocks
- Authenticity/certificate blocks
- Support blocks
- Before/after visual blocks if present
- Accordions
- Wholesale inquiry blocks

## 6. Mobile Typography Rules

Mobile typography should be readable and calm.

Avoid:

- Product titles below readable size
- Long headings that wrap badly
- Dense paragraphs
- Tiny product prices
- Tiny filter labels
- Tiny buttons
- Text over busy images

Recommended mobile text behavior:

- Hero headings: readable, not huge
- Product titles: readable, able to wrap
- Body text: short and scannable
- Buttons: clear and tap-friendly
- Category labels: short and clear

## 7. Mobile Product Card Rules

Product cards must support long technical names.

Examples:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
J-Cain Cream 10.56% 500g
Liporase inj. / Hyaluronidase
```

Mobile product card requirements:

- Product image visible and not distorted
- Product title readable
- Price visible
- Card spacing comfortable
- Optional badges not crowded
- Product links easy to tap
- No horizontal overflow

Preferred grid:

```text
Two-column mobile grid if readable.
One-column layout if long names or images become too crowded.
```

Do not force two columns if readability suffers.

## 8. Mobile Collection Page Rules

Collection mobile UX should support:

- Easy product browsing
- Clear filtering
- Easy sorting
- Readable product cards
- Pagination visibility
- No hidden important controls
- Good spacing

Codex must not:

- Remove filtering
- Remove sorting
- Break pagination
- Hide product prices
- Hardcode product data
- Add heavy custom filtering JS

## 9. Mobile Product Page Rules

Product page mobile UX is high priority.

Mobile product page should provide:

- Product image clarity
- Product title readability
- Dynamic price visibility
- Variant picker usability
- Quantity selector usability
- Add-to-cart clarity
- Safe dynamic checkout behavior
- Product information accordions
- Support/contact access
- Related product access

Codex must not break:

- Product form logic
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- App blocks

## 10. Mobile Add-to-Cart Rules

Add-to-cart should be visible and easy to use.

Allowed improvements:

- Better spacing
- Better button size
- Better contrast
- Better disabled state visibility
- Better mobile placement inside existing product form

Mobile sticky add-to-cart may be proposed but not implemented without explicit approval.

Sticky add-to-cart risks:

- Variant selection conflicts
- Dynamic checkout conflicts
- Covering content
- App block conflicts
- Incorrect product form submission

Do not implement sticky add-to-cart unless requested and planned.

## 11. Mobile Comparison Table Rules

Product family comparison tables should work on mobile.

Preferred mobile behavior:

```text
Desktop: table layout
Mobile: stacked comparison cards
```

Alternative:

```text
Horizontally scrollable table
```

Only use horizontal scrolling if readability remains strong.

Comparison tables must not:

- Break page width
- Create horizontal page overflow
- Use tiny text
- Hardcode prices
- Include medical claim columns
- Include treatment guidance

## 12. Mobile Trust and Support Blocks

Trust/support blocks should be:

- Short
- Readable
- Warm
- Not too tall
- Easy to scan
- Visually calm

Examples of safe content:

```text
Original product focus
Fair pricing
Helpful support
Carefully handled orders
```

Support copy:

```text
Need help choosing a product?
Contact us for product details and availability.
```

Avoid:

- Long paragraphs
- Legal-sounding blocks
- Too many badges/icons
- Medical claims
- Shipping overpromises

## 13. Mobile Header and Navigation Rules

Mobile header must preserve:

- Menu icon
- Logo / brand name
- Search
- Cart
- Account icon if enabled

Do not remove search or cart.

Navigation should prioritize categories:

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

Contact and Wholesale Inquiry may appear lower in mobile drawer.

## 14. Mobile Image Rules

Images should:

- Avoid bad cropping
- Load efficiently
- Maintain product clarity
- Not cover text
- Not create layout jumps
- Not create horizontal overflow

Hero images:

- Avoid busy backgrounds behind text.
- Use overlay only if text remains readable.
- On mobile, consider stacking text and image.

Product images:

- Keep packaging visible.
- Maintain consistent card image containers.

## 15. Accessibility Rules

Mobile UX must support:

- Tap-friendly buttons
- Sufficient contrast
- Readable text
- Visible focus states
- Accessible menu behavior
- Accessible accordion behavior
- Clear links
- Not relying only on color
- No tiny interactive controls

Recommended tap target:

```text
At least 44px height/width where feasible.
```

## 16. Performance Rules

Mobile performance matters.

Prefer:

- CSS-first solutions
- Minimal JavaScript
- Shopify-native functionality
- Optimized images
- No heavy sliders
- No unnecessary animations
- No external animation libraries

Avoid:

- Heavy carousels
- Auto-playing sliders
- Large JS libraries
- Complex scroll effects
- Animation-heavy product cards
- Infinite scroll unless explicitly requested

## 17. Files Likely Involved

Codex must inspect actual repo files.

Likely files:

```text
assets/base.css
assets/component-card.css
assets/component-menu-drawer.css
assets/component-mega-menu.css
assets/component-facets.css
assets/section-main-product.css
assets/component-accordion.css
assets/component-price.css
sections/header.liquid
sections/footer.liquid
sections/main-product.liquid
sections/main-collection-product-grid.liquid
sections/image-banner.liquid
sections/featured-collection.liquid
snippets/header-drawer.liquid
snippets/card-product.liquid
snippets/price.liquid
snippets/facets.liquid
templates/index.json
templates/collection.json
templates/product.json
assets/global.js
assets/product-form.js
```

Do not assume every file exists.

Dawn version may vary.

## 18. What Codex Must Preserve

Codex must preserve:

- Shopify product form
- Variant picker
- Add-to-cart
- Dynamic checkout
- Cart
- Search
- Filters
- Sorting
- Pagination
- Product URLs
- Dynamic prices
- App blocks
- Mobile drawer behavior unless explicitly changing it
- Theme editor compatibility

## 19. What Codex Must Not Do

During mobile UX work, Codex must not:

- Remove search
- Remove cart
- Break mobile drawer
- Break product form
- Break variant picker
- Break add-to-cart
- Break filters/sorting
- Break pagination
- Hardcode product prices
- Hardcode product data
- Add medical claims
- Add heavy JavaScript
- Add auto-moving sliders
- Implement sticky add-to-cart without approval
- Copy competitor mobile designs exactly

## 20. Mobile UX Audit Output Format

Before editing files, Codex must output:

```text
# Mobile UX Audit — YaksuDerma

## 1. Files Inspected

List mobile-related files inspected.

## 2. Mobile Header and Menu

Findings and issues.

## 3. Mobile Homepage

Findings and issues.

## 4. Mobile Product Cards

Findings and issues.

## 5. Mobile Collection Pages

Findings and issues.

## 6. Mobile Product Pages

Findings and issues.

## 7. Mobile Custom Components

Findings and issues.

## 8. Accessibility Issues

Findings and issues.

## 9. Performance Risks

Findings and issues.

## 10. Prioritized Fix List

Use severity:
- Critical
- High
- Medium
- Low

## 11. Files Likely Affected

List files.

## 12. First Safe Mobile Fix

Recommend exactly one first fix.
```

## 21. Mobile UX Implementation Output Format

When implementation is requested, Codex must output:

```text
# Mobile UX Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. Mobile Fixes Made

Explain changes by area:
- Header/menu
- Homepage
- Product cards
- Collection page
- Product page
- Custom components

## 3. Desktop Impact

Confirm whether desktop layout changed.

## 4. Shopify Logic Preserved

Confirm:
- Product form
- Variant picker
- Add-to-cart
- Cart
- Search
- Filters
- Sorting
- Pagination
- App blocks

## 5. Accessibility

Explain improvements.

## 6. Performance

Explain whether JS/images/animations were affected.

## 7. Risk Level

Low / Medium / High.

## 8. Shopify Preview Test Steps

List mobile preview checks.

## 9. Follow-Up Tasks

Recommend next step.
```

## 22. Suggested Implementation Phases

Mobile UX fixes should be implemented in phases:

```text
Phase 1 — Header/mobile menu readability
Phase 2 — Homepage mobile section spacing
Phase 3 — Product card mobile readability
Phase 4 — Collection grid + filter/sort mobile polish
Phase 5 — Product page mobile hierarchy
Phase 6 — Custom component mobile behavior
Phase 7 — Accessibility and tap target polish
Phase 8 — Theme check / validation
```

Do not implement all phases at once.

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

- Mobile spacing
- Font-size adjustments
- Button tap target improvements
- Product card title line-height
- Footer spacing

### Medium Risk

- Mobile grid column changes
- Header drawer styling
- Facet/filter mobile styling
- Product page layout stacking

### High Risk

- Product form behavior
- Variant picker JS
- Cart drawer JS
- Sticky add-to-cart
- Search drawer logic
- Filter JS behavior

### Do Not Touch Yet

- Checkout
- App blocks
- Hardcoded prices
- Medical claims
- Unverified before/after sections

## 24. Example Mobile Audit Prompt

Use this prompt with Codex:

```text
Read:

- .ai/navigation-brief.md
- .ai/design-system.md
- .ai/custom-components.md
- .ai/skills/08-mobile-ux-pass.md

Perform a mobile UX audit of the current theme.

Focus on:
- Header height
- Mobile menu
- Search access
- Cart access
- Hero readability
- Category cards
- Product cards
- Collection grid
- Product page
- Add-to-cart visibility
- Button tap size
- Product comparison tables
- Accordions
- Footer readability
- Image cropping
- Text overflow

Do not edit files yet.

Output:
1. Mobile issues found
2. Severity level
3. Files likely affected
4. Recommended fixes
5. Risks
6. First safe mobile fix
```

## 25. Example Mobile Implementation Prompt

Use this prompt after approving the mobile audit:

```text
Implement the approved first mobile UX fixes.

Requirements:
- Keep desktop layout unchanged unless necessary.
- Preserve Shopify functionality.
- Improve mobile readability.
- Improve tap targets.
- Fix product card/mobile grid issues.
- Fix header/mobile menu issues if included in approved plan.
- Fix comparison table mobile behavior if included in approved plan.
- Avoid large unrelated redesign changes.

Output:
1. Files changed
2. Mobile fixes made
3. Desktop impact
4. Risk level
5. Shopify preview test steps
```

## 26. Final Reminder

Mobile UX is not a polish-only step. It is essential for product discovery, trust, and conversion.

Main principle:

> Make YaksuDerma easy to browse, compare, trust, and contact on mobile — without breaking Shopify product, cart, search, filter, or variant logic.
