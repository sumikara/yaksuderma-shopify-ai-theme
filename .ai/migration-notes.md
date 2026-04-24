# Migration Notes — YaksuDerma

## 1. Purpose

This file defines how useful elements from an old Shopify theme should be reviewed and migrated into the new YaksuDerma Dawn-based theme.

The current main development direction is:

```text
Clean Dawn base
→ YaksuDerma design system
→ Homepage / product card / collection / product page redesign
→ Mobile UX pass
→ Theme validation
→ Selective old-theme migration
```

Old theme migration must happen **only after** the new design system is stable.

## 2. Old Theme Reference

Current old theme reference:

```text
OLD Reference - Dawn - Do Not Publish
```

Other possible old/reference themes may include:

```text
OLD Reference - Horizon - Do Not Publish
OLD Reference - Rise - Do Not Publish
OLD Reference - Sleek - Do Not Publish
```

If more old themes are reviewed later, add them here with notes.

## 3. Migration Principle

Do not copy blindly.

Only migrate elements that genuinely improve the new YaksuDerma theme.

The new theme must remain:

- Clean
- Mobile-first
- Premium but accessible
- Shopify-native
- Easy to maintain
- Aligned with the YaksuDerma design system
- Safe from medical-claim risk
- Dynamic through Shopify data where possible

Old theme elements should be treated as **reference material**, not as the source of truth.

## 4. What Can Be Considered for Migration

Codex may review and selectively migrate:

- Logo assets
- Brand images
- Banner images
- Useful section ideas
- Strong homepage layout ideas
- Existing copy that matches content rules
- Existing collection descriptions
- Useful page templates
- Useful product page content structure
- Trust/authenticity section ideas
- Contact or support section ideas
- Existing menu ideas if compatible
- Verified certificate/authenticity content
- Useful icons if licensed and appropriate
- Theme editor settings that are still relevant

## 5. What Should Usually Not Be Migrated

Avoid migrating:

- Messy old CSS
- Random custom CSS overrides
- Hardcoded product prices
- Hardcoded product cards
- Outdated homepage layout
- Poor mobile layouts
- Old section order if it conflicts with the new plan
- Unverified medical claims
- Unverified certificate claims
- Aggressive sales copy
- Countdown timers
- Marketplace-style discount visuals
- Broken Liquid snippets
- Old app-specific code unless still needed
- Code that bypasses Shopify product/cart/variant logic
- Any checkout-related customization

## 6. Migration Safety Rules

Before migrating anything, Codex must check:

1. Does this element fit the new YaksuDerma design system?
2. Does it support the current brand direction?
3. Does it preserve Shopify theme editor compatibility?
4. Does it preserve product/cart/variant/search/filtering logic?
5. Does it avoid hardcoded product prices?
6. Does it avoid medical or regulatory claims?
7. Does it work on mobile?
8. Does it improve the user experience?
9. Is it easier to rebuild cleanly instead of copying?
10. Can it be migrated in a small, reviewable change?

If the answer is uncertain, Codex should recommend rebuilding the idea cleanly instead of copying old code.

## 7. Migration Priority

Use this priority order:

### Priority 1 — Safe Assets

Examples:

- Logo
- Brand images
- Approved product images
- Approved banner images
- Icons if licensed and useful

### Priority 2 — Safe Content

Examples:

- About text
- Contact copy
- Verified authenticity text
- Verified certificate notes
- Existing collection descriptions if compliant

### Priority 3 — Useful Layout Ideas

Examples:

- A useful hero structure
- A good category section idea
- A trust section concept
- A support/contact section concept

These should usually be rebuilt using the new design system instead of copied directly.

### Priority 4 — Code Migration

Only migrate code if:

- It is clean
- It is still needed
- It does not conflict with Dawn
- It does not conflict with the new design system
- It does not break Shopify logic
- It is easier than rebuilding

## 8. Old Theme Review Table

When reviewing an old theme, Codex should produce a migration table.

| Source Area / File | Old Element | Target Area / File | Migrate? | Reason | Risk Level | Decision |
|---|---|---|---|---|---|---|
| Example: old homepage hero | Banner image + headline idea | New homepage hero section | Maybe | Image may fit brand, but copy needs review | Medium | Rebuild cleanly |
| Example: old CSS override | Button styling | Design system CSS | No | Conflicts with new button system | High | Do not migrate |
| Example: old logo asset | Logo image | Theme assets / header | Yes | Brand asset | Low | Migrate |

Risk levels:

```text
Low
Medium
High
Do not migrate
```

## 9. Migration Decision Types

Use one of these decision labels:

```text
Migrate as-is
Migrate with cleanup
Rebuild using new design system
Use as inspiration only
Do not migrate
Needs user confirmation
```

## 10. Questions Codex Must Ask Before Migration

Codex must ask or flag uncertainty before migrating:

- Certificate images
- Regulatory claims
- Product authenticity claims
- Before / after images
- Medical claims
- Old app code
- Checkout-related code
- Product-specific hardcoded content
- Wholesale-specific content
- Any content that may have legal/compliance risk

## 11. Files That May Be Compared

Old theme comparison may involve:

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

## 12. Migration Prompt

Use this prompt when ready to review the old theme:

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

## 13. Final Rule

Old theme migration is not a shortcut.

Main principle:

> Keep the new Dawn-based YaksuDerma theme clean. Migrate only what strengthens the final store, rebuild useful ideas when needed, and never copy old messy code blindly.
