# Skill 03 — CSS Refactor & Design Foundation Implementation

## 1. Purpose

This skill is used to implement the approved YaksuDerma design-system foundations in the Shopify Dawn theme.

This skill comes after:

```text
01-theme-audit.md
02-design-system-planning.md
```

Use this skill only after the design-system plan has been reviewed and approved.

The goal is to safely improve the visual foundation of the theme without rewriting the entire CSS and without breaking Shopify functionality.

## 2. Required Context Files

Before starting CSS refactor work, Codex must read:

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
.ai/skills/02-design-system-planning.md
.ai/skills/03-css-refactor.md
```

Codex should use these files to understand:

- Approved color direction
- Typography goals
- Spacing system
- Button system
- Product card foundation
- Mobile-first design priorities
- Shopify safety rules
- Content safety boundaries
- Custom component styling needs

## 3. Implementation Scope

This skill is for foundational CSS and design implementation only.

Allowed work:

- Color tokens / CSS variable refinement
- Global typography foundation
- Section spacing foundation
- Button style foundation
- Link style foundation
- Card radius / border / shadow foundation
- Product card foundation styling
- Badge style foundation
- Trust block styling foundation
- Mobile spacing improvements
- Header/footer visual polish if low risk

Not allowed in this skill:

- Full homepage redesign
- Full product page redesign
- Full collection page redesign
- Custom component buildout
- Product family comparison table implementation
- Before / after module implementation
- Old theme migration
- Cart logic changes
- Product form logic changes
- Variant picker logic changes
- Filtering/sorting logic changes
- Checkout changes

## 4. Non-Negotiable Shopify Safety Rules

Codex must preserve:

- Product form logic
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
- Hardcode product data
- Add medical claims
- Rewrite the entire CSS
- Add unnecessary JavaScript
- Copy reference site code
- Make broad unrelated changes

## 5. CSS Refactor Goal

The CSS foundation should make Dawn feel more like YaksuDerma:

- Clean
- Premium but accessible
- Water-inspired
- Trustworthy
- Warm and helpful
- Product-first
- Mobile-first
- Suitable for long technical product names
- Not marketplace-like
- Not generic Dawn default

The refactor should create a foundation for later homepage, product card, collection, and product page redesign work.

## 6. Color Implementation Rules

Use the approved palette from `.ai/design-system.md`.

Core color families:

```text
White / off-white / clean neutrals
Soft turquoise
Aqua
Muted medical blue-green
Trust blue
Warm sand / soft beige
Charcoal text
Light borders
```

Implementation should support tokens such as:

```css
--color-white: #FFFFFF;
--color-off-white: #F8FBFA;
--color-soft-gray: #EEF3F2;
--color-border: #DDE7E5;
--color-muted-text: #5F6F6D;
--color-charcoal: #1F2D2B;
--color-deep-charcoal: #111A19;

--color-soft-turquoise: #57C7C2;
--color-aqua-light: #DDF7F5;
--color-aqua-pale: #EFFCFB;
--color-medical-blue-green: #2F8F8A;
--color-muted-teal: #3D7976;

--color-trust-blue: #3A6EA5;
--color-trust-blue-soft: #EAF2FA;
--color-trust-blue-deep: #234D73;

--color-warm-sand: #F3E8D5;
--color-soft-beige: #FAF5EC;
--color-sand-text: #7A684D;
```

Codex should adapt token placement to the actual Dawn CSS structure.

Avoid:

- Neon turquoise
- Aggressive red sale styling
- Strong orange CTA buttons
- Random gradients
- Too many competing accent colors
- Marketplace-style discount colors

## 7. Typography Implementation Rules

Typography changes should improve:

- Readability
- Product title clarity
- Heading hierarchy
- Mobile readability
- Premium but approachable tone

Codex may adjust:

- Heading sizes
- Heading line-height
- Body text line-height
- Product card title size
- Product card title line-height
- Button text style
- Badge text style

Codex must avoid:

- Too many font sizes
- Too many font weights
- Overly decorative typography
- Tiny mobile text
- Breaking Dawn theme font settings
- Hardcoding fonts that conflict with Shopify theme editor settings

Preferred approach:

- Preserve Shopify theme font settings where possible.
- Improve scale, spacing, and readability through CSS.
- Keep product titles readable and stable.

## 8. Spacing Implementation Rules

Spacing should create calm, premium rhythm.

Codex may implement or align with spacing tokens:

```css
--space-2xs: 4px;
--space-xs: 8px;
--space-sm: 12px;
--space-md: 16px;
--space-lg: 24px;
--space-xl: 32px;
--space-2xl: 48px;
--space-3xl: 72px;
--space-4xl: 96px;
```

Use spacing improvements for:

- Section padding
- Product card spacing
- Grid gaps
- Button padding
- Trust blocks
- Header/footer breathing room
- Mobile spacing

Avoid:

- Random margins
- Massive mobile gaps
- Crowded product cards
- Overriding every existing Dawn spacing rule
- Breaking layout consistency

## 9. Button Implementation Rules

Buttons should feel:

- Clear
- Calm
- Premium
- Tap-friendly
- Not aggressive

Button system should support:

```text
Primary CTA
Secondary CTA
Text link
Add-to-cart button
Product card CTA
Support/Contact CTA
Wholesale Inquiry CTA
```

Preferred primary CTA:

- Background: medical blue-green or muted teal
- Text: white
- Hover: deeper muted teal
- Border radius: medium
- Strong but calm contrast

Preferred secondary CTA:

- Transparent or white background
- Teal/trust-blue border
- Teal/trust-blue text
- Pale aqua hover state

Avoid:

- Red CTA buttons
- Orange sales buttons
- Too many button color styles
- Tiny buttons
- Buttons with poor contrast

## 10. Card Foundation Rules

Cards should feel:

- Clean
- Organized
- Professional
- Soft but not childish
- Premium but not luxury-heavy
- Suitable for product-heavy catalog browsing

Codex may implement:

- Light borders
- Subtle radius
- Soft hover elevation
- Consistent internal spacing
- Better card image rhythm
- Improved product card text spacing

Preferred:

```css
border: 1px solid var(--color-border);
border-radius: 16px;
box-shadow: none;
```

Hover may use:

```css
box-shadow: 0 12px 30px rgba(31, 45, 43, 0.06);
```

Use shadows sparingly.

Avoid:

- Heavy marketplace shadows
- Overly glossy cards
- Random radii
- Too many badges
- Crowded card interiors

## 11. Product Card Foundation Rules

This skill can improve product card foundations, but should not fully redesign product card logic unless explicitly approved.

Allowed:

- Better title readability
- Better spacing
- Better image container consistency
- Better price spacing
- Better border/radius
- Subtle hover state
- Badge base styling

Not allowed yet unless explicitly requested:

- Large markup restructuring
- Product card data logic changes
- Hardcoded badges
- Hardcoded prices
- Removing dynamic Shopify price snippet
- Removing product links
- Breaking product image logic

Product card must support long names such as:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
J-Cain Cream 10.56% 500g
Rejuran Healer
```

## 12. Badge Foundation Rules

Badge styles should be subtle.

Potential badge types:

```text
Korean Origin
Original Product
Popular
Featured
Professional Use
Wholesale Inquiry Available
Bestseller
```

Do not invent badge claims.

Allowed CSS work:

- Badge radius
- Badge font size
- Badge spacing
- Badge colors
- Badge border

Avoid:

- Loud red badges
- Too many badge styles
- Fake “Bestseller” styling without data
- Certificate badges unless verified

## 13. Trust and Support Block Foundation

Codex may create reusable styling foundations for future trust/support blocks.

These blocks may later support:

- Original Korean-origin products
- Fair pricing
- Helpful support
- Carefully handled orders
- Wholesale inquiry
- Authenticity information

Style direction:

- Soft aqua, trust-blue-soft, or warm beige backgrounds
- Light borders
- Rounded corners
- Short readable copy
- Calm icon treatment if icons exist
- Mobile-friendly stacked layout

Do not add actual claims or section content during CSS foundation unless approved.

## 14. Header/Footer Visual Polish

Allowed low-risk refinements:

- Better header spacing
- Better link hover states
- Better menu readability
- Better footer spacing
- Footer typography improvements
- Mobile drawer visual polish

Must preserve:

- Search
- Cart
- Account icon if enabled
- Shopify menu logic
- Mobile drawer behavior
- Header settings

Final visible desktop navigation from `.ai/navigation-brief.md`:

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

Do not hardcode navigation if Shopify admin menus can control it.

## 15. Mobile CSS Rules

Mobile improvements are allowed if safe.

Focus on:

- Product card readability
- Section spacing
- Button tap targets
- Header/menu spacing
- Text wrapping
- Image containment
- Product grid breathing room

Avoid:

- Desktop-first overrides
- Tiny text
- Hidden search/cart
- Overly deep mobile menus
- Horizontal overflow
- Product cards that become unreadable

## 16. Files Likely Involved

Codex should inspect actual repo files before editing.

Likely files:

```text
assets/base.css
assets/component-card.css
assets/component-price.css
assets/component-button.css
assets/section-main-product.css
assets/component-menu-drawer.css
assets/component-mega-menu.css
assets/component-accordion.css
sections/header.liquid
sections/footer.liquid
snippets/card-product.liquid
snippets/price.liquid
```

Do not assume every file exists.

Adapt to the actual Dawn version.

## 17. Implementation Size Rules

CSS refactor must be small and reviewable.

Good first implementation:

```text
Design tokens + button foundation + basic spacing improvements
```

Bad first implementation:

```text
Rewrite all CSS, redesign homepage, product cards, product page, and mobile layout in one commit
```

Each implementation should be scoped.

Suggested phases:

```text
Phase 1 — Color tokens and global foundations
Phase 2 — Typography and spacing
Phase 3 — Button system
Phase 4 — Card foundation
Phase 5 — Product card foundation
Phase 6 — Header/footer polish
Phase 7 — Mobile refinements
```

Do not implement all phases at once unless explicitly requested.

## 18. Required Output Format for Implementation

When implementing, Codex must output:

```text
# CSS Refactor Implementation — YaksuDerma

## 1. Files Changed

List files changed.

## 2. What Changed

Explain changes grouped by:
- Colors
- Typography
- Spacing
- Buttons
- Cards
- Mobile
- Header/footer if applicable

## 3. Why It Changed

Tie each change back to `.ai/design-system.md`.

## 4. Shopify Logic Preserved

Confirm what was not touched:
- Product form
- Variant picker
- Cart
- Search
- Filtering
- Sorting
- Pagination
- App blocks

## 5. Risk Level

Use:
- Low
- Medium
- High

## 6. How to Test in Shopify Preview

List practical checks.

## 7. Follow-Up Tasks

Recommend the next safe task.
```

## 19. Testing Checklist

After CSS implementation, test:

### Global

- Homepage loads
- Header displays correctly
- Footer displays correctly
- Search opens/works
- Cart icon still works
- No horizontal overflow

### Product Cards

- Long product names wrap properly
- Price still displays dynamically
- Product images are not distorted
- Product links work
- Mobile grid remains readable

### Collection Pages

- Filters still work
- Sorting still works
- Pagination still works
- Product grid is readable

### Product Pages

- Product form still works
- Variant picker still works
- Add-to-cart still works
- Dynamic checkout buttons still display if enabled
- App blocks are not removed

### Mobile

- Header not too tall
- Menu readable
- Buttons tappable
- Product cards readable
- No text overflow
- No layout breaking

## 20. What Codex Must Not Do

During CSS refactor, Codex must not:

- Change product form logic
- Change variant picker logic
- Change cart JavaScript
- Change filtering JavaScript
- Change search JavaScript
- Modify checkout
- Remove app blocks
- Hardcode product prices
- Hardcode product data
- Add medical claims
- Copy external reference site CSS
- Rewrite entire Dawn CSS
- Add heavy animation libraries

## 21. Example User Prompt

Use this prompt with Codex after approving the design-system plan:

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

## 22. Final Reminder

This skill is for carefully implementing the approved visual foundation.

Main principle:

> Improve Dawn’s visual foundation without breaking Shopify commerce logic. Keep CSS changes small, reviewable, mobile-safe, and aligned with YaksuDerma’s design system.
