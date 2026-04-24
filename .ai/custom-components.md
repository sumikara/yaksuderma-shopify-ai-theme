# Custom Components Brief — YaksuDerma

## 1. Purpose

This file defines custom Shopify theme components that YaksuDerma may need beyond default Dawn sections.

Codex should use this file when working on:

- Product page custom modules
- Product comparison tables
- Product family tables
- Unit comparison tables
- Related products
- Purchased-together logic
- Authenticity / certificate blocks
- Before / after visual modules
- Category education blocks
- Product information accordions
- Shopify metafield-driven product content
- Theme editor configurable sections

The goal is to make YaksuDerma feel more professional, helpful, and product-discovery focused without hardcoding product data or breaking Shopify commerce logic.

This file should be read together with:

- `.ai/codex-instructions.md`
- `.ai/brand-brief.md`
- `.ai/store-brief.md`
- `.ai/catalog-brief.md`
- `.ai/navigation-brief.md`
- `.ai/design-system.md`
- `.ai/content-rules.md`
- `.ai/skills/07-product-page-redesign.md`
- `.ai/skills/10-conversion-copywriting.md`

## 2. General Component Strategy

YaksuDerma should not rely only on default Dawn components.

The theme may need custom components that help customers understand:

- Product families
- Unit differences
- Category differences
- Related product options
- Product origin and authenticity
- Availability and support
- Wholesale inquiry paths
- Product comparison logic

However, custom components must remain:

- Clean
- Trustworthy
- Shopify-native
- Mobile-friendly
- Editable where possible
- Safe from medical-claim risk
- Dynamic where possible
- Easy to maintain

Codex should avoid building overly complex, hardcoded, fragile components.

## 3. Non-Negotiable Rules

Codex must not hardcode:

- Product prices
- Product availability
- Product stock
- Product URLs
- Product images
- Product descriptions
- Product certificates
- Regulatory approvals
- Medical claims
- Treatment instructions
- Before / after claims

Use Shopify dynamic data whenever possible.

Preferred data sources:

- Shopify product data
- Shopify collections
- Shopify metafields
- Shopify metaobjects if appropriate
- Shopify section settings
- Shopify section blocks
- Theme editor configurable content

Reference information in `.ai/catalog-brief.md` is for planning only.

## 4. Product Family Comparison Tables

YaksuDerma needs the ability to show product family comparison tables.

Example product families:

- Botulax 100 Units / 200 Units / 300 Units
- Nabota 100 Units / 200 Units
- Re N Tox 100 Units / 200 Units
- Liztox 100 Units / 200 Units
- Wondertox 100 Units / 200 Units
- One Tox 100 Units / 200 Units
- Kaimax 100 Units / 200 Units
- Jurtox 100 Units / 200 Units
- EPTQ S100 / S300 / S500
- Chaeum Premium 1 / 2 / 3 / 4
- VOM Light / Intensive / Volume
- Rejuran I / HB / Healer

The purpose is to help customers compare related products in the same family.

## 5. Product Family Table Example

A product family table may look like this:

| Product | Unit / Type | Price | Availability | Action |
|---|---|---:|---|---|
| Botulax 100 Units | 100 Units | Dynamic Shopify price | Dynamic Shopify availability | View Product |
| Botulax 200 Units | 200 Units | Dynamic Shopify price | Dynamic Shopify availability | View Product |
| Botulax 300 Units | 300 Units | Dynamic Shopify price | Dynamic Shopify availability | View Product |

Important:

- Prices must come from Shopify dynamically.
- Availability must come from Shopify dynamically if shown.
- Product links must come from Shopify dynamically.
- Product names should remain exact.
- Table should work well on mobile.
- Table should not feel cluttered.

## 6. Unit Comparison Tables

Some products have unit-based differences such as:

- 50 Units
- 100 Units
- 200 Units
- 300 Units
- 30g
- 500g
- 1.2 ml
- 60ml
- 60cc
- 365mg

Codex may create a reusable unit comparison module.

Possible columns:

| Column | Purpose |
|---|---|
| Product | Exact Shopify product title |
| Unit / Size | Unit value if available |
| Product Family | Product group |
| Price | Dynamic Shopify price |
| Link | Dynamic Shopify product URL |

Do not invent unit information if it is not in the product title, metafield, or user-provided data.

## 7. Product Comparison Table UX

Comparison tables should be:

- Clean
- Minimal
- Easy to scan
- Mobile-friendly
- Not overly dense
- Not too wide on mobile
- Scrollable horizontally only if necessary
- Styled with light borders
- Styled with soft neutral backgrounds
- Consistent with the YaksuDerma design system

Recommended styling:

- White background
- Light border
- Charcoal text
- Subtle turquoise or trust-blue accents
- Clear header row
- No aggressive colors
- No heavy shadows

Avoid:

- Marketplace-style comparison tables
- Overcrowded technical tables
- Tiny mobile text
- Hardcoded prices
- Medical claims
- Treatment advice

## 8. Product Family Data Strategy

Preferred technical strategy:

Use Shopify metafields or metaobjects to group products by family.

Suggested metafields:

```text
product.metafields.custom.product_family
product.metafields.custom.comparison_group
product.metafields.custom.unit_size
product.metafields.custom.product_origin
product.metafields.custom.authenticity_note
product.metafields.custom.professional_use_note
product.metafields.custom.related_products
product.metafields.custom.certificate_note
```

Example:

```text
Product: Botulax 100 Units
product_family: Botulax
comparison_group: botulax-units
unit_size: 100 Units
product_origin: Korea
```

```text
Product: Botulax 200 Units
product_family: Botulax
comparison_group: botulax-units
unit_size: 200 Units
product_origin: Korea
```

Codex should propose a metafield strategy before implementing dynamic comparison tables.

## 9. Theme Editor Fallback Strategy

If metafields are not ready, Codex may create configurable section blocks.

Example section:

```text
Product Family Comparison Table
```

Possible block settings:

- Product selector
- Unit / size text
- Optional note
- Optional badge
- Button label

This allows the store owner to manually select related products from the Shopify theme editor.

Preferred fallback:

- Use product picker blocks.
- Pull product title, price, image, and URL dynamically.
- Allow optional manually entered unit label.
- Do not manually enter prices.

Do not create a component that requires editing Liquid every time a product changes.

## 10. Related Products / Purchased Together

YaksuDerma may need related-product modules.

Examples:

- Liporase may be shown as a related product for Dermal & Body Filler products.
- Numbing creams may be shown as related accessories where appropriate.
- Skin booster products may show related PDRN / exosome products.
- Toxin product pages may show products from the same product family.

Preferred labels:

- Related products
- You may also explore
- Often viewed with
- Explore related categories
- Related accessories

Avoid:

- Required for treatment
- Must be used with
- Use this together
- Medical instruction wording
- Treatment protocol wording

## 11. Related Products Data Strategy

Preferred technical options:

1. Shopify product recommendations if suitable.
2. Product metafield list of related products.
3. Theme editor product picker blocks.
4. Collection-based fallback.

Suggested metafield:

```text
product.metafields.custom.related_products
```

Possible fallback:

```text
If product is in Dermal & Body Fillers collection,
show a related accessories block that can include Liporase or numbing creams through configurable product picker blocks.
```

Codex must not hardcode related products unless explicitly instructed.

## 12. Authenticity / Certificate Blocks

Trust and authenticity are central to YaksuDerma.

The theme may include authenticity or certificate-related blocks.

Possible block titles:

- Original Korean-Origin Products
- Authenticity-Focused Sourcing
- Certificate Information
- Product Authenticity
- Need Certificate Details?

Possible safe copy:

```text
We prioritize original Korean-origin products and clear product information. Contact us for product details, availability, and certificate information where applicable.
```

Rules:

- Do not invent certificate names.
- Do not invent approval claims.
- Do not claim FDA, CE, KFDA, Thai FDA, or any regulatory status unless the user provides verified information.
- Do not use certificate logos unless the user provides them and confirms permission.
- Keep wording neutral and trust-focused.

## 13. Authenticity Block Data Strategy

Preferred data sources:

- Product metafield: certificate note
- Product metafield: authenticity note
- Product metafield: product origin
- Theme editor text block
- Theme editor image picker for uploaded certificate image, if verified

Suggested metafields:

```text
product.metafields.custom.product_origin
product.metafields.custom.authenticity_note
product.metafields.custom.certificate_note
product.metafields.custom.certificate_image
```

Do not display certificate sections globally if product-specific certificate data is missing, unless the text is general and neutral.

## 14. Before / After Visual Blocks

YaksuDerma may want before / after or comparison-style visual blocks in some places.

These components are sensitive because the product category is related to beauty and medical aesthetics.

Before / after blocks are allowed only if:

- The user provides verified images.
- The user confirms the content is compliant.
- Copy does not imply guaranteed results.
- Copy does not invent treatment claims.
- Copy does not imply medical advice.
- The section is optional and configurable.

Preferred neutral labels:

- Visual reference
- Product information image
- Result reference, if legally verified
- Customer-provided visual, if verified
- Before / after, only if legally safe and explicitly approved

Avoid:

- Guaranteed result language
- “This product will produce this result”
- “Instant transformation”
- “Clinically proven result”
- “Permanent result”
- Treatment claims
- Fake before / after imagery

## 15. Before / After UX Rules

If implemented, before / after visual blocks should:

- Be optional
- Be disabled by default
- Be editable from Shopify theme editor
- Allow image upload
- Allow short caption
- Include disclaimer text if needed
- Avoid aggressive sales design
- Avoid fake urgency
- Be mobile-friendly

Possible section settings:

- Before image
- After image
- Caption
- Disclaimer text
- Layout style
- Enable / disable section

Codex should first propose the safe implementation plan before editing files.

## 16. Category Education Blocks

YaksuDerma may use short educational blocks to help customers understand categories.

Examples:

- What are Toxins?
- What are Fillers?
- What are Skin Boosters?
- What are Fat Dissolvers?
- What are Collagen Stimulators?
- What are Clinical Accessories?

These blocks must be careful and non-medical-claim-heavy.

Preferred copy style:

```text
Explore this product category through organized Korean-origin product selections. For product details and availability, contact our support team.
```

Avoid:

- Treatment instructions
- Dosage explanations
- Injection guidance
- Medical advice
- Guaranteed benefits
- Before / after promises

## 17. Product Page Accordions

Product pages may use accordions to keep information organized.

Recommended accordion sections:

- Product Details
- Origin / Authenticity
- Shipping & Availability
- Support
- Wholesale Inquiry
- Related Products

Optional sections if verified:

- Certificate Information
- Product Family
- Storage Notes
- Professional Use Note

Do not invent information to fill accordions.

If data is missing, keep the accordion editable or omit it.

## 18. Professional Use Notes

The store may use “Professional Use” or similar wording only if confirmed.

Possible safe wording:

```text
This product may be intended for professional use. Please review product details and contact us if you have questions before purchasing.
```

Avoid:

- Medical instructions
- Usage directions
- Dosage information
- Treatment advice
- Legal claims
- Country-specific use claims

Suggested metafield:

```text
product.metafields.custom.professional_use_note
```

## 19. Availability and Shipping Blocks

Product pages may include careful availability and shipping notes.

Preferred copy:

```text
Availability may vary by product. Contact us for current product and shipping details.
```

```text
Orders are handled carefully, with product authenticity and proper handling as priorities.
```

Avoid:

- Fastest shipping
- Same-day delivery
- Guaranteed delivery
- Always in stock
- Cold-chain claims unless operationally confirmed
- Storage claims unless verified

## 20. Wholesale Inquiry Blocks

Wholesale is secondary but allowed.

Product pages and footer may include a subtle wholesale inquiry block.

Preferred copy:

```text
Wholesale or business inquiry?
Contact us for product availability and order details.
```

Rules:

- Keep it secondary.
- Do not make the store feel B2B-first.
- Use warm, helpful language.
- Avoid cold distributor-style copy.

Possible placements:

- Product page accordion
- Product page support block
- Footer
- Contact page
- Homepage support section

## 21. Product Family Examples

Codex should understand that some products belong to families.

Examples from current catalog context:

### Botulax Family

- Botulax 100 Units
- Botulax 200 Units
- Botulax 300 Units

### Nabota Family

- Nabota 100 Units
- Nabota 200 Units

### Re N Tox Family

- Re N Tox 100 Units
- Re N Tox 200 Units

### Liztox Family

- Liztox 100 Units
- Liztox 200 Units

### Wondertox Family

- Wondertox 100 Units
- Wondertox 200 Units

### EPTQ Family

- EPTQ S100
- EPTQ S300
- EPTQ S500

### Chaeum Premium Family

- Chaeum Premium 1
- Chaeum Premium 2
- Chaeum Premium 3
- Chaeum Premium 4

### Rejuran Family

- Rejuran I
- Rejuran HB
- Rejuran Healer

These examples are for planning and grouping logic.

Do not hardcode them into templates unless explicitly requested.

## 22. Component Priority

Custom components should be implemented in this order:

1. Product family comparison table
2. Related products / product picker module
3. Authenticity / certificate information block
4. Product page accordions
5. Wholesale inquiry block
6. Category education block
7. Before / after visual block only if verified and requested

Do not implement all custom components at once.

Each component should be created as a small, reviewable task.

## 23. Recommended Implementation Approach

For each custom component, Codex should first output:

1. Component purpose
2. Best data source
3. Required metafields or section settings
4. Files likely affected
5. Risk level
6. Theme editor usability
7. Mobile behavior
8. Testing steps
9. Implementation plan

Only implement after approval.

## 24. Possible Files Involved

Custom component work may involve:

```text
sections/main-product.liquid
sections/featured-collection.liquid
sections/product-recommendations.liquid
sections/related-products.liquid
sections/custom-product-family-table.liquid
sections/custom-authenticity-block.liquid
sections/custom-before-after.liquid
sections/custom-category-education.liquid
snippets/card-product.liquid
snippets/price.liquid
snippets/product-variant-options.liquid
snippets/custom-product-table-row.liquid
assets/base.css
assets/component-card.css
assets/section-main-product.css
assets/component-accordion.css
assets/custom-components.css
templates/product.json
templates/collection.json
config/settings_schema.json
```

Codex must inspect the actual repository before editing because Dawn file names may vary by version.

## 25. Mobile Requirements

All custom components must work well on mobile.

Mobile requirements:

- Tables should not break layout.
- Comparison tables may become stacked cards on mobile.
- Buttons must be tap-friendly.
- Text must remain readable.
- Product names must wrap gracefully.
- Images must not crop badly.
- Accordions should be easy to open.
- Related product cards should not feel crowded.
- Before / after images should stack cleanly if needed.

Preferred mobile strategy for comparison tables:

```text
Desktop: table layout
Mobile: stacked comparison cards or horizontally scrollable table
```

Stacked cards are usually preferred if readability is better.

## 26. Accessibility Requirements

Custom components should support:

- Proper heading hierarchy
- Readable contrast
- Semantic tables when using table data
- Accessible buttons and links
- Descriptive image alt text via Shopify image data or theme settings
- Keyboard-friendly accordion behavior
- Not relying only on color to communicate differences

## 27. Performance Requirements

Custom components should avoid unnecessary complexity.

Prefer:

- CSS-first layout
- Minimal JavaScript
- Shopify-native dynamic data
- Reusable snippets
- Lightweight sections
- Lazy-loaded images when appropriate

Avoid:

- Heavy sliders
- Complex JS frameworks
- Hardcoded repeated markup
- Large external libraries
- Auto-moving carousels
- Performance-heavy animations

## 28. Content Safety Rules

Custom components must follow content safety rules.

Do not create:

- Medical claims
- Treatment promises
- Dosage instructions
- Injection instructions
- Regulatory claims
- Safety guarantees
- Before / after promises
- Clinical performance claims
- Country-specific legal claims
- Product usage protocols

Use neutral product discovery language.

When unsure, ask for confirmation.

## 29. Codex Default Behavior

When asked to create or improve a custom product component, Codex should:

1. Read this file.
2. Read `.ai/catalog-brief.md`.
3. Read `.ai/content-rules.md`.
4. Inspect the relevant Shopify theme files.
5. Propose a safe implementation plan.
6. Avoid hardcoding dynamic product data.
7. Prefer metafields or theme editor blocks.
8. Preserve Shopify product, cart, variant, and app logic.
9. Keep changes small and reviewable.
10. Explain how to test the component in Shopify preview.

## 30. Final Summary

YaksuDerma custom components should help customers compare, understand, and trust products.

They should make the store feel:

- More helpful
- More professional
- More organized
- More premium
- More trustworthy
- Easier to browse

They should not make the store feel:

- Overly technical
- Medical-claim-heavy
- Hardcoded
- Fragile
- Crowded
- Marketplace-like
- Difficult to maintain

Main principle:

> Build custom components that improve product understanding while keeping Shopify data dynamic, content safe, mobile usability strong, and theme editing manageable.
