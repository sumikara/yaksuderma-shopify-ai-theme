# Skill 11 — Existing Theme Migration

## 1. Purpose

This skill is used to review and selectively migrate useful elements from an old Shopify theme into the new YaksuDerma Dawn-based theme.

This skill must be used only after the new theme direction is stable.

Recommended order before using this skill:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
04-homepage-redesign.md
05-product-card-redesign.md
06-collection-page-redesign.md
07-product-page-redesign.md
08-mobile-ux-pass.md
09-theme-check-fix.md
```

Old theme migration must not be used as a shortcut to copy messy old code into the clean Dawn base.

## 2. Required Context Files

Before migration work, Codex must read:

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
.ai/skills/11-existing-theme-migration.md
```

Codex should use these files to understand:

- New YaksuDerma design system
- Final navigation structure
- Product catalog structure
- Content safety rules
- Custom component strategy
- What should and should not be migrated
- Migration risk levels
- Selective migration principles

## 3. Migration Goal

The goal is to identify old theme elements that genuinely strengthen the new YaksuDerma theme.

Migration should preserve the new clean Dawn-based architecture.

Good migration means:

- Useful old assets are reused safely.
- Strong content ideas are adapted.
- Good section ideas are rebuilt cleanly.
- Verified brand material is preserved.
- Messy old CSS is not copied blindly.
- Product/cart/variant logic remains safe.
- The new design system remains the source of truth.

## 4. Old Theme Reference

Current reference theme:

```text
OLD Reference - Dawn - Do Not Publish
```

Possible additional reference themes:

```text
OLD Reference - Horizon - Do Not Publish
OLD Reference - Rise - Do Not Publish
OLD Reference - Sleek - Do Not Publish
```

If multiple old themes are available, Codex should compare them only as references and clearly identify which one each element came from.

## 5. Migration Principle

Do not copy blindly.

Old theme elements should be treated as:

```text
Reference material
```

not as:

```text
Source of truth
```

The new theme source of truth is:

```text
.ai/codex-instructions.md
.ai/brand-brief.md
.ai/store-brief.md
.ai/catalog-brief.md
.ai/navigation-brief.md
.ai/design-system.md
.ai/custom-components.md
.ai/content-rules.md
```

## 6. What Can Be Considered for Migration

Codex may review and selectively migrate:

- Logo assets
- Brand images
- Approved banner images
- Approved product images
- Useful homepage section ideas
- Useful category section ideas
- Existing About page copy
- Existing Contact page copy
- Verified authenticity text
- Verified certificate notes
- Useful support section copy
- Useful wholesale inquiry copy
- Existing collection descriptions if content-safe
- Existing product page structure ideas
- Existing trust section ideas
- Existing footer content ideas
- Existing icons if licensed and appropriate
- Useful theme editor settings
- Useful page templates if compatible

## 7. What Should Usually Not Be Migrated

Avoid migrating:

- Messy old CSS
- Random custom CSS overrides
- Hardcoded product prices
- Hardcoded product cards
- Hardcoded product URLs
- Outdated homepage layout
- Poor mobile layouts
- Broken Liquid snippets
- Old app-specific code unless still needed
- Checkout-related code
- Aggressive sales copy
- Fake urgency copy
- Countdown timers
- Marketplace-style sale visuals
- Unverified medical claims
- Unverified certificate claims
- Unverified regulatory claims
- Before / after content unless verified and approved
- Code that bypasses Shopify product/cart/variant logic
- Code that conflicts with the new design system

## 8. Migration Safety Rules

Before recommending migration, Codex must check:

1. Does this element fit the new YaksuDerma design system?
2. Does it support the current brand direction?
3. Does it preserve Shopify theme editor compatibility?
4. Does it preserve product/cart/variant/search/filtering logic?
5. Does it avoid hardcoded product prices?
6. Does it avoid hardcoded product data?
7. Does it avoid medical, regulatory, or certificate claims?
8. Does it work on mobile?
9. Does it improve the user experience?
10. Is it easier and safer to rebuild the idea cleanly instead of copying?
11. Can it be migrated in a small, reviewable change?

If uncertain, recommend:

```text
Rebuild using new design system
```

instead of copying old code.

## 9. Migration Priority

Use this priority order.

### Priority 1 — Safe Assets

Examples:

- Logo
- Brand images
- Approved product images
- Approved banner images
- Icons if licensed and useful

Migration approach:

- Migrate only if the asset supports the new visual direction.
- Avoid low-quality or off-brand images.
- Avoid images that imply risky medical results.

### Priority 2 — Safe Content

Examples:

- About text
- Contact copy
- Verified authenticity text
- Verified certificate notes
- Existing collection descriptions if compliant
- Existing support copy
- Existing wholesale inquiry copy

Migration approach:

- Review against `.ai/content-rules.md`.
- Rewrite if needed to match YaksuDerma tone.
- Do not migrate risky claims.

### Priority 3 — Useful Layout Ideas

Examples:

- A strong hero concept
- A useful category showcase idea
- A trust bar concept
- A support/contact section idea
- A product page accordion concept
- A footer grouping idea

Migration approach:

- Usually rebuild cleanly using the new design system.
- Do not copy old CSS unless it is clean and compatible.

### Priority 4 — Code Migration

Only migrate code if:

- It is clean
- It is still needed
- It does not conflict with Dawn
- It does not conflict with the new design system
- It does not break Shopify logic
- It is easier than rebuilding
- It can be tested safely

## 10. Migration Decision Labels

Use one of these labels:

```text
Migrate as-is
Migrate with cleanup
Rebuild using new design system
Use as inspiration only
Do not migrate
Needs user confirmation
```

Recommended default for most layout/code items:

```text
Rebuild using new design system
```

## 11. Migration Risk Labels

Use these risk labels:

```text
Low
Medium
High
Do not migrate
Needs user confirmation
```

Examples:

### Low Risk

- Logo asset
- Approved brand image
- Safe About page copy
- Safe footer link idea

### Medium Risk

- Homepage section idea
- Product page accordion idea
- Trust block concept
- Collection description copy

### High Risk

- Old CSS overrides
- Product card code
- Product page Liquid
- Cart-related snippets
- App-specific code

### Do Not Migrate

- Checkout code
- Hardcoded product prices
- Unverified medical claims
- Unverified certificate claims
- Broken Liquid
- Code that conflicts with Dawn logic

## 12. Old Theme Areas to Review

Codex may review these areas:

```text
layout/theme.liquid
templates/index.json
templates/product.json
templates/collection.json
templates/page.json
sections/header.liquid
sections/footer.liquid
sections/image-banner.liquid
sections/featured-collection.liquid
sections/main-product.liquid
sections/main-collection-product-grid.liquid
snippets/card-product.liquid
snippets/price.liquid
assets/base.css
assets/theme.css
assets/custom.css
config/settings_data.json
config/settings_schema.json
assets/*
```

Codex must inspect actual files before making recommendations.

## 13. Specific Migration Checks

### Assets

Check:

- File quality
- Brand fit
- Image dimensions
- Usage rights
- Whether image implies medical results
- Whether image fits the new turquoise/aqua/trust/warm system

### CSS

Check:

- Is CSS clean?
- Is it scoped?
- Does it conflict with Dawn?
- Does it conflict with `.ai/design-system.md`?
- Does it use too many `!important` rules?
- Does it create mobile issues?
- Is it easier to rebuild?

### Liquid

Check:

- Does it preserve Shopify objects?
- Does it hardcode product data?
- Does it affect product/cart/variant logic?
- Does it depend on old app code?
- Does it use valid Liquid?
- Is it reusable?
- Is it theme-editor compatible?

### Copy

Check:

- Does it match YaksuDerma voice?
- Does it include risky medical claims?
- Does it include certificate claims?
- Does it overpromise shipping?
- Does it make the brand sound cheap?
- Should it be rewritten?

### Section Settings

Check:

- Are settings still relevant?
- Can they be recreated cleanly?
- Do they support theme editor usage?
- Do they conflict with the new design system?
- Are they too specific to old design?

## 14. Migration Table Required

When reviewing old theme elements, Codex must produce a table.

Use this format:

| Source Theme | Source Area / File | Old Element | Target Area / File | Migrate? | Reason | Risk Level | Decision | Implementation Plan |
|---|---|---|---|---|---|---|---|---|
| OLD Reference - Dawn | Example: homepage hero | Banner image + headline idea | New homepage hero | Maybe | Image may fit, copy needs review | Medium | Rebuild using new design system | Use image if approved, rewrite copy |
| OLD Reference - Dawn | Example: old CSS override | Button styling | Design system CSS | No | Conflicts with new button system | High | Do not migrate | Ignore old CSS |
| OLD Reference - Dawn | Example: logo asset | Logo image | Theme assets/header | Yes | Brand asset | Low | Migrate with cleanup | Add asset and configure header |

## 15. Migration Analysis Output Format

Before editing files, Codex must output:

```text
# Existing Theme Migration Analysis — YaksuDerma

## 1. Source Theme Reviewed

Name the old theme or source.

## 2. Files / Areas Inspected

List inspected files or areas.

## 3. Migration Candidate Table

Use the required migration table.

## 4. Recommended Items to Migrate

List approved-looking candidates.

## 5. Items to Rebuild Instead of Copy

List items that should be rebuilt cleanly.

## 6. Items Not to Migrate

List risky or incompatible items.

## 7. Content Safety Issues

Flag medical, regulatory, certificate, shipping, or claim risks.

## 8. Design System Conflicts

Explain conflicts with `.ai/design-system.md`.

## 9. Shopify Logic Risks

Flag product/cart/variant/search/filtering/app-block risks.

## 10. Recommended Migration Order

Prioritize safe assets/content first.

## 11. First Safe Migration Item

Recommend exactly one first migration item.
```

## 16. Migration Implementation Output Format

When a specific migration item is approved, Codex must output:

```text
# Existing Theme Migration Implementation — YaksuDerma

## 1. Approved Migration Item

State the exact approved item.

## 2. Files Changed

List changed files.

## 3. What Was Migrated

Explain what moved.

## 4. What Was Rebuilt Instead of Copied

Explain if applicable.

## 5. What Was Intentionally Not Migrated

Explain excluded parts.

## 6. Design System Alignment

Explain how it fits `.ai/design-system.md`.

## 7. Shopify Logic Preserved

Confirm:
- Product form
- Variant picker
- Add-to-cart
- Cart
- Search
- Filtering
- Sorting
- Pagination
- App blocks

## 8. Content Safety

Confirm no risky claims were added.

## 9. Risk Level

Low / Medium / High.

## 10. Shopify Preview Test Steps

List practical checks.

## 11. Follow-Up Tasks

Recommend next step.
```

## 17. What Codex Must Not Do

During migration work, Codex must not:

- Copy old theme wholesale
- Replace the new design system
- Copy messy old CSS blindly
- Copy checkout code
- Copy hardcoded product prices
- Copy hardcoded product cards
- Copy product-specific hardcoded Liquid
- Copy unverified certificate claims
- Copy medical claims
- Copy before/after content unless verified
- Copy old app code without confirming it is still needed
- Break Shopify product/cart/variant/search/filtering logic
- Change unrelated files
- Migrate many unrelated items at once

## 18. Recommended Migration Phases

Use this order:

```text
Phase 1 — Review old theme only
Phase 2 — Migrate safe assets
Phase 3 — Migrate or rewrite safe copy
Phase 4 — Rebuild useful section ideas using new design system
Phase 5 — Review any code migration candidates
Phase 6 — Implement one approved code migration item at a time
Phase 7 — Mobile and theme-check validation
```

Do not skip the review phase.

## 19. Example Migration Analysis Prompt

Use this prompt with Codex:

```text
Read:

- .ai/migration-notes.md
- .ai/skills/11-existing-theme-migration.md
- .ai/codex-instructions.md
- .ai/design-system.md
- .ai/content-rules.md

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

## 20. Example Migration Implementation Prompt

Use this only after approving one migration item:

```text
Implement only the approved migration item.

Read:
- .ai/migration-notes.md
- .ai/skills/11-existing-theme-migration.md
- .ai/design-system.md
- .ai/content-rules.md

Approved migration item:
[Describe exact item.]

Rules:
- Do not copy old messy CSS blindly.
- Do not override the new design system.
- Do not migrate outdated layout patterns.
- Do not break Shopify product/cart/variant/search/filtering logic.
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

## 21. Final Reminder

Existing theme migration is not a shortcut.

Main principle:

> Keep the new Dawn-based YaksuDerma theme clean. Migrate only what strengthens the final store, rebuild useful ideas when safer, and never copy old messy code blindly.
