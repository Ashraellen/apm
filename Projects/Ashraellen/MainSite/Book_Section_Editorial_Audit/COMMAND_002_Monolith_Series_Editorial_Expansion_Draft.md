# COMMAND 002 — MONOLITH Series Editorial Expansion Draft

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: command for editorial draft only

## Mission

Prepare an editorial expansion draft for the Russian MONOLITH series page.

This command is a draft-writing task only.

Do not edit the live site.
Do not edit any HTML files.
Do not edit `sitemap.xml`.
Do not create SEO scripts.
Do not use client-side JavaScript for content, SEO, metadata, or social metadata repair.

## Source files and previous report

Read the previous audit report first:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
```

Then read the current live page source:

```text
ru/books/monolith/index.html
```

Use the following reference pages only as architectural models, not as style to copy:

```text
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

## Output files

Create the main editorial draft here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_002_Monolith_Series_Editorial_Expansion.md
```

Create a short handoff report for MS here:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
```

The MS report must be short and practical. It should tell MS what was done, where the draft is saved, what decisions were made, and what should be reviewed next.

## Language

Work in Russian.

Use English only for fixed terms that are already part of the site vocabulary, such as:

```text
MONOLITH
BETON
SLUDGE
artistic research through fiction
```

## Core editorial position

Do not make MONOLITH sound like a grant application.

Do not use a dry institutional tone.

Do not turn the page into a lecture, manifesto, spiritual teaching, therapy page, political pamphlet, or academic abstract.

The public framing should show MONOLITH as:

```text
литературно-философская антиутопическая трилогия
и художественное исследование контроля, памяти,
социальной материи, редактирования реальности
и распада систем.
```

The page must keep the temperature of MONOLITH:

```text
холод, протокол, распад, контроль, сжатие, стена, трещина, разгерметизация.
```

The research framing must begin from the artistic image, not from institutional language.

## Required draft blocks

Prepare public-facing draft text for the following blocks for:

```text
ru/books/monolith/index.html
```

### 1. Hero / entry into the cycle

Provide:

- optional updated kicker;
- optional updated lead;
- one strong short formula of the series;
- suggested CTA labels if needed.

Keep the series identity:

```text
БЕТОН / ЖИЖА / ГАЗ
```

### 2. Что такое МОНОЛИТ

Prepare 3–5 paragraphs.

This block should explain the series as a literary-philosophical anti-dystopian trilogy, not merely as genre fiction.

It should preserve the current idea of three aggregate states of social matter.

### 3. Художественно-исследовательская рамка

Prepare 3–5 paragraphs.

Explain what the trilogy investigates through fiction:

- control;
- memory;
- social matter;
- editing of reality;
- system pressure;
- social training;
- collapse of form;
- the transition from solid to viscous to unsealed.

Do not write this as a grant text.

### 4. Карта распада / карта смысловых узлов

Prepare 6–9 short nodes.

Each node must have:

```text
Title — short explanation.
```

Mandatory nodes to consider:

- БЕТОН;
- ЖИЖА;
- ГАЗ;
- память;
- шум;
- стабильность;
- контроль;
- трещина;
- разгерметизация.

Do not force all nodes if the list becomes too heavy. Choose the strongest 6–9.

### 5. Для кого этот проект

Prepare two sub-blocks:

```text
Читателям
Издателям / партнёрам / переводчикам
```

Keep this concise.

The partner-facing part must be professional but not grant-like.

### 6. Что важно не перепутать

Prepare 4–6 short statements.

Required boundaries:

- MONOLITH is not a prediction of the future;
- not a manual for rebellion;
- not a political pamphlet;
- not decorative cyberpunk about gadgets;
- not a technological fantasy;
- it is an artistic study of how system logic enters memory, language, body, habit, fear, and normality.

### 7. Existing material to preserve

Identify the existing phrases / blocks from `ru/books/monolith/index.html` that should be preserved.

Especially check:

```text
Перед вами хроника контролируемого распада...
Система боится не бунта. Она боится первой трещины.
```

## Required structure of the main draft

The draft file must include:

1. Short editorial note.
2. Proposed page architecture.
3. Draft block: Hero / entry.
4. Draft block: What is MONOLITH.
5. Draft block: Artistic research frame.
6. Draft block: Map of collapse / meaning nodes.
7. Draft block: For whom.
8. Draft block: What not to confuse.
9. Existing text to preserve.
10. Implementation notes for a later HTML phase.
11. Explicit statement that no live-site edits were made.

## Required structure of the MS report

Create:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
```

It must include:

1. Status.
2. Files created.
3. Summary of editorial decisions.
4. Key risks.
5. What MS should review next.
6. Explicit statement that live site was not edited.

## Important safeguards

- Preserve the MONOLITH voice.
- Do not soften MONOLITH into the tone of Radiance.
- Use Radiance / Sampo only as architectural standards.
- Do not copy their mythopoetic temperature.
- Do not add warmth where the page should feel like concrete, protocol, pressure, and fracture.
- Do not overuse the words `research`, `framework`, `partners`, `cultural collaboration` in public-facing text.
- Do not write public text in the language of the audit report.
- Do not touch other book pages during this command.

## Implementation boundary

This command ends with two APM files only:

```text
DRAFT_002_Monolith_Series_Editorial_Expansion.md
MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
```

A separate explicit command is required before editing:

```text
ru/books/monolith/index.html
```

or any other live-site file.
