# Focus Group Books Area Rule

Date: 2026-07-01
Project: Ashraellen / MainSite
Status: active operational rule

## Context

A dedicated public-but-unlisted area was created in the live site repository for sharing PDF reading copies with selected focus-group readers.

Live repository path:

```text
focus-group/books/
```

Initial book-specific folder:

```text
focus-group/books/beton-pl/
```

Initial PDF reading copy:

```text
focus-group/books/beton-pl/beton-pl-2026-03-21-pz.pdf
```

## Decision

The `/focus-group/` area is an unlisted reading-copy distribution area, not a public navigation section of the Ashraellen site.

It may be used for direct-link PDF sharing with selected readers, reviewers, focus-group participants, editors, or trusted contacts.

## Operational rules

- Do not add `/focus-group/` to public menus, language navigation, book indexes, public archive pages, or homepage cards unless a separate explicit command approves it.
- Do not create public landing pages inside `/focus-group/` unless a separate explicit command approves it.
- Do not add `/focus-group/` to sitemap manually.
- Keep PDF files in this area direct-link only.
- Prefer clean lowercase filenames with hyphens and no spaces or parentheses.
- Treat this area as public-by-URL, not private or password-protected.

## Robots / indexing rule

The live `robots.txt` should include:

```text
User-agent: *
Disallow: /focus-group/
Allow: /

Sitemap: https://www.ashraellen.com/sitemap.xml
```

This asks compliant crawlers not to crawl `/focus-group/`.

Important: `robots.txt` is not access control. Anyone with the direct URL may still be able to open the PDF.

## Sitemap rule

The current sitemap workflow is HTML-oriented. PDF files in `/focus-group/books/` should not be expected to appear in `sitemap.xml`.

If any `.html` page is later created inside `/focus-group/`, it must be reviewed before sitemap generation because it may become discoverable through the automatic sitemap workflow.

## Current public direct link

```text
https://www.ashraellen.com/focus-group/books/beton-pl/beton-pl-2026-03-21-pz.pdf
```

## Not approved by this decision

- Public launch of a focus-group portal.
- Adding focus-group links to visible site navigation.
- Adding focus-group URLs to sitemap.
- Treating this location as confidential storage.
- Uploading private, confidential, legally restricted, or not-ready-for-public-access files.
