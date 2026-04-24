# Design System — YaksuDerma

## 1. Purpose

This file defines the visual design system for the YaksuDerma Shopify theme.

Codex should use this file when working on:

- Colors
- Typography
- Spacing
- Buttons
- Product cards
- Collection grids
- Homepage sections
- Trust blocks
- Badges
- Mobile layout
- Header / footer styling
- Product page UI
- Conversion-focused design

This design system should be used together with:

- `.ai/codex-instructions.md`
- `.ai/brand-brief.md`
- `.ai/store-brief.md`
- `.ai/catalog-brief.md`
- `.ai/navigation-brief.md`
- `.ai/content-rules.md`

## 2. Design Goal

YaksuDerma should feel like:

> A clean, trustworthy, retail-friendly Korean aesthetics e-commerce store where customers can discover original products at fair prices and receive helpful human support.

The visual system should communicate:

- Trust
- Authenticity
- Korean-origin product focus
- Fair pricing
- Warm support
- Clean product discovery
- Professional but approachable e-commerce
- Premium feeling without looking expensive or distant

The store should not feel like:

- A cheap marketplace
- A cold B2B distributor portal
- An aggressive discount store
- A medical-claim-heavy website
- A generic Shopify template
- A luxury fashion store with poor product clarity

## 3. Core Design Principles

Use these principles in every UI decision:

1. **Trust first**
   - The store must feel legitimate, clean, and safe to browse.

2. **Product clarity**
   - Products have long technical names, so layouts must be readable and organized.

3. **Retail-friendly**
   - The site should be easy for individual customers, not only professional buyers.

4. **Professional but warm**
   - Avoid cold clinical design. Add subtle warmth through spacing, copy, and warm neutral backgrounds.

5. **Mobile-first**
   - Product discovery, navigation, and product cards must work beautifully on mobile.

6. **Fair price, not cheap**
   - Prices should be visible but not aggressive, loud, or suspicious.

7. **Editable Shopify structure**
   - Prefer theme settings, sections, blocks, dynamic sources, and Shopify objects.

8. **No risky medical claims**
   - Visual and text decisions must avoid treatment promises or invented claims.

## 4. Color Strategy

Color must support three psychological goals:

1. Trust
2. Authenticity
3. Warm helpfulness

The core brand direction uses:

- Soft turquoise
- Aqua
- Muted medical blue-green
- Clean neutrals

Only two additional color families should be used:

1. Trust Blue
2. Warm Sand / Soft Beige

Do not add random accent colors beyond this system.

## 5. Color Palette

These are recommended starting tokens. Codex may refine slightly during implementation, but should preserve the overall direction.

### 5.1 Base Neutrals

| Token | Hex | Purpose |
|---|---:|---|
| `--color-white` | `#FFFFFF` | Main background |
| `--color-off-white` | `#F8FBFA` | Soft section background |
| `--color-soft-gray` | `#EEF3F2` | Dividers, light UI blocks |
| `--color-border` | `#DDE7E5` | Borders, card outlines |
| `--color-muted-text` | `#5F6F6D` | Secondary text |
| `--color-charcoal` | `#1F2D2B` | Main text |
| `--color-deep-charcoal` | `#111A19` | High-emphasis text |

### 5.2 Core Brand Tones

| Token | Hex | Purpose |
|---|---:|---|
| `--color-soft-turquoise` | `#57C7C2` | Main brand accent |
| `--color-aqua-light` | `#DDF7F5` | Soft water-inspired background |
| `--color-aqua-pale` | `#EFFCFB` | Very light background tint |
| `--color-medical-blue-green` | `#2F8F8A` | Professional medical-aesthetic accent |
| `--color-muted-teal` | `#3D7976` | Deeper hover / text accent |

### 5.3 Additional Color Family 1 — Trust Blue

| Token | Hex | Purpose |
|---|---:|---|
| `--color-trust-blue` | `#3A6EA5` | Trust, links, certificate blocks |
| `--color-trust-blue-soft` | `#EAF2FA` | Soft trust section background |
| `--color-trust-blue-deep` | `#234D73` | Hover / strong trust accent |

Use Trust Blue for:

- Links
- Authenticity blocks
- Certificate-related sections
- Informational highlights
- Trust badges
- Subtle secondary CTAs

Avoid using Trust Blue in a cold corporate way.

### 5.4 Additional Color Family 2 — Warm Sand / Soft Beige

| Token | Hex | Purpose |
|---|---:|---|
| `--color-warm-sand` | `#F3E8D5` | Warm support sections |
| `--color-soft-beige` | `#FAF5EC` | Gentle background |
| `--color-sand-text` | `#7A684D` | Warm neutral text/accent |

Use Warm Sand / Soft Beige for:

- Customer support blocks
- Brand story sections
- Wholesale inquiry sections
- Gentle callout areas
- Human warmth

Avoid strong yellow, orange, gold, or luxury-metallic colors.

## 6. Color Usage Ratios

Recommended page-level color distribution:

```text
70–80%   White / off-white / clean neutrals
10–15%   Soft turquoise / aqua / medical blue-green
5–10%    Trust blue
5%       Warm sand / soft beige
```

Color should feel calm and intentional.

Avoid:

- Neon turquoise
- Saturated blue
- Heavy black sections
- Aggressive red sale labels
- Strong orange CTA buttons
- Random gradients
- Too many competing colors
- Marketplace-style discount colors

## 7. Background Rules

Preferred background hierarchy:

1. Main background: white
2. Alternate sections: off-white or pale aqua
3. Trust sections: trust blue soft or aqua pale
4. Support sections: warm sand / soft beige
5. Product cards: white
6. Footer: very light neutral or deep charcoal only if elegant and readable

Avoid dark backgrounds unless necessary.

If using a dark footer, make sure it feels premium and readable, not heavy.

## 8. CTA Color Rules

Primary CTA should usually use:

```text
Soft turquoise / medical blue-green
```

Recommended primary button:

- Background: `--color-medical-blue-green`
- Text: white
- Hover: `--color-muted-teal`

Secondary CTA:

- White or transparent background
- Border: `--color-medical-blue-green`
- Text: `--color-medical-blue-green`
- Hover: pale aqua background

Trust CTA / informational links:

- Use `--color-trust-blue`

Support CTA:

- Use warm neutral section background with teal or trust blue button

Avoid:

- Red CTA buttons
- Orange sales buttons
- Black buttons everywhere
- Too many button colors

## 9. Typography Direction

Typography should feel:

- Clean
- Modern
- Professional
- Readable
- Slightly premium
- Calm
- Suitable for technical product names

Avoid:

- Overly decorative fonts
- Too many font families
- Too many font weights
- Random font sizes
- Crowded text blocks
- Text over busy images

## 10. Suggested Font Strategy

Use Shopify/Dawn-compatible font settings where possible.

Recommended direction:

### Headings

Should feel:

- Clean
- Refined
- Confident
- Not overly playful
- Not too luxury-fashion

### Body

Should feel:

- Highly readable
- Neutral
- Friendly
- Clear on mobile

### Product Titles

Must support:

- Long product names
- Unit-based names
- Technical names
- Variant-like product names

Product titles should not be too thin or too small.

## 11. Type Scale

Suggested type scale:

| Element | Desktop | Mobile | Notes |
|---|---:|---:|---|
| Hero heading | 48–64px | 34–42px | Strong but not huge |
| Page heading | 40–52px | 30–36px | Clean hierarchy |
| Section heading | 30–40px | 24–30px | Reusable |
| Card title | 16–18px | 14–16px | Must handle long names |
| Body text | 16px | 15–16px | Readable |
| Small text | 13–14px | 12–13px | Avoid going too small |
| Badge text | 11–12px | 11–12px | Uppercase optional |

## 12. Heading Rules

Headings should:

- Be clear and direct.
- Use sentence case or title case consistently.
- Avoid exaggerated claims.
- Avoid too many lines on mobile.
- Support SEO-friendly collection names on category pages.

Good examples:

```text
Authentic Korean-Origin Aesthetic Products
Shop by Category
Explore Toxins
Dermal & Body Fillers
Fair Pricing, Helpful Support
```

Avoid:

```text
Miracle Beauty Transformation
Cheapest Botox Online
Guaranteed Results
Instant Fat Loss
```

## 13. Spacing System

Spacing should feel calm and premium.

Use consistent spacing instead of random margins.

Suggested spacing tokens:

| Token | Value | Usage |
|---|---:|---|
| `--space-2xs` | `4px` | Tiny gaps |
| `--space-xs` | `8px` | Badge/card internals |
| `--space-sm` | `12px` | Small components |
| `--space-md` | `16px` | Base spacing |
| `--space-lg` | `24px` | Card/section spacing |
| `--space-xl` | `32px` | Section groups |
| `--space-2xl` | `48px` | Large sections |
| `--space-3xl` | `72px` | Hero/major section |
| `--space-4xl` | `96px` | Large desktop sections |

## 14. Section Spacing

Recommended section padding:

### Desktop

```text
Small section: 48px top/bottom
Normal section: 72px top/bottom
Hero section: 80–112px top/bottom
```

### Mobile

```text
Small section: 32px top/bottom
Normal section: 48px top/bottom
Hero section: 56–72px top/bottom
```

Avoid:

- Huge empty spaces on mobile
- Sections touching each other with no rhythm
- Random padding values
- Overcrowded product grids

## 15. Layout Widths

Recommended layout behavior:

- Use Dawn’s page width system where possible.
- Do not make content full-width unless visually intentional.
- Keep text content readable.
- Product grids should have enough breathing room.
- Homepage hero may use full-width background, but content should remain aligned and readable.

Suggested maximum content width:

```text
Main content: 1200–1320px
Text-only content: 720–860px
Product grid: theme page width
```

## 16. Border Radius

YaksuDerma should feel soft but professional.

Suggested radius:

| Token | Value | Usage |
|---|---:|---|
| `--radius-sm` | `6px` | Small badges |
| `--radius-md` | `10px` | Buttons, small cards |
| `--radius-lg` | `16px` | Product/category cards |
| `--radius-xl` | `24px` | Hero blocks, feature cards |

Avoid:

- Fully childish pill shapes everywhere
- Sharp harsh boxes everywhere
- Inconsistent radius values

## 17. Shadows and Borders

Use borders more than heavy shadows.

Preferred:

- Light border
- Very soft shadow only on hover or elevated cards
- Clean separation through spacing and background

Suggested shadow:

```css
0 12px 30px rgba(31, 45, 43, 0.06)
```

Use sparingly.

Avoid:

- Heavy drop shadows
- Marketplace-style card shadows
- Random shadow directions
- Overly glossy UI

## 18. Button System

Buttons should feel:

- Clear
- Calm
- Premium
- Easy to tap
- Not aggressive

### Primary Button

Use for main CTAs:

- Explore Products
- Shop Categories
- View Collection
- Add to Cart

Style direction:

- Filled teal / medical blue-green
- White text
- Medium radius
- Clear hover state
- Strong contrast
- Comfortable padding

### Secondary Button

Use for supporting CTAs:

- Contact Us
- Wholesale Inquiry
- Learn More
- View Details

Style direction:

- Outline or light background
- Teal or trust blue text
- Calm hover state

### Text Link

Use for subtle navigation:

- View all
- Learn more
- Ask about availability

Style direction:

- Trust blue or muted teal
- Underline on hover
- Accessible focus state

## 19. Button Copy Rules

Preferred CTA copy:

- Explore Products
- Shop Categories
- View Collection
- Browse Products
- Contact Us
- Ask About Availability
- Wholesale Inquiry
- Need Help Choosing?

Avoid:

- Buy Now!!!
- Cheapest Products
- Guaranteed Results
- Limited Time Only
- Miracle Treatment
- Instant Transformation

## 20. Product Card System

Product cards are one of the most important UI components.

They must support:

- Long technical product names
- Unit-based names
- Price visibility
- Clean image ratios
- Mobile two-column browsing
- Optional badges
- Fair-price perception
- Trustworthy presentation

Product cards should look:

- Clean
- Organized
- Professional
- Retail-friendly
- Not cheap
- Not overcrowded

## 21. Product Card Layout

Recommended structure:

1. Product image
2. Optional badge row
3. Product title
4. Optional product category / vendor / origin line
5. Dynamic Shopify price
6. Optional CTA or quick link

Do not hardcode prices.

Use Shopify product data dynamically:

- `product.title`
- `product.price`
- `product.featured_image`
- `product.url`
- `product.available`
- Product metafields when available

## 22. Product Image Rules

Product images should:

- Use consistent aspect ratios.
- Avoid messy cropping.
- Have enough white space.
- Support product packaging visuals.
- Not feel distorted.
- Load responsibly.

Suggested product card aspect ratio:

```text
1:1 or 4:5
```

Use whichever works better with actual product images.

Avoid:

- Overcropping product boxes
- Tiny product images inside huge cards
- Inconsistent image height across cards
- Busy backgrounds

## 23. Product Title Rules

Product titles should:

- Be readable
- Be allowed to wrap gracefully
- Not become visually messy
- Avoid being too small
- Preserve exact product names

Recommended:

- 2–3 line clamp on cards if needed
- Full title visible on product page
- Avoid changing product title text

Examples:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
J-Cain Cream 10.56% 500g
Rejuran Healer
```

## 24. Price Display Rules

Price should be:

- Visible
- Clean
- Calm
- Trustworthy
- Not aggressive

Avoid:

- Oversized red prices
- Flash-sale price styling
- Marketplace discount design
- Hardcoded prices
- Fake urgency

Use Shopify dynamic pricing.

## 25. Badge System

Potential badges:

- Korean Origin
- Original Product
- Popular
- Featured
- Professional Use
- Wholesale Inquiry Available
- Bestseller

Badge rules:

- Do not invent badge claims.
- Do not show “Bestseller” unless confirmed.
- Do not show “Certified” unless certificate details are provided.
- Keep badges subtle.
- Avoid more than 1–2 badges per product card.

Badge style:

- Small
- Calm
- Rounded
- Light background
- Muted teal / trust blue / warm neutral
- Not red-heavy

## 26. Collection Page System

Collection pages should feel:

- Organized
- Searchable
- Filter-friendly
- Mobile-friendly
- Professional
- Not overwhelming despite many products

Collection pages must preserve:

- Shopify filtering
- Shopify sorting
- Pagination
- Product URLs
- Product data
- Dynamic product prices

## 27. Collection Header Rules

Collection page headers should:

- Use clear SEO-friendly collection titles.
- Include short, safe, non-medical-claim descriptions.
- Avoid treatment promises.
- Avoid overly long text.
- Look clean on mobile.

Example title mapping:

```text
Toxins → Botulinum Toxins
Fillers → Dermal & Body Fillers
Skin Boosters → Skin Boosters & Exosomes
Fat Dissolvers → Mesotherapy & Contouring
Accessories → Clinical Accessories & IV Therapy
```

## 28. Homepage System

Homepage should not rely only on a large hero.

Recommended homepage section flow:

1. Hero with clear value proposition
2. Trust / authenticity bar
3. Category showcase
4. Featured collection or products
5. Why YaksuDerma
6. Customer support block
7. Optional wholesale inquiry block
8. Footer trust links

Homepage should communicate:

- What the store sells
- Korean-origin focus
- Original product positioning
- Fair pricing
- Helpful support
- Main categories
- Easy next action

## 29. Hero Section Rules

Hero should feel:

- Clean
- Trustworthy
- Premium but accessible
- Product/category oriented
- Not visually crowded

Hero should include:

- Clear headline
- Short supporting text
- Primary CTA
- Secondary CTA
- Optional product/category visual

Preferred hero copy direction:

```text
Authentic Korean-Origin Aesthetic Products
Fair pricing, clear product discovery, and helpful support.
```

Avoid:

```text
Guaranteed Results
Cheapest Products Online
Instant Transformation
```

## 30. Category Card System

Homepage category cards should use visible navigation labels:

- Toxins
- Fillers
- Skin Boosters
- Fat Dissolvers
- Collagen Stimulators
- Accessories

Cards should:

- Link to collections
- Use clean visuals
- Have short descriptions
- Avoid medical claims
- Work in mobile grid
- Be editable from Shopify theme editor where possible

## 31. Trust Block System

Trust blocks are important.

Possible trust block topics:

- Original Korean-origin products
- Fair pricing
- Helpful support
- Carefully handled orders
- Authenticity-focused sourcing
- Business inquiries welcome

Trust block style:

- Soft aqua, trust blue, or warm beige background
- Small icon optional
- Short copy
- Clear layout
- No exaggerated claims

## 32. Support Block System

Support sections should feel warm and human.

Use warm sand / soft beige carefully.

Possible copy:

```text
Need help choosing a product?
Our team can help with availability and product details.
```

CTA:

```text
Contact Us
Ask About Availability
Wholesale Inquiry
```

Avoid:

- Pressure
- Fake urgency
- Medical advice
- Treatment instructions

## 33. Product Page System

Product pages should prioritize:

- Product image clarity
- Exact product name
- Dynamic Shopify price
- Variant logic if applicable
- Add-to-cart clarity
- Product description
- Origin/authenticity information if verified
- Support/contact option
- Related products
- Careful shipping/availability language

Do not break:

- Product form logic
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Selling plan logic if present
- App blocks
- Shopify product data

## 34. Product Page Layout Direction

Recommended layout:

1. Product media gallery
2. Product title
3. Dynamic price
4. Variant selector if applicable
5. Quantity selector
6. Add to cart
7. Support / availability note
8. Accordion sections
9. Related products

Accordion ideas:

- Product Details
- Authenticity / Origin
- Shipping & Availability
- Wholesale Inquiry
- Support

Only include content that is verified or editable.

## 35. Related Products

Related product sections should feel helpful, not pushy.

Preferred labels:

- Related products
- You may also explore
- Often viewed with
- Explore related categories

Avoid:

- Required for treatment
- Must be used with
- Use this together
- Any medical instruction

Known cross-sell logic:

- Liporase may be recommended with filler products when technically feasible.
- Numbing creams may appear as accessories where appropriate.
- Do not frame cross-sells as medical instructions.

## 36. Header System

Header should feel:

- Clean
- Premium
- Product-first
- Lightweight
- Not marketplace-like
- Not too tall
- Easy to scan

Visible desktop navigation:

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

Header must preserve:

- Search
- Cart
- Account icon if enabled
- Mobile drawer
- Shopify menu logic

## 37. Footer System

Footer should support:

- Product discovery
- Trust
- Contact
- Policies
- Wholesale inquiry
- Authenticity / certificates if verified

Footer groups:

### Shop

- Toxins
- Fillers
- Skin Boosters
- Fat Dissolvers
- Collagen Stimulators
- Accessories

### Support

- Contact
- Shipping Information
- Product Availability
- Wholesale Inquiry
- Returns / Refund Policy

### Company

- About YaksuDerma
- Authenticity / Certificates
- Customer Support
- Privacy Policy
- Terms of Service

## 38. Mobile System

Mobile design is a priority.

Mobile must support:

- Fast category understanding
- Easy menu access
- Readable product cards
- Two-column product grids where appropriate
- Clear product prices
- Tap-friendly buttons
- Easy contact/support access
- Search access
- Cart access

Avoid:

- Desktop-first layouts squeezed into mobile
- Tiny text
- Tiny buttons
- Overlapping hero text
- Crowded product cards
- Hidden search/cart
- Deep nested menus unless needed

## 39. Mobile Product Grid

Recommended:

- Two-column product grid on mobile if product images and titles remain readable.
- One-column layout for product-heavy sections if cards become crowded.
- Keep product titles readable.
- Keep price visible.
- Avoid too many badges.

Codex should test mobile layout assumptions carefully.

## 40. Accessibility Rules

Design should support:

- Sufficient contrast
- Logical heading hierarchy
- Visible focus states
- Clear buttons
- Tap-friendly mobile targets
- Readable text
- Avoiding text over busy images
- Not relying only on color to communicate meaning

## 41. Animation and Interaction

Use minimal interaction.

Preferred:

- Soft hover states
- Subtle card elevation
- Gentle underline on links
- Smooth but not distracting transitions

Avoid:

- Heavy animations
- Auto-moving carousels
- Distracting effects
- Slow interactions
- Anything that hurts mobile performance

## 42. Performance Rules

Avoid unnecessary complexity.

Prefer:

- CSS-first solutions
- Minimal JavaScript
- Shopify-native lazy loading where applicable
- Optimized images
- Reusable snippets
- Small changes

Avoid:

- Large JS libraries
- Heavy sliders
- Unnecessary animation frameworks
- Duplicate CSS
- Overly complex custom components

## 43. Implementation Rules for Codex

When implementing this design system:

- Inspect actual Dawn files before editing.
- Preserve Shopify product/cart/variant/search/filtering logic.
- Do not modify checkout.
- Do not remove app blocks.
- Do not hardcode prices.
- Do not hardcode product data unless explicitly requested.
- Prefer reusable sections, snippets, and settings.
- Keep Shopify theme editor compatibility.
- Make small, reviewable changes.
- Explain changed files.
- Do not rewrite the entire theme at once.

## 44. Files Likely Involved

Design system changes may involve:

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
sections/main-product.liquid
sections/main-collection-product-grid.liquid
sections/featured-collection.liquid
sections/image-banner.liquid
snippets/card-product.liquid
snippets/price.liquid
config/settings_schema.json
templates/index.json
templates/collection.json
templates/product.json
```

Codex must inspect the actual repository because Dawn file names may vary by version.

## 45. Final Visual Summary

YaksuDerma should look:

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

YaksuDerma should not look:

- Cheap
- Aggressive
- Overdesigned
- Cold
- Crowded
- Marketplace-like
- Medical-claim-heavy
- Generic Dawn default
