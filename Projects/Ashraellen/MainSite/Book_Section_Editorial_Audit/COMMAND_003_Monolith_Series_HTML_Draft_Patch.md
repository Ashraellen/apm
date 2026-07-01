# COMMAND 003 — MONOLITH Series HTML Draft Patch

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: command for HTML draft / patch only

## Mission

Prepare a precise HTML draft / patch plan for expanding the Russian MONOLITH series page, based on the approved editorial direction from `DRAFT_002`.

This command does **not** authorize live-site edits.

Do not update `ru/books/monolith/index.html` directly.
Do not edit any live-site HTML file.
Do not edit `sitemap.xml`.
Do not create SEO scripts.
Do not run metadata repair scripts.
Do not use client-side JavaScript for content, SEO, metadata, or social metadata repair.

The output must be an APM draft that MS can review before any implementation.

## Read first

Read these files in order:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_002_Monolith_Series_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
```

Then read the current live source, but do not modify it:

```text
ru/books/monolith/index.html
```

## Output files

Create the main HTML draft / patch plan here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_003_Monolith_Series_HTML_Draft_Patch.md
```

Create a short report for MS here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_003_Monolith_Series_HTML_Draft_Patch.md
```

## Editorial decision from MS

`DRAFT_002` is accepted as a good basis for the next stage, with these practical decisions:

1. Use the colder MONOLITH-specific voice.
2. Keep the project as an artistic / literary-philosophical research frame, not a grant application.
3. Use the shorter or medium versions where the page may become too heavy.
4. Preserve the existing strongest phrases.
5. Prepare a static HTML draft only, not a live edit.

## Specific content choices for the HTML draft

Use these choices unless there is a strong reason to explain otherwise in the draft notes.

### Hero

Preferred kicker:

```text
Протокол распада социальной материи / БЕТОН — ЖИЖА — ГАЗ
```

Preferred lead:

```text
МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Три тома фиксируют переход социальной материи через три состояния: БЕТОН, ЖИЖА, ГАЗ — от затвердевшей стабильности к вязкой деформации и полной разгерметизации формы.
```

Preserve as main signal:

```text
Система боится не бунта.
Она боится первой трещины.
```

Suggested CTA labels:

```text
Тома трилогии
Карта распада
Что важно не перепутать
```

### What is MONOLITH

Use the full version from `DRAFT_002` if it fits naturally.

The opening sentence must preserve:

```text
Перед вами хроника контролируемого распада: последовательная фиксация фазового перехода социальной материи, запечатлённая в трёх агрегатных состояниях: БЕТОН, ЖИЖА, ГАЗ.
```

### Artistic research frame

Use the main version from `DRAFT_002`, but keep it readable.

Avoid overusing the word `исследование`. The page may use it, but should not sound like an application form.

### Map of collapse

Prepare the HTML draft with the 9-node version if the existing CSS can support it without heavy redesign.

If it becomes visually too heavy, include the 6-node version as an alternative in the notes.

### For whom

Use two concise columns:

```text
Читателям
Издателям / партнёрам / переводчикам
```

Use the shorter partner version from `DRAFT_002` unless the full version is clearly better.

### What not to confuse

Use the full version if possible.

If it becomes too heavy, use the short version and mention in notes that the long version can be kept for later.

### Existing material to preserve

Preserve:

```text
Система боится не бунта.
Она боится первой трещины.
```

Preserve or carefully redistribute:

```text
Перед вами хроника контролируемого распада...
Мы привыкли считать стабильность безопасностью.
Абсолютная стабильность — состояние предельного затвердевания.
Любая живая мысль становится дефектом.
«Исправление» называется милосердием.
«Удаление шума» называется заботой о будущем.
Редактирование реальности становится нормальным механизмом управления человеком.
```

## Technical constraints

1. Do not change live files.
2. Do not edit metadata unless the draft explicitly marks a suggested future metadata improvement.
3. Do not change JSON-LD in this draft unless you separately list it as optional future work.
4. Do not change CSS unless strictly necessary; prefer using existing classes and page structure.
5. Do not create new scripts.
6. Important public content must be static HTML.
7. Existing inline JS links may be noted as a future cleanup, but do not solve that in this command unless only described in the patch plan.
8. Do not touch pages for BETON, SLUDGE, Radiance, Sampo, or the general Books index.

## Required structure of DRAFT_003

The main draft must include:

1. Status and scope.
2. Source files read.
3. Implementation principle.
4. Proposed final page architecture for `ru/books/monolith/index.html`.
5. Exact section-by-section HTML draft or pseudo-diff.
6. Notes on which existing blocks should be replaced, preserved, or moved.
7. Any recommended metadata / JSON-LD changes for a future separate stage, if any.
8. Mobile / readability notes.
9. Explicit list of files not touched.
10. Explicit statement that no live-site edits were made.

## Required structure of MS_REPORT_003

The short report for MS must include:

1. Status.
2. Files created.
3. Summary of proposed HTML changes.
4. Decisions requiring MS review.
5. Risks.
6. Clear next step.
7. Explicit statement that live site was not edited.

## Implementation boundary

This command ends with APM draft files only.

A later explicit command is required before editing:

```text
ru/books/monolith/index.html
```

Do not make that edit during this command.
