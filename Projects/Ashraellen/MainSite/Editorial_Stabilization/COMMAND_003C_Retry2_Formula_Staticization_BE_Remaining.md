# COMMAND 003C Retry 2 — Formula Staticization BE Remaining

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation retry.

This command is only for the three remaining BE Formula pages.

## Approved decision

Approved from:

```text
REVIEW_003C_Retry_Formula_Staticization_BE_Remaining.md
```

## Remaining target files

Edit only these files:

```text
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0002.html
be/public/posts/formula/lines/line-0001.html
```

## Known current state

These files are still runtime-rendered Formula pages and still load:

```text
assets/formula-multilingual.js
```

## Goal

Convert the three remaining BE pages into self-contained static HTML pages.

They must contain visible Formula content directly in raw HTML and must not depend on `formula-multilingual.js` or `formulaRoot`.

## Required reading

Read before editing:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Formula_Staticization_Batch_C.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003C_Formula_Staticization_Batch_C.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Retry_Formula_Staticization_BE_Remaining.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003C_Retry_Formula_Staticization_BE_Remaining.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md

Ashraellen/ashraellen:
assets/formulas/be.json
be/public/posts/formula/index.html
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0002.html
be/public/posts/formula/lines/line-0001.html
```

## Allowed live-site changes

Only the three remaining BE HTML files listed above.

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Retry2_Formula_Staticization_BE_Remaining.md
```

## Forbidden changes

Do not edit:

```text
- be/public/posts/formula/index.html
- UK pages
- RU/EN/PT pages
- PL/DE/ES/FR pages
- workflows
- scripts
- sitemap.xml
- assets/formula.css
- assets/formula-multilingual.js
- assets/formulas/*.json
- Public Thoughts
- legacy URLs
- non-Formula pages
```

Do not run emergency repair scripts or emergency workflow.

## Retry strategy

Use a safer payload strategy than the previous retry.

Recommended:

```text
- Keep title, description, keywords, headings and navigation in normal Belarusian text where safe.
- For formula-card body text, use HTML numeric entity escaping if needed.
- Keep tags and structural labels readable.
- Keep the file compact if that reduces connector risk.
```

HTML entity escaping is acceptable for this transfer pass if browser-rendered visible text preserves the approved BE source.

Do not invent new formulas.

Use:

```text
assets/formulas/be.json
```

as the content source.

## Required page behavior

Each completed page must have:

```text
- visible Formula cards in raw HTML;
- 15 formula cards;
- static title/description/keywords/canonical;
- one page-specific JSON-LD block;
- OG and Twitter title/description;
- link to /assets/formula.css;
- seal label `— mark of presence`;
- no formula-multilingual.js;
- no formulaRoot empty shell;
- no code-garbage keywords.
```

## Retry order

Proceed in this order:

```text
1. be/public/posts/formula/lines/index.html
2. be/public/posts/formula/lines/line-0002.html
3. be/public/posts/formula/lines/line-0001.html
```

If a write is blocked, stop immediately and report.

## Validation

After each successful file update, read it back.

Verify:

```text
- formula cards are present;
- formula-multilingual.js is absent;
- formulaRoot is absent;
- metadata is static;
- no forbidden files changed.
```

Compare from current live head before this retry to final head and report changed files.

## Required report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Retry2_Formula_Staticization_BE_Remaining.md
```

Report must include:

```text
1. Files read.
2. Files changed.
3. Commit hashes.
4. Whether all three BE pages completed.
5. If blocked, exact file where it stopped.
6. Validation performed.
7. Confirmation that no forbidden files changed.
8. Decision request.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION_FINAL_REVIEW
REQUEST_MORE_ARCHITECT_REVIEW
```
