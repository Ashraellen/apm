# COMMAND 004 — MONOLITH Series HTML Implementation

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: command for limited live-site HTML implementation

## Mission

Implement the approved editorial expansion of the Russian MONOLITH series page.

This command **does authorize one limited live-site edit**:

```text
ru/books/monolith/index.html
```

No other live-site files are authorized for editing.

## Read first

Read these APM files in order:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_002_Monolith_Series_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_003_Monolith_Series_HTML_Draft_Patch.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_003_Monolith_Series_HTML_Draft_Patch.md
```

Then read the current live file:

```text
ru/books/monolith/index.html
```

## Authorized file to edit

Only this file may be edited:

```text
ru/books/monolith/index.html
```

## Files that must not be edited

Do not edit:

```text
sitemap.xml
assets/books.css
ru/books/index.html
ru/books/monolith/beton/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

Do not edit any other file unless the user gives a separate explicit command.

## MS decisions for implementation

Apply the following decisions exactly.

### 1. Block `Что такое МОНОЛИТ`

Use the **medium version**, not the full version.

The page should be stronger and clearer, but not overloaded.

Preserve the opening sentence:

```text
Перед вами хроника контролируемого распада: последовательная фиксация фазового перехода социальной материи, запечатлённая в трёх агрегатных состояниях: БЕТОН, ЖИЖА, ГАЗ.
```

### 2. `Карта распада`

Use the **expanded 3×3 model**.

Do not use a flat 9-node map.
Do not use a poor 3-card map without inner structure.

The structure must be:

```text
БЕТОН — затвердевшая стабильность
- стабильность как тюрьма;
- память как опасность;
- первая трещина.

ЖИЖА — вязкая деформация
- усталость сопротивления;
- растворение границ;
- соучастие как привычка.

ГАЗ — разгерметизация формы
- контроль становится воздухом;
- смысл выходит из контейнеров;
- прежняя система теряет стену, но не исчезает.
```

Each of the three cards may have one short explanatory line before the three inner signs, if it improves readability.

### 3. `Что важно не перепутать`

Use the **full version**, but keep it visually compact.

The block must clearly state that MONOLITH is:

- not a prediction of the future;
- not a manual for rebellion;
- not a political pamphlet;
- not decorative cyberpunk about gadgets;
- not a technological fantasy;
- an artistic study of how system logic enters memory, language, body, habit, fear, and normality.

### 4. Final phrase

Do not duplicate the signal:

```text
Система боится не бунта.
Она боится первой трещины.
```

If this phrase is moved into the hero, replace the final phrase block with:

```text
Распад начинается не тогда, когда рушится стена.
Он начинается, когда человек впервые слышит внутри неё гул.
```

### 5. Static links

Replace `href="#"` for `БЕТОН` and `ЖИЖА` buttons with static links:

```text
/ru/books/monolith/beton/
/ru/books/monolith/sludge/
```

Do not create a link for `ГАЗ` unless a real page exists.

### 6. Metadata / JSON-LD

Do not change metadata.
Do not change JSON-LD.
Do not change social metadata.

This command is about visible page content and minimal page-local styling only.

## Page content direction

The expanded page must present MONOLITH as:

```text
литературно-философская антиутопическая трилогия
и художественное исследование контроля, памяти, социальной материи,
редактирования реальности и распада систем.
```

But do not make the page sound like a grant application.

Do not use dry institutional language.

Do not turn the page into a lecture, manifesto, therapy page, spiritual teaching, political pamphlet, or academic abstract.

Preserve the MONOLITH temperature:

```text
холод, протокол, контроль, стена, трещина, распад, разгерметизация.
```

## Implementation instructions

1. Start from the current `ru/books/monolith/index.html`.
2. Apply the section architecture from `DRAFT_003`, adjusted by MS decisions above.
3. Keep the current background, cover/card imagery, page atmosphere, and MONOLITH voice.
4. Use static HTML for all important public content.
5. Add only minimal page-local CSS inside the existing inline `<style>` block if necessary.
6. Do not modify shared CSS in `assets/books.css`.
7. Do not introduce new scripts.
8. Do not use client-side JavaScript for content, SEO, metadata, social metadata, or link repair.
9. Keep the page mobile-readable.
10. Preserve the seal behavior and existing structural conventions unless a change is strictly necessary for the visible content.

## Required implementation report

After implementation, create a short MS report here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_004_Monolith_Series_HTML_Implementation.md
```

The report must include:

1. Status.
2. Commit SHA of the live-site edit.
3. Exact files edited.
4. Summary of changes made.
5. Confirmation that prohibited files were not edited.
6. Notes on any deviations from `DRAFT_003` and why.
7. Any follow-up recommendations.

## Post-implementation verification

After editing `ru/books/monolith/index.html`, verify and report:

- the file still contains valid static visible content;
- `sitemap.xml` was not edited;
- `assets/books.css` was not edited;
- metadata / JSON-LD were not edited;
- no new SEO scripts were created;
- no client-side JS was added for content / SEO / metadata / social metadata;
- only the authorized page was changed.

## Implementation boundary

This command authorizes only:

```text
ru/books/monolith/index.html
```

and the APM report:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_004_Monolith_Series_HTML_Implementation.md
```

A separate command is required before editing:

```text
ru/books/monolith/beton/index.html
ru/books/monolith/sludge/index.html
ru/books/index.html
```

or any other live-site file.
