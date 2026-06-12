# Website Asset & Style Consolidation — Planned Technical Action

Status: planned
Created: 2026-06-12
Related website repo: `Ashraellen/ashraellen`
Related memory file: `Projects/Ashraellen/WEB.md`

## Purpose

This planned action records a future cleanup layer for the Ashraellen website: consolidate scattered background images and normalize CSS so the site remains easier to maintain as it grows.

The goal is not to redesign the site, but to reduce technical scattering and prevent future confusion around backgrounds, inline styles and page-specific visual rules.

## Current concern

Background files and visual rules may be spread across the website repository and individual HTML pages.

Risks if left unorganized:

```text
- unclear which background file is canonical;
- duplicate or forgotten background images;
- repeated inline CSS blocks;
- harder future work on Open Graph images and page types;
- greater risk of breaking visual consistency across 9 language versions;
- harder onboarding for future chats / Codex sessions.
```

## Proposed direction

### 1. Consolidate background assets

Create or normalize a central background folder:

```text
assets/backgrounds/
```

Possible structure:

```text
assets/backgrounds/
  ashraellen-home.webp
  ashraellen-research.webp
  ashraellen-professional.webp
  ashraellen-books.webp
  monolith-default.webp
  beton-bg.webp
  sludge-bg.webp
```

or, if the number of files grows:

```text
assets/backgrounds/
  home/
  research/
  professional/
  books/
  monolith/
  public/
  og-source/
```

Important: this must be done only after inventorying current actual usage.

### 2. Keep asset folders conceptually separate

Do not merge these folders conceptually:

```text
assets/backgrounds/  — page backgrounds and source visual material
assets/og/           — Open Graph preview images, 1200x630 or similar social-card formats
assets/icons/        — PWA / installable app icons, favicons, platform icons
assets/covers/       — book covers
```

PWA icons must remain separate from Open Graph images.

### 3. Remove page-level CSS only after mapping

Desired long-term direction:

```text
HTML pages should contain structure and content.
CSS files should contain visual rules.
Background files should live in predictable asset locations.
```

Potential CSS structure:

```text
assets/style.css              — general base / entry pages if already used
assets/styles/home.css        — language entry pages
assets/styles/page.css        — general inner pages
assets/styles/research.css    — research pages
assets/styles/professional.css — professional pages
assets/styles/books.css       — books / book lists
assets/styles/book.css        — individual book pages
assets/styles/monolith.css    — MONOLITH-specific pages
assets/styles/public.css      — public texts / formulas / posts
```

If the existing site already has `assets/books.css` or similar files, do not blindly replace them. First map and then decide whether to preserve, rename or gradually migrate.

## Recommended implementation order

### Phase 1 — Inventory only

Before moving anything, inspect and list:

```text
- all image files used as backgrounds;
- all `background-image` references;
- all inline `<style>` blocks;
- all page-specific CSS rules;
- all references to assets/backgrounds, covers, symbols, icons and OG images;
- all pages that use miniified single-line HTML.
```

Output should be a simple map:

```text
File / asset -> where it is used -> proposed target location -> migration risk
```

### Phase 2 — Background consolidation

After inventory:

```text
1. Create / normalize `assets/backgrounds/`.
2. Move or copy backgrounds into predictable names.
3. Update HTML / CSS references.
4. Keep old files temporarily if needed to avoid breaking pages.
5. Test representative pages in each type and language.
```

Representative pages to check:

```text
/
/en/
/ru/
/pl/
/en/research/
/ru/research/
/en/professional/
/en/books/
/en/books/monolith/
/en/books/monolith/beton/
/ru/books/monolith/beton/
/en/public/
```

### Phase 3 — CSS normalization

Only after backgrounds are stable:

```text
1. Extract repeated inline styles into CSS files.
2. Group CSS by page type, not by language.
3. Keep language-specific differences in content, not style, unless truly required.
4. Avoid page-level CSS when a reusable class or type stylesheet is possible.
5. Remove inline `<style>` blocks gradually.
```

### Phase 4 — Automated protection

Consider adding a future hygiene script to detect:

```text
- href="#"
- src="#"
- inline background-image references outside approved files
- missing canonical
- missing OG tags
- missing JSON-LD
- missing H1
```

This should not be introduced until the current structure is stable.

## Rules and cautions

Do not do this as one large blind rewrite.

Important rules:

```text
1. Inventory first, migration second.
2. Do not break the existing visual identity.
3. Do not move PWA icons into OG or backgrounds.
4. Do not replace successful current OG work.
5. Do not create SEO filler or generic template pages.
6. Keep static HTML metadata intact.
7. Avoid client-side JavaScript for essential structure.
8. Preserve all current canonical / JSON-LD / Open Graph / sitemap / IndexNow automation.
```

## Why this matters

This cleanup will make future development easier:

```text
- easier to create separate OG images;
- easier to maintain page backgrounds;
- easier to add new language pages;
- easier to adjust visual identity consistently;
- easier for future chats and Codex sessions to understand the site;
- lower risk of hidden broken links or stale visual assets.
```

## Priority

Recommended priority:

```text
Medium.
```

Do not interrupt urgent content, grant or legal work for this. Treat it as the next structural website-maintenance layer after the SEO / AI-readiness foundation is stable.
