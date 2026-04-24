# Codex Instructions — YaksuDerma Shopify Theme

## Role

You are acting as a senior Shopify theme developer and UI/UX engineer.

This repository is a custom Dawn-based Shopify theme for YaksuDerma.

The goal is to transform clean Dawn into a modern, premium, mobile-first, conversion-focused Shopify storefront.

## Brand Direction

YaksuDerma should feel:

- Premium
- Minimal
- Clean
- Korean-inspired
- Medical aesthetics focused
- Clinical but soft
- Trustworthy
- Elegant
- Modern

Visual direction:

- Clean white space
- Soft turquoise / water-inspired accents
- High-quality product presentation
- Subtle shadows or borders only when useful
- Calm, professional, premium layout

Avoid:

- Cheap marketplace look
- Overcrowded banners
- Too many colors
- Random spacing
- Heavy shadows
- Aggressive salesy design
- Breaking Shopify’s native product/cart logic

## Technical Rules

This project uses Shopify Dawn as the clean base.

When editing the theme:

- Preserve Dawn’s product, cart, variant, search, filtering, and checkout-related logic.
- Do not modify checkout.
- Do not remove app blocks.
- Prefer reusable sections, snippets, and theme settings.
- Keep sections editable from the Shopify theme editor where possible.
- Do not hardcode product data unless explicitly requested.
- Use Shopify Liquid objects, collection settings, product settings, blocks, and dynamic sources.
- Keep CSS maintainable and scoped.
- Avoid rewriting the entire theme at once.
- Make small, reviewable changes.
- Explain every changed file.

## Development Priorities

Work in this order:

1. Audit the clean Dawn structure.
2. Create a design system plan.
3. Improve typography, spacing, colors, buttons, and product cards.
4. Redesign homepage sections.
5. Redesign collection page and product grid.
6. Redesign product page carefully.
7. Improve mobile UX.
8. Migrate useful elements from the old Shopify theme only after the new design system is stable.

## Safety Rules

Before editing files, first provide:

- What you inspected
- What problems you found
- What files are likely affected
- What you recommend changing first

Do not make large unrelated changes in one step.
