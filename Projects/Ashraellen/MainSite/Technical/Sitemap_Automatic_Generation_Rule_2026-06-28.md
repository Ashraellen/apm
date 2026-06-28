# Sitemap automatic generation rule

Date: 2026-06-28
Project: Ashraellen MainSite
Status: active technical rule

## Core rule

`sitemap.xml` must be generated automatically.

It must not be maintained manually as a normal workflow step after creating, rotating, archiving or deleting pages.

## Reason

Ashraellen.com has many multilingual static pages and rotating content layers.

Manual sitemap maintenance creates high risk of:

```text
- forgotten URLs
- stale archived URLs
- duplicated entries
- missing language versions
- wrong canonical paths
- broken SEO signals
```

## Expected workflow

When site pages are added or changed:

```text
1. Update the actual HTML/content files.
2. Keep canonical URLs correct inside the pages.
3. Run or trigger the sitemap generator.
4. The generator scans the current site tree and writes sitemap.xml.
5. Do not hand-edit sitemap.xml except for emergency repair.
```

## Generator requirements

The sitemap generator should:

```text
- scan the live static site tree;
- include public HTML pages that should be indexed;
- exclude drafts, backups, system files, assets and private/internal files;
- normalize /index.html URLs to trailing-slash URLs where appropriate;
- preserve the canonical production domain;
- avoid duplicates;
- preferably use file modification time for <lastmod> when reliable;
- be repeatable and safe to run after every content update.
```

## Publication principle

The sitemap is a generated artifact.

Source-of-truth is the actual page tree plus canonical page metadata, not a manually curated URL list.

## Relation to SEO cleanup

Bing or other search engine warnings about duplicate titles/descriptions should be fixed in the page metadata itself, not by manually manipulating the sitemap.

The sitemap can help discovery, but it does not solve duplicate title or duplicate meta description problems.

## Future implementation note

If not already present in the live repository, create a generator script and, preferably, a GitHub Actions workflow or other repeatable command that regenerates sitemap.xml automatically after relevant page changes.
