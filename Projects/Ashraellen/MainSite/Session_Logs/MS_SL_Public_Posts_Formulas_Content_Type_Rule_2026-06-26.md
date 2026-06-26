# Session Log — Public Posts / Formula content type rule

Date: 2026-06-26
Project: Ashraellen MainSite / Public / Posts / Formula

## Purpose

Record the finalization of the Formula post type rule after the working mechanism was implemented and tested.

## Context

The Formula section was first built as a Russian page structure, then rotated through visible line states for demonstration:

```text
/ru/public/posts/formula/
→ current active line

/ru/public/posts/formula/lines/
→ previous line

/ru/public/posts/formula/lines/line-0002.html
→ older archive

/ru/public/posts/formula/lines/line-0001.html
→ oldest archive in the current set
```

The current example chain is:

```text
0004 current
→ 0003 previous
→ 0002 archive
→ 0001 archive
```

## Confirmed content-type decisions

- Formula posts are independent from Public Thoughts / Опорные мысли.
- Formulas must not echo, summarize or shorten Public Thoughts.
- Individual formulas are not numbered.
- Only formula lines are numbered conceptually and archivally.
- Previous/archive line pages should use theme-based headings, not repeated ordinal labels.
- Formula localization is transcreation, not literal translation.
- A formula should preserve the same inner strike, rhythm and silence after the line in each language.

## Technical implementation state

The multilingual Formula section now uses:

```text
assets/formula.css
assets/formula-multilingual.js
assets/formulas/<lang>.json
```

Implemented language data files:

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

Russian currently has its own static implementation and may later be moved into the same data model if useful.

## APM updates

Updated:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
```

Commit:

```text
3040f054ddccd677d89e4f65afe53f8f73f66f98
```

Updated:

```text
Projects/Ashraellen/MainSite/INDEX.md
```

Commit:

```text
235b52c2bb8d8325644261aad82de8d8a0e327e4
```

## Future work

When adding a new formula line:

```text
1. Prepare the line content first.
2. Transcreate the line across languages.
3. Rotate /formula/ → /lines/ → line-000N.html.
4. Update assets/formulas/<lang>.json.
5. Touch assets/formula-multilingual.js only if the mechanism changes.
6. Do not update Public Thoughts documentation unless Public Thoughts are actually affected.
```
