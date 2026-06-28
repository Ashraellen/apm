# Sitemap automatic generation rule

Date: 2026-06-28
Project: Ashraellen MainSite
Status: active technical rule

## Core rule

`sitemap.xml` is already generated automatically and must continue to be treated as a generated artifact.

It must not be maintained manually as a normal workflow step after creating, rotating, archiving or deleting pages.

Do not create a second sitemap mechanism unless the existing one is explicitly replaced by a confirmed technical decision.

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
3. Use the existing automatic sitemap generation mechanism.
4. The generator scans the current site tree and writes sitemap.xml.
5. Do not hand-edit sitemap.xml except for emergency repair.
```

## Generator requirements

The existing sitemap generator should continue to:

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

## Existing automation note

The sitemap generation mechanism already exists in the live site workflow.

Future chats should first identify and use the existing mechanism rather than proposing to create a new generator or maintain the sitemap by hand.
