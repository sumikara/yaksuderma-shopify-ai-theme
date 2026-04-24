# Skill 07 — Product Page Redesign

## 1. Purpose

This skill is used to plan and implement YaksuDerma product page improvements.

Product pages are high-risk and high-value pages because they contain Shopify product form logic, variant logic, dynamic pricing, add-to-cart behavior, app blocks, product information, trust content, and possible custom product components.

This skill comes after:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
04-homepage-redesign.md
05-product-card-redesign.md
06-collection-page-redesign.md
```

Use this skill only after product card and collection page foundations are stable.

Codex must plan before implementation.

Do not edit files unless the user explicitly requests implementation after reviewing the product page plan.

## 2. Required Context Files

Before product page work, Codex must read:

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
.ai/skills/07-product-page-redesign.md
```

Codex should use these files to understand:

- Product catalog complexity
- Product family and unit comparison needs
- Dynamic Shopify data rules
- Content safety boundaries
- Product page UX priorities
- Design system requirements
- Custom component strategy
- Mobile-first requirements
- Product form safety rules

## 3. Product Page Goal

Product pages should help customers evaluate products clearly and confidently.

They should feel:

- Clean
- Trustworthy
- Product-first
- Professional
- Retail-friendly
- Warm and helpful
- Premium but accessible
- Mobile-friendly
- Not claim-heavy
- Not marketplace-like
- Not cold B2B

Product pages should support:

- Exact product names
- Dynamic Shopify prices
- Variant selection
- Product media
- Add-to-cart
- Product information
- Origin/authenticity notes if verified
- Shipping and availability notes
- Support / contact option
- Wholesale inquiry option
- Related products
- Product family comparison tables when useful

## 4. Product Page Must Not Feel Like

Avoid product pages that feel:

- Crowded
- Cold
- Overly clinical
- Marketplace-like
- Discount-first
- Overloaded with claims
- Hard to act on
- Hard to read on mobile
- Generic Dawn default
- Like a risky medical advice page

## 5. Non-Negotiable Shopify Logic Preservation

Codex must preserve:

- Product form logic
- Variant picker logic
- Quantity selector logic
- Add-to-cart behavior
- Dynamic checkout buttons
- Selling plan logic if present
- Product media/gallery behavior
- Product description rendering
- Product availability logic if present
- App blocks
- Shopify product data
- Shopify product URL behavior
- Cart behavior
- Product recommendations if present

Codex must not modify checkout.

Codex must not remove app blocks.

Codex must not hardcode prices.

## 6. Product Data Rules

Product page must use Shopify dynamic product data.

Use/preserve:

```text
product.title
product.price
product.compare_at_price
product.description
product.featured_media
product.media
product.variants
product.selected_or_first_available_variant
product.available
product.url
product.metafields, if available and approved
snippets/price.liquid
product form snippets
buy button snippets
```

Do not hardcode:

- Product prices
- Product availability
- Product descriptions
- Product certificates
- Product claims
- Product image URLs
- Product variant values
- Product family comparison rows unless explicitly approved as temporary manual content

## 7. Product Title Requirements

Product title should remain exact and clear.

Examples:

```text
Botulax 100 Units
Revolax Deep with Lidocaine
Neuramis Deep Lidocaine
J-Cain Cream 10.56% 500g
Liporase inj. / Hyaluronidase
Rejuran Healer
```

Product title should:

- Be prominent
- Be readable on mobile
- Preserve exact Shopify product title
- Not be rewritten into marketing language
- Support long technical names
- Avoid tiny text
- Avoid crowded title/price layout

## 8. Product Price Requirements

Price should be:

- Dynamic from Shopify
- Visible
- Clean
- Calm
- Trustworthy
- Not aggressive
- Not red-heavy
- Easy to compare with product family tables if present

Do not hardcode product prices.

Reference prices in `.ai/catalog-brief.md` are for planning only.

## 9. Product Media Requirements

Product media/gallery should:

- Show product packaging clearly
- Avoid bad cropping
- Support multiple images
- Work well on mobile
- Preserve Dawn media logic
- Preserve alt text behavior
- Load efficiently

Avoid:

- Breaking zoom/gallery behavior
- Cropping packaging too tightly
- Heavy custom gallery JavaScript
- Overly decorative image frames
- Replacing Dawn gallery without a plan

## 10. Variant Picker Requirements

Variant picker is high-risk.

Codex must not break:

- Variant selection
- Variant price updates
- Variant availability updates
- Variant image updates if present
- Add-to-cart state
- Variant URL behavior if Dawn uses it

Allowed improvements:

- Visual spacing
- Label readability
- Button/pill styling
- Mobile tap target improvements
- Error message readability

Avoid:

- Rewriting variant picker logic
- Removing variant picker
- Hardcoding variant values
- Changing variant JavaScript without explicit approval

## 11. Add-to-Cart Requirements

Add-to-cart should be highly visible and trustworthy.

Button should:

- Use approved primary CTA styling
- Be tap-friendly
- Have strong contrast
- Not feel aggressive
- Remain connected to Shopify product form logic

Codex must preserve:

- Add-to-cart form submission
- Dynamic checkout buttons
- Cart drawer/page behavior
- Disabled/unavailable state
- Error handling

Avoid:

- Custom add-to-cart JavaScript unless necessary
- Breaking app blocks
- Removing dynamic checkout buttons without approval
- Replacing product form

## 12. Product Information Hierarchy

Recommended product page hierarchy:

```text
1. Product media gallery
2. Product title
3. Dynamic price
4. Variant picker if applicable
5. Quantity selector
6. Add to cart / dynamic checkout
7. Short support or availability note
8. Product description
9. Accordions
10. Authenticity / origin block if verified or safely generic
11. Related products
12. Product family comparison table when useful
13. Wholesale inquiry block
```

The exact order can be adjusted after inspecting the Dawn product template.

## 13. Product Page Accordions

Accordions can help organize content.

Recommended accordion labels:

```text
Product Details
Origin / Authenticity
Shipping & Availability
Support
Wholesale Inquiry
Related Products
Certificate Information
Product Family
```

Rules:

- Do not fill accordions with invented information.
- Use Shopify product description and metafields where possible.
- Make accordion content editable when possible.
- Keep copy short and safe.
- Avoid medical claims.

Safe copy examples:

```text
Availability may vary by product. Contact us for current product and shipping details.
```

```text
We prioritize original Korean-origin products and clear product information.
```

```text
For certificate or product detail questions, please contact us.
```

## 14. Authenticity / Origin Block

Trust is central to YaksuDerma.

Product pages may include authenticity/origin blocks if safe.

Safe headings:

```text
Original Korean-Origin Products
Authenticity-Focused Product Information
Product Details & Availability
Certificate Information
```

Safe copy:

```text
We prioritize original Korean-origin products and clear product information. Contact us for product details and certificate information where applicable.
```

Do not invent:

- Certificates
- Regulatory approvals
- Manufacturer authorization
- Country-specific legality
- Product safety claims
- Medical approval claims

Preferred data sources:

```text
product.metafields.custom.product_origin
product.metafields.custom.authenticity_note
product.metafields.custom.certificate_note
product.metafields.custom.certificate_image
theme editor settings
```

## 15. Shipping & Availability Block

Product page should avoid overpromising shipping speed.

Safe copy:

```text
Availability may vary by product. Contact us for current product and shipping details.
```

```text
Orders are handled carefully, with product authenticity and proper handling as priorities.
```

Avoid:

```text
Fastest shipping
Same-day delivery
Guaranteed delivery
Always in stock
Cold-chain guaranteed
Delivered tomorrow
```

unless explicitly verified.

## 16. Support Block

Support is a key differentiator.

Suggested heading:

```text
Need help choosing a product?
```

Suggested copy:

```text
Contact us for product details, availability, and order questions.
```

CTA options:

```text
Contact Us
Ask About Availability
Product Questions?
```

Design direction:

- Warm sand / soft beige or pale aqua background
- Short copy
- Calm CTA
- Mobile-friendly
- Helpful and human tone

## 17. Wholesale Inquiry Block

Wholesale is secondary but welcome.

Possible product page block:

```text
Wholesale or business inquiry?
Contact us for product availability and order details.
```

Rules:

- Keep it secondary.
- Do not make product page feel B2B-only.
- Do not hide retail add-to-cart behind wholesale messaging.
- Keep tone warm and helpful.

## 18. Related Products

Related product sections should feel helpful, not instructional.

Preferred labels:

```text
Related products
You may also explore
Often viewed with
Explore related categories
Related accessories
```

Avoid:

```text
Required for treatment
Must be used with
Use this together
Treatment protocol
Procedure bundle
```

Known related-product idea:

```text
Liporase may be recommended as a related product for Dermal & Body Filler products when technically feasible.
```

But do not hardcode this unless explicitly approved.

Preferred data sources:

```text
Shopify product recommendations
product.metafields.custom.related_products
theme editor product picker blocks
collection-based fallback
```

## 19. Product Family Comparison Tables

YaksuDerma may need product family comparison tables.

Examples:

```text
Botulax 100 / 200 / 300 Units
Nabota 100 / 200 Units
Re N Tox 100 / 200 Units
Liztox 100 / 200 Units
Wondertox 100 / 200 Units
EPTQ S100 / S300 / S500
Chaeum Premium 1 / 2 / 3 / 4
Rejuran I / HB / Healer
```

These tables should help customers compare related product options.

Rules:

- Do not hardcode prices.
- Use Shopify dynamic product data where possible.
- Prefer metafields or product picker blocks.
- Mobile should use stacked cards or readable responsive table.
- Do not include treatment claims.
- Do not include dosage instructions.
- Do not include medical outcome columns.

Allowed columns:

```text
Product
Unit / Size
Product Family
Price
Availability
View Product
```

Avoid columns:

```text
Best for wrinkles
Injection area
Expected result
Duration
Dosage
Treatment outcome
```

## 20. Metafield Strategy for Product Page

Codex may propose metafields before implementation.

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
product.metafields.custom.certificate_image
```

Codex should not assume these already exist.

If metafields do not exist, propose:

- Theme editor blocks
- Product picker blocks
- Manual configurable fields
- A phased metafield setup plan

## 21. Before / After Visual Blocks

Before / after blocks are sensitive.

Allowed only if:

- User provides verified images.
- User confirms compliance.
- Copy is neutral.
- Section is optional and configurable.
- No guaranteed result is implied.

Preferred labels:

```text
Visual reference
Product information image
Before / after reference, only if approved
```

Avoid:

```text
Guaranteed transformation
This product creates this result
Instant result
Permanent result
Clinically proven before and after
```

Do not implement before/after sections unless explicitly requested.

## 22. Content Safety Rules

Product page must not include:

- Medical claims
- Treatment promises
- Dosage instructions
- Injection instructions
- Regulatory claims
- Certificate claims unless verified
- Country-specific legal claims
- Safety guarantees
- Guaranteed shipping claims
- “Cheapest” claims
- Fake urgency

Use `.ai/content-rules.md` for all copy.

## 23. Design System Requirements

Product pages must follow `.ai/design-system.md`.

Use:

- Clean white / off-white backgrounds
- Soft turquoise / aqua accents
- Medical blue-green primary CTA
- Trust blue for trust/information
- Warm sand/beige for support sections
- Light borders
- Soft radius
- Minimal shadows
- Clean typography
- Calm section spacing

Avoid:

- Heavy black sections
- Neon colors
- Red-heavy sale design
- Orange CTA buttons
- Too many competing accents
- Crowded product page layout

## 24. Mobile Product Page Requirements

Mobile product page must prioritize:

- Product image clarity
- Product title readability
- Price visibility
- Variant picker usability
- Add-to-cart visibility
- Button tap size
- Accordion readability
- Support/contact access
- Related products readability
- Product comparison table responsiveness
- No horizontal overflow

Mobile comparison tables should use:

```text
Stacked cards
```

or:

```text
Horizontally scrollable table only if readability remains strong
```

Stacked cards are usually preferred.

## 25. Reference Site Usage

Codex may use:

```text
.ai/reference-sites.md
.ai/reference-site-links.md
```

Use references for:

- Product page hierarchy
- Product media layout
- Trust block placement
- Accordion patterns
- Related product layout
- Mobile product page usability

Do not copy:

- Exact layout
- Text
- Images
- Product claims
- Code
- Competitor medical/regulatory claims

## 26. Shopify Implementation Strategy

Preferred approach:

- Preserve Dawn product page structure first.
- Improve layout and styling gradually.
- Use existing product blocks where possible.
- Use theme editor settings where possible.
- Use metafields only after planning.
- Add custom sections only when needed.
- Keep changes small and reviewable.

Do not replace the entire product page template in one step.

## 27. Possible Enhancements

Codex may propose:

```text
Improved media/title/price layout
Better add-to-cart visual hierarchy
Cleaner variant picker styling
Support/availability note
Authenticity information block
Accordion cleanup
Related products section
Product family comparison table
Wholesale inquiry block
Mobile sticky add-to-cart, only if safe and approved
```

Do not implement all enhancements at once.

## 28. Mobile Sticky Add-to-Cart

Mobile sticky add-to-cart may be useful but must be treated carefully.

Codex may propose it only after product page basics are stable.

Rules:

- Must preserve product form logic.
- Must handle variants safely.
- Must not hide required variant selections.
- Must not conflict with dynamic checkout.
- Must not cover important content.
- Must be tested on mobile.

Do not implement mobile sticky add-to-cart without explicit approval.

## 29. Files Likely Involved

Codex must inspect actual repo files.

Likely files:

```text
templates/product.json
sections/main-product.liquid
sections/product-recommendations.liquid
sections/related-products.liquid
snippets/product-media-gallery.liquid
snippets/product-variant-picker.liquid
snippets/buy-buttons.liquid
snippets/price.liquid
snippets/icon-*.liquid
assets/section-main-product.css
assets/component-accordion.css
assets/component-price.css
assets/base.css
assets/product-form.js
assets/global.js
locales/*.json
```

Custom component work may also involve:

```text
sections/custom-product-family-table.liquid
sections/custom-authenticity-block.liquid
sections/custom-before-after.liquid
snippets/custom-product-table-row.liquid
assets/custom-components.css
```

Do not assume every file exists.

Dawn version may vary.

## 30. What Codex Must Preserve

Codex must preserve:

- Product form
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Selling plan logic if present
- Product media gallery
- Product description
- Product price snippet
- Product availability logic
- App blocks
- Product recommendations if present
- Shopify product data
- Existing product template compatibility

## 31. What Codex Must Not Do

During product page work, Codex must not:

- Hardcode product prices
- Hardcode product names
- Hardcode product URLs
- Hardcode certificate claims
- Remove app blocks
- Modify checkout
- Break product form
- Break variant logic
- Break add-to-cart
- Break dynamic checkout buttons
- Remove required product data
- Add medical claims
- Add injection/dosage instructions
- Add before/after claims
- Add quick custom JavaScript without approval
- Replace the whole product page at once
- Copy competitor product pages exactly

## 32. Planning Output Format

Before editing files, Codex must output:

```text
# Product Page Redesign Plan — YaksuDerma

## 1. Files Inspected

List product page-related files inspected.

## 2. Current Product Page Structure

Explain how Dawn currently renders product pages.

## 3. High-Risk Logic Areas

Identify product form, variant picker, cart, dynamic checkout, app-block risks.

## 4. Current Problems / Opportunities

Explain what needs improvement for YaksuDerma.

## 5. Recommended Product Page Layout

Describe proposed layout and hierarchy.

## 6. Trust / Support Content Strategy

Explain safe authenticity, availability, support, and wholesale copy.

## 7. Custom Component Opportunities

Explain whether comparison tables, related products, or authenticity blocks are useful.

## 8. Data Source Strategy

Explain what should come from Shopify product data, metafields, or theme editor blocks.

## 9. Mobile Strategy

Explain mobile product page behavior.

## 10. Files Likely Affected

List files.

## 11. Risks

List risk levels.

## 12. Implementation Phases

Break into small phases.

## 13. First Safe Implementation Step

Recommend exactly one safe next action.
```

## 33. Implementation Output Format

When implementation is requested, Codex must output:

```text
# Product Page Redesign Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. What Changed

Explain product page layout/style/content changes.

## 3. Shopify Logic Preserved

Confirm:
- Product form
- Variant picker
- Quantity selector
- Add-to-cart
- Dynamic checkout buttons
- Selling plan logic if present
- App blocks
- Product data

## 4. Dynamic Data Preserved

Confirm product title, price, image, URL, variants, and availability remain dynamic.

## 5. Design System Alignment

Explain how changes follow `.ai/design-system.md`.

## 6. Content Safety

Confirm no medical/certification/shipping claims were invented.

## 7. Mobile Behavior

Explain mobile product page behavior.

## 8. Risk Level

Low / Medium / High.

## 9. Shopify Preview Test Steps

List test steps.

## 10. Follow-Up Tasks

Recommend next step.
```

## 34. Suggested Implementation Phases

Product page improvements should be implemented in phases:

```text
Phase 1 — Visual hierarchy and spacing
Phase 2 — Price/add-to-cart/variant picker styling
Phase 3 — Accordions and support/availability content
Phase 4 — Authenticity block
Phase 5 — Related products
Phase 6 — Product family comparison table
Phase 7 — Mobile polish
Phase 8 — Theme check / validation
```

Do not implement all phases at once.

## 35. Risk Labels

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

- Product page spacing
- Typography hierarchy
- Accordion styling
- Support block styling
- Static safe copy in configurable blocks

### Medium Risk

- Product template JSON changes
- Adding new product page sections
- Related product section changes
- Product comparison component

### High Risk

- Variant picker logic
- Product form changes
- Add-to-cart JavaScript
- Dynamic checkout changes
- Selling plan logic
- Sticky add-to-cart

### Do Not Touch Yet

- Checkout
- Hardcoded product prices
- Medical claims
- Unverified certificates
- Before/after claims without verified content

## 36. Example Planning Prompt

Use this prompt with Codex:

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

## 37. Example Implementation Prompt

Use this prompt after approving the product page plan:

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

## 38. Final Reminder

Product page work is high-impact and high-risk.

Main principle:

> Improve product clarity, trust, mobile usability, and conversion while preserving Shopify product form, variant, add-to-cart, dynamic price, app block, and cart logic.
