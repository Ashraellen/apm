# COMMAND 008 — HTML Implementation

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: limited live-site implementation

## Mission

Implement the approved visible-content expansion for this page only:

```text
ru/books/monolith/beton/index.html
```

This command authorizes editing only that live-site file.

## Read first

Read:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_006_Beton_Individual_Book_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_006_Beton_Individual_Book_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_007_HTML_Draft_Patch.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_007_HTML_Draft_Patch.md
```

Then read the current live file:

```text
ru/books/monolith/beton/index.html
```

## Authorized edit

Only this live-site file may be edited:

```text
ru/books/monolith/beton/index.html
```

## Files and areas not authorized

Do not edit:

```text
sitemap.xml
assets/books.css
ru/books/index.html
ru/books/monolith/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

Do not change:

```text
metadata
JSON-LD
social metadata
shared CSS
scripts
```

Do not create or run scripts.

## Implementation decisions

Apply the approved plan from `DRAFT_007_HTML_Draft_Patch.md` with these MS decisions:

1. Replace the current short lead with the colder lead selected in `DRAFT_007`.
2. Preserve the existing case block, cover, primary signal, protocol line, and verified buttons.
3. Replace the current single long description block with structured sections:
   - `О книге`;
   - `Без спойлеров`;
   - `Художественно-исследовательская рамка`;
   - `Темы / смысловые узлы`;
   - `Для кого эта книга`;
   - `Место в трилогии`;
   - `Где читать / издания`;
   - `Что важно не перепутать`.
4. Use the full `О книге` block from `DRAFT_007`.
5. Use the prose `Без спойлеров` block from `DRAFT_007`.
6. Use the full research-frame block from `DRAFT_007`, if the resulting layout remains readable.
7. Use the 6-node themes block from `DRAFT_007`.
8. Use the full reader block from `DRAFT_007`, unless the final page becomes too dense.
9. Use the shorter trilogy-place block from `DRAFT_007`.
10. Keep the bottom editions block with verified links.
11. Use the compact prose version of the boundaries block, not the card alternative.
12. Preserve the final signal and edition note near the lower part of the page.
13. Add only minimal page-local CSS inside the existing inline style block if needed.
14. Do not edit shared CSS.
15. Do not change metadata, JSON-LD, social metadata, scripts, or sitemap.

## Verification

After editing, verify:

1. Only `ru/books/monolith/beton/index.html` changed in the live-site repository.
2. The page content is static HTML.
3. The cover and verified links remain present.
4. The existing case-file atmosphere remains recognizable.
5. The page has the structured sections listed above.
6. `sitemap.xml` was not edited.
7. `assets/books.css` was not edited.
8. metadata, JSON-LD, social metadata, and scripts were not changed.
9. No new scripts were created or run.

## Required MS report

After implementation, create:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_008_HTML_Implementation.md
```

The report must include:

1. Status.
2. Live-site commit SHA.
3. Exact files edited.
4. Summary of visible-content changes.
5. Confirmation that forbidden files and areas were not edited.
6. Any deviations from `DRAFT_007` and why.
7. Browser / readability notes if checked.
8. Clear next step.

## Boundary

This command authorizes only the one live-site edit named above and the APM report.

A separate command is required before editing any other page or any technical/metadata area.
