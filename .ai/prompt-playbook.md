# Prompt Playbook

## MASTER PROMPT:
You are working on my Shopify Dawn-based theme repository for YaksuDerma.

Before doing anything, read:
- .ai/codex-instructions.md
- .ai/brand-brief.md
- .ai/store-brief.md
- .ai/catalog-brief.md
- .ai/design-system.md
- the relevant file under .ai/skills/

Goal:
Transform clean Dawn into a modern, premium, mobile-first, conversion-focused Shopify storefront for a Korean-inspired medical aesthetics / professional beauty products brand.

Important:
Do not edit files immediately unless I explicitly ask you to implement changes.
First audit the relevant theme structure and produce a plan.

Brand direction:
Minimal, elegant, clean, premium, clinical but soft, Korean-inspired, with subtle turquoise / water-inspired accents.

Technical rules:
- Work on a new branch.
- Preserve Shopify product, cart, variant, search, filtering, and checkout-related logic.
- Do not modify checkout.
- Do not remove existing app blocks.
- Do not hardcode product data unless explicitly requested.
- Prefer reusable sections, snippets, blocks, and theme settings.
- Keep sections editable in Shopify theme editor where possible.
- Keep changes small and reviewable.
- Explain every changed file.
- Run theme check if available, or explain manual validation steps if not.

Priority:
1. Audit theme structure
2. Create design system plan
3. Improve typography, spacing, colors, buttons, and product cards
4. Redesign homepage section hierarchy
5. Improve collection page and filtering experience
6. Improve product page conversion flow
7. Improve mobile UX
8. Check accessibility and performance
9. Migrate useful old-theme elements only after the new system is stable

Output format:
1. Files inspected
2. Current structure summary
3. Key problems/opportunities
4. Recommended plan
5. Files likely affected
6. Risks
7. Next safe implementation step

   
## 1. Repo Audit Prompt
Use before any editing.

## 2. Design System Planning Prompt
Use before CSS/design changes.

## 3. Design System Implementation Prompt
Use after design-system.md is approved.

## 4. Homepage Redesign Prompt
Use after design system is stable.

## 5. Product Card + Collection Prompt
Use after homepage direction is approved.

## 6. Product Page Prompt
Use after product cards are stable.

## 7. Migration Prompt
Use only after new design system is stable.
