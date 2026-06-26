# Public Posts — Formulas content type rule

Date: 2026-06-26
Project: Ashraellen MainSite / Public / Posts / Formula
Status: active content-type rule

## 1. Scope

This rule governs the `Formula` post type under Public Posts:

```text
/[lang]/public/posts/formula/
/[lang]/public/posts/formula/lines/
/[lang]/public/posts/formula/lines/line-000N.html
assets/formula.css
assets/formula-multilingual.js
assets/formulas/<lang>.json
```

This rule does not govern Public Thoughts / Опорные мысли.

All language work for this content type is also governed by the site-wide transcreation rule:

```text
Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
```

## 2. Core distinction

Formulas are their own public format.

They must not be treated as:

```text
- Public Thoughts excerpts
- shortened support thoughts
- summaries of Public Thoughts
- echoes of the current Public Thoughts arc
- replacements for Public Thoughts
```

Formulas may belong to the same Ashraellen field, but they are a separate content type.

## 3. Content principle

A formula is a short, self-contained line of thought.

It should work as:

```text
one thought
one inner movement
one precise strike
```

Formula cards should remain concise, clean and direct.

A formula should not become:

```text
- a miniature essay
- a motivational quote
- a doctrine statement
- an explanation
- a comment on another page
```

## 4. Numbering rule

Individual formulas are not numbered.

Only formula lines are numbered conceptually and archivally:

```text
line-0001.html
line-0002.html
line-0003.html
...
```

Inside a line, formulas appear as unnumbered cards.

## 5. Rotation model

The formula section uses a layered rotation model.

Current state after the first implemented rotation set:

```text
/[lang]/public/posts/formula/
→ current active line

/[lang]/public/posts/formula/lines/
→ previous line

/[lang]/public/posts/formula/lines/line-0002.html
→ older archived line

/[lang]/public/posts/formula/lines/line-0001.html
→ oldest archived line in the current set
```

Example current chain:

```text
0004 current
→ 0003 previous
→ 0002 archive
→ 0001 archive
```

When a new line appears:

```text
1. Move the current /formula/ line into /formula/lines/.
2. Preserve the previous /formula/lines/ line as the next numbered archive file.
3. Keep older numbered archive files intact.
4. Put the new active line into /formula/.
```

## 6. Navigation model

The active line page uses:

```text
Следующая линия →
```

to move from the newest active line toward the previous line.

Previous and archived line pages may use:

```text
Актуальная линия
← Предыдущая линия
Следующая линия →
```

Navigation is chronological by line layers, not by individual formula cards.

## 7. Heading model

Avoid repeating the same line label several times on a page.

Preferred visible structure for previous/archive line pages:

```text
H1:
<theme of the line>

Lead:
<ordinal status of the line>

Inner block heading:
Formulas of the line / Формулы линии / localized equivalent
```

Example:

```text
H1: Мысль, внимание, тело, прошлое
Lead: Первая архивная линия формул.
Block: Формулы линии
```

The active page may keep:

```text
H1: Формулы
Lead: Лаконичные формулировки...
Block: <theme of the active line>
```

## 8. Implementation model

The current multilingual Formula implementation uses lightweight language page shells plus a shared renderer:

```text
assets/formula-multilingual.js
assets/formulas/<lang>.json
```

This exists because the language pages were first created technically, and the transcreation step was added afterward.

Therefore this model is accepted as the current working implementation, but it must not be treated as the preferred model for future content creation.

For future Formula lines, the preferred workflow is:

```text
1. Prepare the source line.
2. Approve the line's meaning, rhythm and set of formulas.
3. Transcreate the line into all target languages before publication.
4. Publish self-contained language pages with the transcreated text already present in HTML, unless there is a concrete technical reason to keep a shared renderer/data model.
```

The current page shells exist at:

```text
/[lang]/public/posts/formula/index.html
/[lang]/public/posts/formula/lines/index.html
/[lang]/public/posts/formula/lines/line-0001.html
/[lang]/public/posts/formula/lines/line-0002.html
```

The current data files are:

```text
assets/formulas/en.json
assets/formulas/pl.json
assets/formulas/de.json
assets/formulas/es.json
assets/formulas/fr.json
assets/formulas/pt.json
assets/formulas/uk.json
assets/formulas/be.json
```

Russian currently has its own static implementation.

## 9. Transcreation rule

Formula localization follows the site-wide transcreation rule:

```text
Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
```

Formula language work must be transcreation, not literal translation.

Goal:

```text
same inner strike
same rhythmical force
same silence after the line
natural language-specific expression
```

Do not force Russian syntax into other languages.

Each language should sound as if the formula was originally written in that language.

## 10. Language coverage

Current implemented languages for the formula section:

```text
RU
EN
PL
DE
ES
FR
PT
UK
BE
```

The current shared renderer supports the multilingual pages through each page's `<html lang="...">` value.

## 11. Source rule

New formula lines may come from:

```text
- Telegram material
- newly written formulas
- author-approved adaptations
- distilled ideas from Ashraellen work, if they do not duplicate Public Thoughts
```

Do not automatically derive formulas from the current Public Thoughts arc.

Before publishing a new formula line, check that it does not duplicate Public Thoughts by:

```text
- exact final line
- central image
- rhetorical turn
- same wording shortened
- same theme presented as a card instead of a support thought
```

## 12. Practical line size

The current working size is 15 formulas per line.

This may remain the default unless there is a concrete reason to change it.

## 13. Files to update when a new line is created

When adding a new current line, check these files:

```text
/[lang]/public/posts/formula/index.html
/[lang]/public/posts/formula/lines/index.html
/[lang]/public/posts/formula/lines/line-000N.html
assets/formulas/<lang>.json, only while the current shared data implementation remains in use
assets/formula-multilingual.js, only if the mechanism changes
assets/formula.css, only if visual style changes
```

Preferred future publication is self-contained language HTML with the transcreated text already present.

Update the APM memory if the mechanism, file layout, or line logic changes.

Do not update Public Thoughts documentation unless the change also affects Public Thoughts, which should be rare.
