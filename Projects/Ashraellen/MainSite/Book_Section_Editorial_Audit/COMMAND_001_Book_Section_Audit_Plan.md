# COMMAND 001 — Book Section Editorial Audit Plan

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: command for audit and planning only

## Mission

Bring order to the Books section of Ashraellen.com by auditing the series pages and individual book pages, especially the difference between the mature `Radiance / Sampo` frame and the currently thinner `MONOLITH / BETON / SLUDGE` frame.

Do not edit the live site during this command.

The first task is audit, decision, and implementation plan only.

## Source of truth

Read this command file first:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/COMMAND_001_Book_Section_Audit_Plan.md
```

Write the main report here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
```

If additional notes are needed, put them in the same folder and reference them from the report.

## Language

Work in Russian.

If later any public-facing English text is needed, prepare it in English separately and explicitly label it as public-facing draft.

## Mandatory comparison pages

Reference / mature model:

```text
https://www.ashraellen.com/ru/books/radiance/
https://www.ashraellen.com/ru/books/radiance/sampo/
```

Pages to audit and possibly strengthen:

```text
https://www.ashraellen.com/ru/books/monolith/
https://www.ashraellen.com/ru/books/monolith/beton/
https://www.ashraellen.com/ru/books/monolith/sludge/
```

General Books section:

```text
https://www.ashraellen.com/ru/books/
```

Other book pages to inspect after MONOLITH:

```text
https://www.ashraellen.com/ru/books/error-404-god-not-found/
https://www.ashraellen.com/ru/books/seccus/
https://www.ashraellen.com/ru/books/you-are-already-online/
https://www.ashraellen.com/ru/books/the-book-of-whinesis/
```

## Background

`Radiance` and `Sampo` already have a mature expanded frame:

- literary-philosophical / artistic research framing;
- method explanation;
- meaning-node map;
- sections for readers and partners;
- clear boundary markers explaining what the project is not.

`MONOLITH`, `BETON`, and `SLUDGE` are strong as book / genre pages but weaker as research-oriented pages.

The question is not whether to make them longer for the sake of length. The question is whether to strengthen them so they match the current professional standard of the site while preserving their atmosphere.

## First-stage tasks

1. Compare the page architecture of `Radiance / Sampo` with `MONOLITH / BETON / SLUDGE`.
2. Identify which blocks should become part of the standard Ashraellen book-page model:
   - About the book / cycle;
   - artistic research frame;
   - method or reading key;
   - without spoilers;
   - map of themes / meaning nodes;
   - for readers;
   - for publishers / partners;
   - what this project is not.
3. Decide which pages should definitely be changed and which can remain mostly unchanged.
4. Propose a new standard for Ashraellen book and book-series pages.
5. Propose an implementation order.
6. Mark risks and constraints.

## Required report structure

Create the report at:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
```

The report must include:

1. Executive summary.
2. Current state of the Books section.
3. Comparison: `Radiance / Sampo` vs `MONOLITH / BETON / SLUDGE`.
4. Decision: whether the MONOLITH pages should be strengthened.
5. Proposed standard for book-series pages.
6. Proposed standard for individual book pages.
7. Page-by-page recommendations.
8. Implementation order.
9. Risks and safeguards.
10. Explicit list of files that would be edited in a later implementation phase.
11. Explicit statement that no live-site edits were made during this audit command.

## Important constraints

Do not edit the live site during this command.

Do not manually edit `sitemap.xml`.

Do not create a second sitemap generator.

Do not use client-side JavaScript for content, SEO, metadata, or social metadata repair.

Do not run broad metadata repair scripts.

Do not mix Public Posts / Formula with Public Thoughts.

Do not change APM canon files outside this command unless explicitly requested.

Do not turn book pages into grant applications, lectures, spiritual teachings, therapy pages, or institutional self-promotion.

Preserve the literary atmosphere of each book and cycle.

## Transcreation rule

If later implementation expands to other languages, use the existing site-wide transcreation rule:

- public multilingual content is transcreated by default;
- literal translation is reserved only for paths, code, canonical labels, legal/admin text, schema identifiers, and fixed seal text.

## Implementation boundary

This command ends with a written report and plan only.

A separate command or explicit user approval is required before changing any live-site HTML files.
