# Prompt Playbook — YaksuDerma Shopify AI Theme

## 1. Purpose

This file contains reusable Codex prompts for the YaksuDerma Shopify theme redesign project.

Use this file to guide Codex through a structured, safe, step-by-step Shopify theme development workflow.

This playbook is designed for:

- Clean Dawn baseline audit
- Design system planning
- CSS/design implementation
- Homepage redesign
- Product card redesign
- Collection page redesign
- Product page redesign
- Custom product components
- Mobile UX pass
- Theme validation
- Existing theme migration

Codex should not work randomly. It should follow this playbook, read the relevant `.ai` files, produce a plan first, and only implement after explicit approval.

## 2. Core Working Rule

Default workflow:

```text
Read context → inspect files → produce plan → wait for approval → implement small change → explain changed files → provide test steps
```

Do not ask Codex to redesign the whole store in one prompt.

Do not ask Codex to edit too many unrelated files at once.

Do not let Codex hardcode product data, prices, certificates, claims, or navigation logic unless explicitly approved.

## 3. Required Context Files

Before any meaningful design or code task, Codex should read:

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
```

For task-specific work, Codex should also read the relevant file under:

```text
.ai/skills/
```

Note:

- Custom product components are guided by `.ai/custom-components.md` and the relevant product-page/custom-component prompts in this playbook.
- There is no separate numbered skill file for custom product components.

## 4. Project Priorities

Codex should follow this project order unless explicitly instructed otherwise:

1. Audit the clean Dawn theme.
2. Create a premium design system plan.
3. Implement design foundations: colors, typography, spacing, buttons, cards.
4. Redesign homepage section hierarchy.
5. Redesign product cards.
6. Redesign collection pages and product grids.
7. Redesign product pages carefully.
8. Add custom product components only when needed.
9. Run mobile UX pass.
10. Run theme check / validation pass.
11. Migrate useful elements from old Shopify theme only after the new design system is stable.

## 5. Non-Negotiable Technical Rules

Codex must preserve:

- Shopify product form logic
- Variant picker logic
- Quantity selector logic
- Add-to-cart behavior
- Cart page / cart drawer logic
- Search logic
- Collection filtering
- Collection sorting
- Pagination
- Dynamic checkout buttons
- App blocks
- Theme editor compatibility

Codex must not:

- Modify checkout
- Remove app blocks
- Hardcode product prices
- Hardcode product availability
- Hardcode product URLs
- Hardcode product data unless explicitly requested
- Invent medical claims
- Invent certificate or regulatory claims
- Rewrite the entire theme at once
- Make large unrelated changes in one task
- Add unnecessary JavaScript
- Copy external reference sites exactly

## 6. Branch Naming Rules

Use a new branch for each meaningful task.

Suggested branches:

```text
feature/theme-audit
feature/design-system-plan
feature/design-system-foundation
feature/homepage-redesign
feature/product-card-redesign
feature/collection-page-redesign
feature/product-page-redesign
feature/custom-product-components
feature/mobile-ux-pass
feature/theme-check-fixes
feature/existing-theme-migration
```

Keep changes small and reviewable.

## 7. Master Context Prompt

Use this prompt at the beginning of a new Codex session.

```text
You are working on my Shopify Dawn-based theme repository for YaksuDerma.

Before doing anything, read:

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
- .ai/migration-notes.md
- the relevant file under .ai/skills/

Project goal:
Transform clean Dawn into a modern, premium, mobile-first, conversion-focused Shopify storefront for YaksuDerma.

Brand direction:
YaksuDerma is a Korean-origin aesthetics e-commerce store. It should feel clean, trustworthy, product-first, warm, fair-price, retail-friendly, and professional. The visual system should use soft turquoise, aqua, muted medical blue-green, trust blue, warm sand/beige, and clean neutrals.

Navigation direction:
Use the final visible header navigation from .ai/navigation-brief.md:

Home
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
About

Important:
Do not edit files immediately unless I explicitly ask you to implement changes.
First inspect the relevant theme files and produce a plan.

Technical rules:
- Work on a new branch.
- Preserve Shopify product, cart, variant, search, filtering, sorting, pagination, and checkout-related logic.
- Do not modify checkout.
- Do not remove app blocks.
- Do not hardcode product prices or product data unless explicitly requested.
- Prefer reusable sections, snippets, blocks, metafields, dynamic sources, and theme settings.
- Keep sections editable in Shopify theme editor where possible.
- Keep changes small and reviewable.
- Explain every changed file.
- Run theme check if available, or explain manual validation steps if not.

Output format:
1. Files inspected
2. Current structure summary
3. Key problems or opportunities
4. Recommended plan
5. Files likely affected
6. Risks
7. Next safe implementation step
```

## 8. Prompt 1 — Clean Dawn Theme Audit

Use this before any redesign or CSS changes.

Relevant skill file:

```text
.ai/skills/01-theme-audit.md
```

Prompt:

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

Expected outcome:

```text
Audit only. No code changes.
```

## 9. Prompt 2 — Design System Planning

Use after the clean Dawn audit.

Relevant skill file:

```text
.ai/skills/02-design-system-planning.md
```

Prompt:

```text
Read:

- .ai/codex-instructions.md
- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/navigation-brief.md
- .ai/design-system.md
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

Expected outcome:

```text
Design system plan only. No code changes.
```

## 10. Prompt 3 — Design System Foundation Implementation

Use only after the design-system plan is approved.

Relevant skill files:

```text
.ai/skills/02-design-system-planning.md
.ai/skills/03-css-refactor.md
```

Prompt:

```text
Read:

- .ai/design-system.md
- .ai/navigation-brief.md
- .ai/content-rules.md
- .ai/skills/03-css-refactor.md

Implement the first safe design-system foundation changes in small, reviewable commits.

Focus only on:
- Color tokens or CSS variables
- Typography hierarchy foundations
- Button styling foundations
- Section spacing foundations
- Basic card radius/border/shadow rules
- Mobile-safe spacing improvements

Preserve Dawn’s product, cart, variant, search, filtering, sorting, pagination, and app-block logic.

Do not redesign homepage, product page, or collection page yet.

Do not rewrite the entire CSS.

Output:
1. Files changed
2. What changed
3. Why each change was made
4. Risk level
5. How to test in Shopify preview
6. Follow-up tasks
```

Expected outcome:

```text
Small foundation CSS/design changes only.
```

## 11. Prompt 4 — Homepage Redesign Plan

Use after the design system foundation is stable.

Relevant skill file:

```text
.ai/skills/04-homepage-redesign.md
```

Prompt:

```text
Read:

- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/navigation-brief.md
- .ai/design-system.md
- .ai/content-rules.md
- .ai/reference-sites.md
- .ai/reference-site-links.md
- .ai/skills/04-homepage-redesign.md

Create a homepage redesign plan for YaksuDerma.

Do not edit files yet.

Homepage should include:
1. Hero with clear value proposition
2. Trust / authenticity bar
3. Category showcase using:
   - Toxins
   - Fillers
   - Skin Boosters
   - Fat Dissolvers
   - Collagen Stimulators
   - Accessories
4. Featured collection or featured products
5. Why YaksuDerma / fair pricing / authenticity section
6. Customer support section
7. Optional wholesale inquiry section
8. Footer trust links

Rules:
- Do not hardcode product prices.
- Do not hardcode product cards if Shopify dynamic data can be used.
- Prefer sections, blocks, theme settings, product pickers, collection pickers, and dynamic Shopify data.
- Avoid medical claims.
- Keep content editable from Shopify theme editor where possible.
- Keep mobile-first layout.

Output:
1. Current homepage structure
2. Proposed new section flow
3. New sections needed, if any
4. Existing Dawn sections that can be reused
5. Files likely affected
6. Risks
7. Implementation phases
8. First safe implementation step
```

Expected outcome:

```text
Homepage plan only. No code changes.
```

## 12. Prompt 5 — Homepage Redesign Implementation

Use only after approving the homepage plan.

Prompt:

```text
Implement the approved homepage redesign in a small, safe first phase.

Read:
- .ai/skills/04-homepage-redesign.md
- .ai/design-system.md
- .ai/content-rules.md
- .ai/navigation-brief.md

Only implement the first homepage phase:
- Do not rebuild the entire homepage at once.
- Do not hardcode products or prices.
- Use Shopify sections, blocks, and theme settings where possible.
- Preserve Dawn compatibility.
- Keep the homepage mobile-friendly.
- Avoid medical claims.

Output:
1. Files changed
2. New/updated sections
3. Theme editor settings added, if any
4. What the store owner can edit in Shopify
5. Risk level
6. Shopify preview test steps
7. Next homepage phase recommendation
```

Expected outcome:

```text
First homepage implementation phase only.
```

## 13. Prompt 6 — Product Card Redesign Plan

Use before collection page redesign.

Relevant skill file:

```text
.ai/skills/05-product-card-redesign.md
```

Prompt:

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

Expected outcome:

```text
Product card plan only.
```

## 14. Prompt 7 — Product Card Redesign Implementation

Use after approving product card plan.

Prompt:

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

Expected outcome:

```text
Product card changes only.
```

## 15. Prompt 8 — Collection Page Redesign Plan

Use after product cards are stable.

Relevant skill file:

```text
.ai/skills/06-collection-page-redesign.md
```

Prompt:

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

Expected outcome:

```text
Collection page plan only.
```

## 16. Prompt 9 — Collection Page Redesign Implementation

Use after approving collection plan.

Prompt:

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

Expected outcome:

```text
Collection page first phase only.
```

## 17. Prompt 10 — Product Page Redesign Plan

Use only after product cards and collection page are stable.

Relevant skill file:

```text
.ai/skills/07-product-page-redesign.md
```

Prompt:

```text
Read:

- .ai/catalog-brief.md
- .ai/design-system.md
- .ai/custom-components.md
- .ai/content-rules.md
- .ai/reference-sites.md
- .ai/reference-site-links.md
- .ai/skills/07-product-page-redesign.md

Analyze the current Dawn product page.

Focus on:
- Product media gallery
- Product title
- Dynamic price
- Variant picker
- Quantity selector
- Add-to-cart button
- Dynamic checkout buttons
- Product description
- Product accordions
- Support / availability note
- Authenticity block
- Related products
- Product family comparison table potential
- Mobile product page layout

Do not edit files yet.

Must preserve:
- Product form logic
- Variant logic
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Selling plan logic if present
- App blocks
- Shopify product data

Output:
1. Files inspected
2. Current product page structure
3. Risky areas
4. Recommended product page layout
5. Custom components that may be useful
6. Data source recommendations
7. Files likely affected
8. First safe implementation step
```

Expected outcome:

```text
Product page plan only.
```

## 18. Prompt 11 — Product Page Redesign Implementation

Use only after approving product page plan.

Prompt:

```text
Implement the approved first phase of the product page redesign.

Read:
- .ai/skills/07-product-page-redesign.md
- .ai/custom-components.md
- .ai/content-rules.md
- .ai/design-system.md

Requirements:
- Preserve Shopify product form logic.
- Preserve variant picker.
- Preserve quantity selector.
- Preserve add-to-cart.
- Preserve dynamic checkout buttons.
- Preserve app blocks.
- Preserve product data.
- Do not hardcode prices.
- Do not invent product claims.
- Improve product information hierarchy.
- Add only safe, editable support/authenticity/availability content if approved.

Output:
1. Files changed
2. What changed
3. Shopify logic preserved
4. Risk level
5. Mobile behavior
6. How to test product page in Shopify preview
7. Follow-up tasks
```

Expected outcome:

```text
Product page first phase only.
```

## 19. Prompt 12 — Custom Product Components Plan

Use when adding comparison tables, product family tables, before/after modules, certificate blocks, or related product modules.

Relevant file:

```text
.ai/custom-components.md
```

Prompt:

```text
Read:

- .ai/custom-components.md
- .ai/catalog-brief.md
- .ai/content-rules.md
- .ai/design-system.md
- .ai/skills/07-product-page-redesign.md

I want to add a custom product component.

Component type:
[Replace with one: product family comparison table / related products / authenticity block / certificate block / before-after visual block / product accordion / wholesale inquiry block]

Use case:
[Describe the specific use case.]

Important:
Do not implement yet.

First propose the safest implementation plan.

Your plan must include:
1. Component purpose
2. Best data source
3. Whether metafields are needed
4. Whether theme editor blocks can be used as fallback
5. Files likely affected
6. Mobile layout behavior
7. Content safety risks
8. Shopify functionality risks
9. Recommended implementation approach
10. Test steps
```

Expected outcome:

```text
Custom component plan only.
```

## 20. Prompt 13 — Product Family Comparison Table Implementation

Use when specifically implementing comparison tables such as Botulax 100/200/300 Units.

Prompt:

```text
Implement the approved Product Family Comparison Table component.

Read:
- .ai/custom-components.md
- .ai/catalog-brief.md
- .ai/design-system.md
- .ai/content-rules.md

Requirements:
- Support product families such as Botulax 100/200/300 Units, Re N Tox 100/200 Units, EPTQ S100/S300/S500, or Rejuran I/HB/Healer.
- Do not hardcode prices.
- Use Shopify product data dynamically where possible.
- Prefer product picker blocks or metafields.
- Make the component editable from Shopify theme editor if feasible.
- Desktop may use table layout.
- Mobile should use stacked cards or a readable responsive table.
- Do not add medical claims.
- Do not add treatment instructions.

Output:
1. Files changed
2. Data source used
3. How store owner edits the table
4. How prices remain dynamic
5. Mobile behavior
6. Risk level
7. Shopify preview test steps
```

Expected outcome:

```text
One custom comparison component only.
```

## 21. Prompt 14 — Mobile UX Pass

Use after homepage, product cards, collection page, and product page have initial implementations.

Relevant skill file:

```text
.ai/skills/08-mobile-ux-pass.md
```

Prompt:

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

Expected outcome:

```text
Mobile audit only.
```

## 22. Prompt 15 — Mobile UX Implementation

Use after approving mobile audit.

Prompt:

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

Expected outcome:

```text
First mobile fix batch only.
```

## 23. Prompt 16 — Theme Check / Validation

Use after any implementation batch.

Relevant skill file:

```text
.ai/skills/09-theme-check-fix.md
```

Prompt:

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

Do not make broad redesign changes.

Output:
1. Validation method used
2. Issues found
3. Severity
4. Recommended fixes
5. Files affected
6. Whether implementation is safe
```

Expected outcome:

```text
Validation report, or small fixes only if explicitly requested.
```

## 24. Prompt 17 — Conversion Copywriting

Use when writing homepage text, category copy, trust blocks, support copy, or CTAs.

Relevant skill file:

```text
.ai/skills/10-conversion-copywriting.md
```

Prompt:

```text
Read:

- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/content-rules.md
- .ai/skills/10-conversion-copywriting.md

Create conversion-focused copy for:
[Replace with: homepage hero / trust bar / category cards / support block / product page accordion / wholesale block / collection description]

Rules:
- Keep copy warm, professional, and trust-building.
- Do not invent medical claims.
- Do not invent certificates.
- Do not invent regulatory approvals.
- Do not mention guaranteed results.
- Do not use aggressive sales language.
- Use fair-pricing language without making the brand look cheap.
- Keep copy short and mobile-friendly.

Output:
1. Recommended copy
2. Alternative versions
3. Risk notes
4. Where the copy should be used
```

Expected outcome:

```text
Copy only, unless implementation is explicitly requested.
```

## 25. Prompt 18 — Existing Theme Migration Plan

Use only after the new Dawn-based design system is stable.

Relevant files:

```text
.ai/migration-notes.md
.ai/skills/11-existing-theme-migration.md
```

Prompt:

```text
Read:

- .ai/migration-notes.md
- .ai/skills/11-existing-theme-migration.md
- .ai/codex-instructions.md
- .ai/design-system.md

Compare the current redesigned Dawn theme with the reference old Shopify theme.

Do not copy blindly.

Identify reusable customizations, section settings, page templates, CSS snippets, assets, and layout ideas that should be migrated.

Produce a migration table with:

1. Source file or source area
2. Target file or target area
3. What the old theme contains
4. Whether it should be migrated
5. Reason
6. Risk level
7. Implementation plan
8. Whether it conflicts with the new design system

Do not edit files yet.
```

Expected outcome:

```text
Migration plan only.
```

## 26. Prompt 19 — Existing Theme Migration Implementation

Use only after approving a specific migration item.

Prompt:

```text
Implement only the approved migration item.

Read:
- .ai/migration-notes.md
- .ai/skills/11-existing-theme-migration.md
- .ai/design-system.md

Approved migration item:
[Describe exact item.]

Rules:
- Do not copy old messy CSS blindly.
- Do not override the new design system.
- Do not migrate outdated layout patterns.
- Do not break Shopify product/cart/variant logic.
- Keep changes small and reviewable.
- Explain exactly what was migrated and why.

Output:
1. Files changed
2. What was migrated
3. What was intentionally not migrated
4. Conflicts avoided
5. Risk level
6. Shopify preview test steps
```

Expected outcome:

```text
One migration item only.
```

## 27. Emergency Prompt — Stop and Review

Use when Codex starts changing too much or making risky assumptions.

```text
Stop implementation.

Do not edit more files.

Review your current changes and produce:

1. Files changed so far
2. Why each file was changed
3. Whether any Shopify product/cart/variant/search/filtering logic was affected
4. Whether any product data, prices, claims, or certificates were hardcoded
5. Risks introduced
6. Suggested rollback or cleanup plan

Do not continue until I approve.
```

## 28. Review Prompt — Pull Request Review

Use when Codex creates a PR or set of changes.

```text
Review this PR as a senior Shopify theme developer and UI/UX engineer.

Check against:

- .ai/codex-instructions.md
- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/navigation-brief.md
- .ai/design-system.md
- .ai/custom-components.md
- .ai/content-rules.md

Review for:
1. Shopify logic preservation
2. Product/cart/variant/search/filtering safety
3. Theme editor compatibility
4. Mobile UX
5. Accessibility
6. Performance
7. Design-system consistency
8. Content safety
9. Hardcoded data or prices
10. Overly broad changes

Output:
1. Approve / request changes
2. Critical issues
3. Medium issues
4. Nice-to-have improvements
5. Files needing review
6. Recommended next action
```

## 29. Default Output Format for Codex

Unless a prompt says otherwise, Codex should respond with:

```text
1. Files inspected
2. Current structure summary
3. Key problems or opportunities
4. Recommended plan
5. Files likely affected
6. Risks
7. Next safe implementation step
```

For implementation tasks, Codex should respond with:

```text
1. Files changed
2. What changed
3. Why it changed
4. Shopify logic preserved
5. Risk level
6. How to test in Shopify preview
7. Follow-up tasks
```

## 30. Final Reminder

Codex should act like a careful Shopify theme developer, not a random code generator.

Main principles:

```text
Plan before editing.
Edit small.
Preserve Shopify logic.
Keep data dynamic.
Avoid medical claims.
Keep UI clean and mobile-first.
Use references for inspiration, not copying.
Make every change reviewable.
```
