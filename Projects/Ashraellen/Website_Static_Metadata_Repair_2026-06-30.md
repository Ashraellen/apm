# Ashraellen Website — Static Metadata Repair 2026-06-30

Date: 2026-06-30
Website repository: `Ashraellen/ashraellen`
Memory repository: `Ashraellen/apm`
Live site: `https://www.ashraellen.com/`

This file records the full technical memory of the static metadata repair completed for Ashraellen.com on 2026-06-30.

A parallel maintenance report was also placed inside the website repository:

```text
Ashraellen/ashraellen
reports/apm/2026-06-30-static-metadata-repair.md
```

## Final status

The final metadata audit in the website repository reached:

```text
Pages checked: 550
Pages with issues: 0
Total issues: 0
```

The Google verification HTML file is intentionally excluded from metadata audit because it is a verification file, not a public SEO page.

Remaining review notes are image-review signals only. They are not metadata errors.

## Main purpose of the work

The purpose was to repair the metadata layer of the static multilingual Ashraellen website without adding client-side JavaScript for SEO, metadata, or social-preview correction.

The work repaired:

```text
page titles
meta descriptions
meta keywords
canonical links
Open Graph metadata
Twitter Card metadata
JSON-LD structured data
public identity repetition
metadata duplication
OG image fallback usage
sitemap workflow behavior
maintenance reporting
```

## Core technical rule

The site must remain clean static HTML.

Do not solve metadata, navigation, canonical, image-source, title, language-link, or structured-data problems by adding client-side runtime correction scripts.

Correct approach:

```text
Fix the source HTML, CSS, file paths, metadata and workflow directly.
```

JSON-LD structured data is allowed as:

```html
<script type="application/ld+json">
```

It is structured data for search engines and not runtime JavaScript.

## Root cause

The old GitHub Actions workflow automatically ran metadata generators that rewrote HTML metadata across the site:

```text
scripts/apply-canonical.js
scripts/apply-static-links.js
scripts/apply-jsonld.js
scripts/apply-og.js
scripts/generate-sitemap.js
scripts/submit-indexnow.js
```

The problematic generators were especially:

```text
scripts/apply-jsonld.js
scripts/apply-og.js
```

They inserted broad generic metadata, repeated the same author identity, repeated the same default OG image, and sometimes produced unsuitable generic page schema.

The solution was not to remove sitemap automation, but to stop uncontrolled metadata rewriting and replace it with controlled repair + audit scripts.

## Identity rule fixed

Primary public identity:

```text
Ashraellen
```

Real author name:

```text
Nikolai Kostyshev
```

Rule:

```text
Nikolai Kostyshev is not secret and is not forbidden.
The issue was uncontrolled repetition in ordinary content metadata.
```

Allowed contexts for real name:

```text
biography
professional dossier
contact/about pages
author identity blocks
JSON-LD Person data as alternateName
```

Ordinary pages should normally use Ashraellen as the public identity:

```text
books
research
public text pages
archive pages
multilingual content pages
```

## Fallback OG image rule

Approved fallback image:

```text
https://www.ashraellen.com/assets/og/ashraellen-og-home-default-1200x630.jpg
```

This image is allowed where no better page-specific image, cover, background, or project image exists.

Preferred order:

```text
1. page-specific image / cover / background
2. series-specific or project-specific image
3. approved default Ashraellen OG image
```

Repeated fallback usage is a review signal, not an automatic error.

## Scripts added or updated in the website repository

### `scripts/audit-page-metadata.js`

Creates:

```text
reports/page-metadata-audit.md
```

Checks for:

```text
MISSING_TITLE
MISSING_DESCRIPTION
MISSING_KEYWORDS
MISSING_CANONICAL
MISSING_JSON_LD
MULTIPLE_JSON_LD
MISSING_OG_TITLE
MISSING_OG_DESCRIPTION
MISSING_OG_IMAGE
MISSING_TWITTER_CARD
MISSING_TWITTER_IMAGE
DESCRIPTION_TOO_SHORT
DESCRIPTION_TOO_LONG
REAL_NAME_ON_ORDINARY_CONTENT_PAGE
DUPLICATE_TITLE
DUPLICATE_DESCRIPTION
DUPLICATE_KEYWORDS
DUPLICATE_CANONICAL
DUPLICATE_OG_TITLE
DUPLICATE_OG_DESCRIPTION
```

Also records review notes for fallback/shared OG and Twitter images.

Google verification files are skipped.

### `scripts/export-page-keyword-workbench.js`

Creates:

```text
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
```

Purpose: page-by-page keyword review map.

### `scripts/add-missing-keywords.js`

Adds missing static:

```html
<meta name="keywords" content="...">
```

This removed the original mass issue where all pages were missing keywords.

### `scripts/clean-public-identity-head.py`

Replaces uncontrolled `Nikolai Kostyshev` inside `<head>` on ordinary content pages with `Ashraellen`.

Scope:

```text
books
research
public
```

Does not treat identity pages as ordinary content.

### `scripts/repair-title-description-og.py`

Repairs and deduplicates:

```text
title
meta description
og:title
og:description
twitter:title
twitter:description
```

### `scripts/repair-structured-social-gaps.py`

Repairs missing structured/social metadata:

```text
JSON-LD
OG image
Twitter image
Twitter card
canonical
title
description
keywords
OG title
OG description
```

### `scripts/dedupe-page-metadata.py`

Final deduplication pass for repeated titles, descriptions, OG descriptions and keywords.

Uses page-path context to make similar pages unique.

### `scripts/apply-og-from-page-backgrounds.py`

Uses page background images as OG/Twitter images where possible.

Detects:

```text
inline background-image declarations
inline background url(...) declarations
known class-based CSS backgrounds
```

Known background mappings:

```text
assets/hero.webp
assets/backgrounds/books-bg.webp
assets/backgrounds/monolith-bg.webp
assets/backgrounds/online-bg.jpg
assets/backgrounds/whinesis-bg.jpg
```

Creates:

```text
reports/page-backgrounds.md
```

If no background image exists, keeps the approved fallback image.

## Current workflow order

Website workflow:

```text
.github/workflows/sitemap.yml
```

Current order after repair:

```text
1. Add missing static keywords
2. Clean public identity in ordinary page metadata
3. Repair title description and OG metadata
4. Repair structured data and social gaps
5. Dedupe page metadata
6. Apply OG images from page backgrounds
7. Audit page metadata
8. Export page keyword workbench
9. Generate sitemap.xml
10. Submit sitemap URLs to IndexNow
11. Commit repaired HTML, sitemap.xml and reports if changed
```

The workflow commits:

```text
**/*.html
sitemap.xml
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
reports/page-backgrounds.md
```

## Reports in website repository

### `reports/page-metadata-audit.md`

Main metadata audit report.

Desired state:

```text
Pages with issues: 0
Total issues: 0
```

### `reports/page-keyword-workbench.md`

Human-readable keyword review workbench.

### `reports/page-keyword-workbench.json`

Machine-readable keyword review workbench.

### `reports/page-backgrounds.md`

Mapping of pages to selected OG/Twitter image sources.

## Progress summary

Issue counts moved through this sequence:

```text
1604 → 584 → 126 → 80 → 0
```

Main repairs:

```text
MISSING_KEYWORDS: 551 → 0
REAL_NAME_ON_ORDINARY_CONTENT_PAGE: 500 → 0
MISSING_JSON_LD: 23 → 0
MISSING_OG_IMAGE: 5 → 0
MISSING_TWITTER_CARD: 5 → 0
MISSING_TWITTER_IMAGE: 5 → 0
DUPLICATE_TITLE: resolved
DUPLICATE_DESCRIPTION: resolved
DUPLICATE_KEYWORDS: resolved
DUPLICATE_OG_TITLE: resolved
DUPLICATE_OG_DESCRIPTION: resolved
```

## OG image result

After applying page background images, some pages now use actual background assets.

Examples:

```text
be/books/index.html
og:image -> assets/backgrounds/books-bg.webp

be/books/monolith/beton/index.html
og:image -> assets/backgrounds/monolith-bg.webp
```

Pages without a specific background still use the approved common fallback.

## Important future warning

Do not re-enable broad site-wide metadata generators that blindly overwrite page-level metadata.

Future metadata changes should be:

```text
page-specific and intentional
or
controlled by repair scripts with audit reports
```

Sitemap automation should remain active.

Do not add client-side JavaScript to generate, repair or rewrite SEO/social metadata.

## Recommended next stage

The emergency metadata repair is complete.

Future work is quality improvement:

```text
1. Create stronger page-specific OG images for important pages.
2. Improve individual descriptions for high-value pages.
3. Replace fallback images only where a better project-specific visual exists.
4. Continue running the audit after major structural changes.
5. Refactor older inline CSS and runtime link scripts only through direct static HTML/CSS improvements, not patches.
```
