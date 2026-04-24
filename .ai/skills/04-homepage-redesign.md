# Skill 04 — Homepage Redesign

## 1. Purpose

This skill is used to plan and implement the YaksuDerma homepage redesign.

This skill comes after:

```text
01-theme-audit.md
02-design-system-planning.md
03-css-refactor.md
```

Use this skill only after the clean Dawn structure has been audited and the design-system foundation has been planned or partially implemented.

The homepage must communicate trust, product category clarity, Korean-origin product focus, fair pricing, and helpful customer support.

Codex must plan before implementation.

Do not edit files unless the user explicitly requests implementation after reviewing the homepage plan.

## 2. Required Context Files

Before homepage work, Codex must read:

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
.ai/skills/04-homepage-redesign.md
```

Codex should use these files to understand:

- Brand positioning
- Store strategy
- Final navigation labels
- Product category structure
- Color and design system
- Content safety rules
- Homepage copy tone
- Reference site usage rules
- Shopify implementation constraints

## 3. Homepage Goal

The homepage should answer these questions quickly:

1. What does YaksuDerma sell?
2. Why should customers trust the store?
3. Are the products Korean-origin?
4. Are products original/authenticity-focused?
5. Are prices fair and accessible?
6. What are the main categories?
7. How can customers get help?
8. Are wholesale or business inquiries possible?

The homepage should feel:

- Clean
- Trustworthy
- Product-first
- Korean-inspired
- Warm and helpful
- Retail-friendly
- Premium but accessible
- Mobile-first
- Not marketplace-like
- Not cold B2B

## 4. Homepage Must Not Feel Like

Avoid creating a homepage that feels like:

- A generic Dawn homepage
- A cheap discount marketplace
- A cold distributor portal
- A single-banner landing page
- A medical claims website
- A luxury brand with no product clarity
- A crowded product warehouse
- An aggressive sales funnel

## 5. Recommended Homepage Section Flow

Recommended homepage structure:

```text
1. Hero section
2. Trust / authenticity bar
3. Category showcase
4. Featured collection or featured products
5. Why YaksuDerma / value proposition
6. Customer support section
7. Optional wholesale inquiry section
8. Footer trust links
```

This order can be adjusted after inspecting the actual Dawn homepage structure, but the homepage should not rely only on a single hero banner.

## 6. Hero Section Requirements

The hero section should communicate YaksuDerma’s core value proposition.

Hero should include:

- Clear headline
- Short supporting text
- Primary CTA
- Secondary CTA
- Optional product/category visual
- Clean layout
- Mobile-readable text
- No crowded overlay text on busy images

Recommended hero direction:

```text
Authentic Korean-Origin Aesthetic Products
```

Supporting copy example:

```text
Explore trusted product categories with fair pricing, clear information, and helpful support.
```

Primary CTA examples:

```text
Explore Products
Shop Categories
Browse Collections
```

Secondary CTA examples:

```text
Contact Us
Ask About Availability
Wholesale Inquiry
```

Avoid hero copy such as:

```text
Guaranteed Results
Cheap Botox Online
Instant Transformation
Fastest Shipping
Miracle Beauty Treatments
```

## 7. Trust / Authenticity Bar

The homepage should include a short trust bar or trust row.

Possible trust points:

```text
Original Product Focus
Korean-Origin Products
Fair Pricing
Helpful Support
Carefully Handled Orders
```

Rules:

- Keep text short.
- Do not invent certificates.
- Do not claim regulatory approvals.
- Do not claim fastest shipping.
- Do not make medical claims.
- Use neutral and trust-building wording.

Design direction:

- Soft aqua, trust-blue-soft, or neutral background
- Small icons optional
- Light borders
- Mobile stacked layout if needed

## 8. Category Showcase

The homepage must show the final product category structure.

Use the visible labels from `.ai/navigation-brief.md`:

```text
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
```

Category card mapping:

```text
Toxins → Botulinum Toxins
Fillers → Dermal & Body Fillers
Skin Boosters → Skin Boosters & Exosomes
Fat Dissolvers → Mesotherapy & Contouring
Collagen Stimulators → Collagen Stimulators
Accessories → Clinical Accessories & IV Therapy
```

Category cards should:

- Link to collection pages.
- Use clean visuals.
- Use short descriptions.
- Be editable from Shopify theme editor where possible.
- Work well on mobile.
- Avoid medical claims.
- Avoid clutter.

Suggested section headings:

```text
Shop by Category
Explore Product Categories
Browse Korean-Origin Aesthetic Products
```

## 9. Category Card Copy

Safe category card subtitles:

### Toxins

```text
Botulinum toxin product category.
```

### Fillers

```text
Dermal and body filler selections.
```

### Skin Boosters

```text
Skin booster, PDRN, and exosome categories.
```

### Fat Dissolvers

```text
Lipolytic and contouring product categories.
```

### Collagen Stimulators

```text
Biostimulator and collagen stimulator selections.
```

### Accessories

```text
Numbing creams, dissolvers, IV-related products, and support items.
```

Avoid:

- Treatment promises
- Dosage claims
- Injection guidance
- Guaranteed results
- Medical outcome language

## 10. Featured Collection / Featured Products

Homepage may include a featured collection or featured products section.

Preferred approach:

- Use Shopify featured collection section where possible.
- Use collection picker or product picker settings.
- Pull product titles, prices, images, and links dynamically.
- Do not hardcode prices.
- Do not hardcode product cards.
- Do not hardcode inventory.

Recommended initial featured collection options:

```text
Toxins / Botulinum Toxins
Fillers / Dermal & Body Fillers
Skin Boosters / Skin Boosters & Exosomes
```

Commercially important products from catalog context may include:

```text
Botulax 100 Units
Botulax 200 Units
Innotox 100 Units
Re N Tox 100 Units
Revolax Deep with Lidocaine
Neuramis Deep Lidocaine
Rejuran Healer
Lipo Lab PPC Solution
J-Cain Cream 10.56% 500g
S-Cain Cream 10.56% 500g
```

These are planning references only.

Do not hardcode these products into the homepage unless explicitly requested.

## 11. Why YaksuDerma / Value Proposition Section

Homepage should include a section explaining why customers may choose YaksuDerma.

Safe value points:

```text
Authentic Korean-origin product focus
Fair pricing approach
Helpful customer support
Organized product categories
Carefully handled orders
Business inquiries welcome
```

Possible section heading:

```text
Why YaksuDerma?
```

Safe copy direction:

```text
YaksuDerma focuses on clear product discovery, original Korean-origin products, fair pricing, and helpful support before and after purchase.
```

Avoid:

```text
We guarantee the best results.
We are the cheapest in the market.
All products are globally certified.
Fastest shipping worldwide.
```

## 12. Customer Support Section

Support is a core differentiator.

Homepage should include a warm support block.

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

- Warm sand / soft beige background
- Calm layout
- Human and helpful tone
- Not overly corporate
- Not aggressive

## 13. Wholesale Inquiry Section

Wholesale is secondary but welcome.

The homepage may include a subtle wholesale inquiry section.

Suggested heading:

```text
Wholesale or business inquiry?
```

Suggested copy:

```text
Business inquiries are welcome. Contact us for product availability and order details.
```

CTA:

```text
Wholesale Inquiry
Contact Us
```

Rules:

- Keep wholesale secondary.
- Do not make the homepage feel B2B-first.
- Do not make the site feel trade-only.
- Keep retail shopping experience primary.

## 14. Homepage Content Safety Rules

Homepage must not include:

- Medical claims
- Treatment promises
- Before/after claims
- Dosage instructions
- Injection instructions
- Regulatory claims
- Certificate claims unless verified
- Country-specific legal claims
- Safety guarantees
- Guaranteed shipping claims
- “Cheapest” claims
- Fake urgency

Use `.ai/content-rules.md` for all copywriting decisions.

## 15. Design System Requirements

Homepage must follow `.ai/design-system.md`.

Use:

- White / off-white backgrounds
- Soft turquoise / aqua accents
- Medical blue-green CTA
- Trust blue for trust/information
- Warm sand / beige for support sections
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
- Crowded section layouts

## 16. Mobile Homepage Requirements

Mobile homepage must prioritize:

- Clear hero text
- Easy CTA taps
- Quick category discovery
- Readable category cards
- Product cards that do not feel crowded
- Trust bar that stacks cleanly
- Support/contact section visibility
- No text overflow
- No image cropping issues
- No horizontal scrolling

Mobile section order should remain logical:

```text
Hero
Trust bar
Categories
Featured products/collection
Why YaksuDerma
Support
Wholesale optional
Footer
```

## 17. Reference Site Usage

Codex may use:

```text
.ai/reference-sites.md
.ai/reference-site-links.md
```

Use references for:

- Homepage hierarchy
- Clean product discovery
- Trust bar placement
- Category card ideas
- Product section rhythm
- Mobile section flow

Do not copy:

- Exact layout
- Exact text
- Images
- Claims
- Code
- Brand identity

## 18. Shopify Implementation Strategy

Homepage implementation should prefer:

- Existing Dawn sections where suitable
- New reusable custom sections only when needed
- Theme editor settings
- Section blocks
- Collection pickers
- Product pickers
- Image pickers
- Dynamic Shopify data

Do not hardcode:

- Product prices
- Product URLs
- Product cards
- Product availability
- Certificate claims
- Regulatory claims

## 19. Possible New Custom Sections

Codex may propose these, but should not create all at once:

```text
custom-hero.liquid
custom-trust-bar.liquid
custom-category-showcase.liquid
custom-support-block.liquid
custom-wholesale-inquiry.liquid
custom-authenticity-block.liquid
```

Each section should:

- Be reusable
- Be editable from Shopify theme editor
- Use safe default copy
- Have mobile-friendly schema/settings
- Avoid hardcoded product data
- Avoid medical claims

## 20. Existing Dawn Sections to Consider

Codex should inspect whether these can be reused:

```text
image-banner
rich-text
multicolumn
featured-collection
collage
image-with-text
slideshow
```

Prefer reusing existing Dawn sections when they can achieve the goal cleanly.

Create custom sections only if Dawn’s existing sections are insufficient.

## 21. Files Likely Involved

Homepage redesign may involve:

```text
templates/index.json
sections/image-banner.liquid
sections/featured-collection.liquid
sections/multicolumn.liquid
sections/rich-text.liquid
sections/image-with-text.liquid
sections/custom-hero.liquid
sections/custom-trust-bar.liquid
sections/custom-category-showcase.liquid
sections/custom-support-block.liquid
snippets/card-product.liquid
snippets/price.liquid
assets/base.css
assets/component-card.css
assets/section-image-banner.css
config/settings_schema.json
```

Codex must inspect actual files because Dawn version may vary.

## 22. Homepage Plan Output Format

Before editing files, Codex must output:

```text
# Homepage Redesign Plan — YaksuDerma

## 1. Files Inspected

List files inspected and why they matter.

## 2. Current Homepage Structure

Explain current sections and template structure.

## 3. Homepage UX Gaps

Explain what Dawn lacks for YaksuDerma.

## 4. Proposed Section Flow

List recommended homepage section order.

## 5. Existing Dawn Sections to Reuse

List reusable sections.

## 6. New Custom Sections Needed

List only if necessary.

## 7. Dynamic Data Strategy

Explain how products, collections, prices, images, and links remain dynamic.

## 8. Copy Strategy

Suggest safe copy direction based on content rules.

## 9. Mobile Strategy

Explain mobile behavior.

## 10. Files Likely Affected

List files.

## 11. Risks

List risk levels.

## 12. Implementation Phases

Break into small phases.

## 13. First Safe Implementation Step

Recommend exactly one next action.
```

## 23. Homepage Implementation Output Format

When implementation is requested, Codex must output:

```text
# Homepage Redesign Implementation — YaksuDerma

## 1. Files Changed

List changed files.

## 2. What Changed

Explain section/template/style changes.

## 3. Why It Changed

Tie changes to briefs and design system.

## 4. Shopify Data Preserved

Confirm dynamic collections/products/prices remain dynamic.

## 5. Theme Editor Controls

Explain what the store owner can edit.

## 6. Mobile Behavior

Explain mobile layout.

## 7. Content Safety

Confirm no medical/certification/shipping claims were invented.

## 8. Risk Level

Low / Medium / High.

## 9. Shopify Preview Test Steps

List test steps.

## 10. Follow-Up Tasks

Recommend next step.
```

## 24. Suggested Implementation Phases

Homepage should be implemented in phases:

```text
Phase 1 — Hero + trust bar plan/implementation
Phase 2 — Category showcase
Phase 3 — Featured collection/product section refinement
Phase 4 — Why YaksuDerma / value proposition section
Phase 5 — Support + wholesale inquiry sections
Phase 6 — Mobile polish
Phase 7 — Theme check / validation
```

Do not implement all phases at once unless explicitly requested.

## 25. Risk Labels

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

- Updating homepage JSON section order
- Adding safe rich text content
- Styling a custom trust bar
- Creating a category showcase section with configurable links

### Medium Risk

- Creating new custom Liquid sections
- Changing featured collection markup
- Adjusting product card styling used globally

### High Risk

- Changing product card logic used across the store
- Changing dynamic product data
- Editing global CSS too broadly

### Do Not Touch Yet

- Checkout
- Product form logic
- Cart logic
- App blocks
- Hardcoded product prices
- Medical/regulatory claims

## 26. What Codex Must Not Do

During homepage work, Codex must not:

- Hardcode product prices
- Hardcode product availability
- Hardcode certificate claims
- Invent medical claims
- Remove app blocks
- Modify checkout
- Break product card dynamic data
- Copy reference site layouts exactly
- Replace final navigation structure with generic “Shop”
- Make wholesale the primary homepage message
- Add heavy animations or performance-heavy sliders
- Implement every homepage idea in one commit

## 27. Example Planning Prompt

Use this prompt with Codex:

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

## 28. Example Implementation Prompt

Use this after approving the homepage plan:

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

## 29. Final Reminder

Homepage is the first major customer impression.

Main principle:

> Make YaksuDerma’s homepage communicate trust, Korean-origin product focus, fair pricing, category clarity, and helpful support — without hardcoding product data or making risky claims.
