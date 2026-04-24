# Navigation Brief — YaksuDerma

## 1. Purpose

This file defines the navigation strategy for the YaksuDerma Shopify theme.

Codex should use this file when working on:

- Header layout
- Main menu
- Dropdown logic
- Mobile menu
- Footer navigation
- Collection links
- Category cards
- Wholesale / contact links
- Homepage category showcase

Navigation must stay clean, product-focused, SEO-friendly, retail-friendly, and easy to use on mobile.

This file should be read together with:

- `.ai/codex-instructions.md`
- `.ai/brand-brief.md`
- `.ai/store-brief.md`
- `.ai/catalog-brief.md`
- `.ai/design-system.md`

## 2. Navigation Goal

The navigation should help users quickly understand:

1. What YaksuDerma sells
2. Which main product categories exist
3. How to browse products directly
4. How to understand the product catalog without confusion
5. How to find support or business inquiry paths when needed

Navigation should feel:

- Clean
- Product-first
- Retail-friendly
- Professional
- Mobile-first
- Easy to scan
- Not crowded
- Not like a cold B2B distributor portal

## 3. Final Top-Level Header Navigation

Use this top-level navigation structure:

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

This is the preferred visible header menu.

Do not replace this with a generic “Shop” dropdown unless explicitly requested.

## 4. Product Category Mapping

The visible menu labels should be short and retail-friendly, while collection page titles should remain SEO-friendly and professional.

| Header Label | Full Collection / Page Title | Suggested Handle |
|---|---|---|
| Home | Homepage | `/` |
| Toxins | Botulinum Toxins | `botulinum-toxins` |
| Fillers | Dermal & Body Fillers | `dermal-body-fillers` |
| Skin Boosters | Skin Boosters & Exosomes | `skin-boosters-exosomes` |
| Fat Dissolvers | Mesotherapy & Contouring | `mesotherapy-contouring` |
| Collagen Stimulators | Collagen Stimulators | `collagen-stimulators` |
| Accessories | Clinical Accessories & IV Therapy | `clinical-accessories-iv-therapy` |
| About | About YaksuDerma | `about` |

Use short labels in the header for visual clarity.

Use the fuller collection names on collection pages, SEO titles, meta titles, category cards, and structured content when helpful.

## 5. Header Label Rules

Use short, clear labels in the visible header.

Preferred visible labels:

- Home
- Toxins
- Fillers
- Skin Boosters
- Fat Dissolvers
- Collagen Stimulators
- Accessories
- About

These labels are intentionally shorter than the full collection names.

Use:

```text
Toxins
```

instead of:

```text
Botulinum Toxins
```

in the main header.

Use:

```text
Fillers
```

instead of:

```text
Dermal & Body Fillers
```

Use:

```text
Skin Boosters
```

instead of:

```text
Skin Boosters & Exosomes
```

Use:

```text
Fat Dissolvers
```

instead of:

```text
Mesotherapy & Contouring
```

Use:

```text
Accessories
```

instead of:

```text
Clinical Accessories & IV Therapy
```

The full SEO/category names can still be used on collection pages, page titles, meta titles, category cards, and structured content.

## 6. Fillers Dropdown

The `Fillers` menu item may either link directly to the main Fillers collection or open a dropdown.

Preferred dropdown structure:

```text
Fillers
  Dermal Fillers
  Body Fillers
```

Dropdown rules:

- Keep it short.
- Do not add too many subcategories.
- Do not use medical-claim language.
- Keep labels product/category-based.
- Use Shopify navigation/admin-managed menus where possible.

If no dropdown is implemented yet, `Fillers` should link to the main Dermal & Body Fillers collection.

## 7. Accessories Dropdown

The `Accessories` menu item may either link directly to the main Accessories collection or open a dropdown.

Optional dropdown structure:

```text
Accessories
  Numbing Creams
  IV Therapy
  Dissolvers
  Clinical Accessories
```

Dropdown rules:

- Use only if it improves browsing.
- Keep it compact.
- Do not make the header feel like a complex distributor catalog.
- Avoid medical-use instructions.
- Avoid unverified claims.

If no dropdown is implemented yet, `Accessories` should link to the main Clinical Accessories & IV Therapy collection.

## 8. Toxins Navigation

Use the visible header label:

```text
Toxins
```

This menu item should map to the full collection/page title:

```text
Botulinum Toxins
```

Reason:

- “Toxins” is shorter and cleaner in the header.
- “Botulinum Toxins” is more professional and SEO-friendly on the collection page.
- The category is one of the most commercially important product groups.
- It should be immediately visible in the main menu.

Do not use “Botox” in the main navigation unless explicitly requested.

Avoid:

```text
Botox Deals
Cheap Botox
Wrinkle Injections
Treatment Toxins
```

## 9. Skin Boosters Navigation

Use the visible label:

```text
Skin Boosters
```

This menu item should map to:

```text
Skin Boosters & Exosomes
```

Reason:

- “Skin Boosters” is shorter and easier to scan in header navigation.
- Exosome products can live inside this broader category.
- The collection page title can use the fuller SEO phrase.

## 10. Fat Dissolvers Navigation

Use the visible header label:

```text
Fat Dissolvers
```

This menu item should map to the broader collection/page title:

```text
Mesotherapy & Contouring
```

Alternative collection page title if preferred:

```text
Fat Dissolvers & Contouring
```

Reason:

- “Fat Dissolvers” is clearer and more commercial for customers.
- It directly matches a high-interest product category.
- It is easier to understand than “Mesotherapy & Contouring” in the header.
- The fuller category language can still be used for SEO and collection page content.

Avoid:

```text
Fat Loss Injections
Weight Loss Shots
Slimming Miracles
Guaranteed Contouring
Instant Fat Removal
```

Use neutral product-category language and avoid treatment/result claims.

## 11. Collagen Stimulators Navigation

Use the visible label:

```text
Collagen Stimulators
```

This category can remain top-level because it is specific and commercially meaningful.

Collagen Stimulators should not be merged into Fat Dissolvers unless the user explicitly changes the catalog architecture later.

Reason:

- Products such as Aesthefill, Etrebelle, Power Coltra, and Richesse PCL are commercially different from fat dissolvers.
- This category can feel more premium and specialist.
- Keeping it separate prevents catalog confusion.

Avoid making it too technical in the header.

## 12. About Navigation

`About` should remain in the top-level header.

The About page should support:

- Brand story
- Trust
- Korean-origin product positioning
- Fair pricing philosophy
- Customer support approach
- Authenticity focus

Do not overload About with product categories.

## 13. Contact and Wholesale Placement

Contact and Wholesale Inquiry should be accessible but do not need to be primary desktop header items.

Recommended placement:

- Footer
- Mobile menu
- Homepage support section
- Product page support note
- Contact page
- Optional announcement/support bar later

Mobile menu may include:

```text
Contact
Wholesale Inquiry
```

Footer should include:

```text
Contact
Wholesale Inquiry
Shipping Information
Authenticity / Certificates
Policies
```

Do not make wholesale dominate the retail shopping experience.

## 14. Mobile Navigation Structure

Recommended mobile menu order:

```text
Home
Toxins
Fillers
  Dermal Fillers
  Body Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
  Numbing Creams
  IV Therapy
  Dissolvers
  Clinical Accessories
About
Contact
Wholesale Inquiry
```

If nested mobile menus feel too complex, use this simpler version:

```text
Home
Toxins
Fillers
Skin Boosters
Fat Dissolvers
Collagen Stimulators
Accessories
About
Contact
Wholesale Inquiry
```

Mobile priority:

- Easy tapping
- Readable labels
- No tiny text
- No deep nested menus unless necessary
- Clear category access
- Search and cart preserved

## 15. Homepage Category Showcase

Homepage should show the main category structure using product-first labels.

Recommended homepage category cards:

1. Toxins
2. Fillers
3. Skin Boosters
4. Fat Dissolvers
5. Collagen Stimulators
6. Accessories

Optional card subtitles:

### Toxins

Botulinum toxin product category.

### Fillers

Dermal and body filler selections.

### Skin Boosters

Skin booster, PDRN, and exosome categories.

### Fat Dissolvers

Lipolytic and contouring product categories.

### Collagen Stimulators

Biostimulator and collagen stimulator selections.

### Accessories

Numbing creams, dissolvers, IV-related products, and support items.

Avoid treatment promises and medical claims in category card text.

## 16. Footer Navigation

Footer should support product discovery, trust, policies, and contact.

Recommended footer groups:

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

Footer should be structured but not overloaded.

## 17. Search Navigation

Search should remain available and easy to access.

The catalog contains many technical product names, so search is important.

Search UX should support:

- Exact product names
- Long names
- Unit-based names
- Brand/family names
- Product category terms

Do not remove or hide Shopify search unless a better replacement exists.

## 18. Product Discovery Paths

Navigation should support three discovery paths.

### Path 1 — Category-first

```text
Home → Toxins → Botulinum Toxins collection → Product
```

```text
Home → Fillers → Dermal Fillers → Product
```

```text
Home → Fat Dissolvers → Mesotherapy & Contouring collection → Product
```

### Path 2 — Search-first

```text
Search → “Botulax 100 Units” → Product
```

### Path 3 — Support-first

```text
Home → Need Help? → Contact
```

The theme should support all three.

## 19. SEO Navigation Rules

Visible header labels can be shorter, but SEO/category page titles should remain clear and searchable.

Examples:

Visible header:

```text
Toxins
```

Collection title:

```text
Botulinum Toxins
```

Visible header:

```text
Fillers
```

Collection title:

```text
Dermal & Body Fillers
```

Visible header:

```text
Skin Boosters
```

Collection title:

```text
Skin Boosters & Exosomes
```

Visible header:

```text
Fat Dissolvers
```

Collection title:

```text
Mesotherapy & Contouring
```

Visible header:

```text
Accessories
```

Collection title:

```text
Clinical Accessories & IV Therapy
```

Avoid decorative category names that reduce search clarity.

Do not use:

- Glow Essentials
- Beauty Lab
- Magic Treatments
- Youth Solutions
- Miracle Products
- Secret Formula

## 20. Header Design Requirements

Header should feel:

- Clean
- Premium
- Product-first
- Lightweight
- Not marketplace-like
- Not too tall
- Not visually heavy
- Easy to scan

Header should include:

- Logo / brand name
- Main menu
- Search
- Account icon if enabled
- Cart icon
- Mobile menu icon

Do not remove Shopify cart or search logic.

## 21. Menu Label Rules

Use short and clear labels.

Preferred:

- Home
- Toxins
- Fillers
- Skin Boosters
- Fat Dissolvers
- Collagen Stimulators
- Accessories
- About

Avoid:

- Very long menu labels
- Technical jargon in top nav
- Duplicate links
- Too many top-level items
- Emotional category names
- Treatment-result category names

## 22. Trust Links

Trust-related pages may be linked in footer, homepage support sections, or About page.

Possible trust links:

- Authenticity
- Certificates
- Product Availability
- Shipping Information
- Contact
- About YaksuDerma

Do not create certificate or approval pages unless content is verified by the user.

## 23. Codex Implementation Rules

When Codex edits navigation-related theme files:

- Preserve Shopify menu settings where possible.
- Prefer Shopify navigation/admin-managed menus rather than hardcoded navigation.
- Do not hardcode collection URLs unless explicitly requested.
- Prefer configurable section settings and menu references.
- Preserve mobile menu behavior.
- Preserve cart/search/account icons.
- Preserve app blocks.
- Keep header and footer editable from Shopify theme editor where possible.
- Make small, reviewable changes.

## 24. Files Likely Involved

Navigation-related Shopify Dawn files may include:

```text
sections/header.liquid
sections/footer.liquid
snippets/header-drawer.liquid
snippets/header-mega-menu.liquid
snippets/header-dropdown-menu.liquid
snippets/icon-*.liquid
assets/base.css
assets/component-menu-drawer.css
assets/component-mega-menu.css
config/settings_schema.json
```

Codex must inspect the actual repository before editing because file names may vary by Dawn version.

## 25. Navigation Summary

Final preferred visible desktop navigation:

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

Full collection/page title mapping:

```text
Toxins → Botulinum Toxins
Fillers → Dermal & Body Fillers
Skin Boosters → Skin Boosters & Exosomes
Fat Dissolvers → Mesotherapy & Contouring
Collagen Stimulators → Collagen Stimulators
Accessories → Clinical Accessories & IV Therapy
```

Optional dropdowns:

```text
Fillers
  Dermal Fillers
  Body Fillers
```

```text
Accessories
  Numbing Creams
  IV Therapy
  Dissolvers
  Clinical Accessories
```

Main principle:

> Keep navigation short in the header, but keep collection titles professional, SEO-friendly, and clear on category pages.
