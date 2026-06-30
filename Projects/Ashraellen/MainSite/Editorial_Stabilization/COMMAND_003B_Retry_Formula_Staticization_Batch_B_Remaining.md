# COMMAND 003B Retry — Formula Staticization Batch B Remaining

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation retry.

This command continues Batch B only for the remaining files.

## Approved decision

Approved from:

```text
REVIEW_003B_Formula_Staticization_Batch_B.md
```

## Current known state

Already completed in Batch B:

```text
pl/public/posts/formula/index.html
pl/public/posts/formula/lines/index.html
pl/public/posts/formula/lines/line-0002.html
```

Still remaining:

```text
pl/public/posts/formula/lines/line-0001.html

de/public/posts/formula/index.html
de/public/posts/formula/lines/index.html
de/public/posts/formula/lines/line-0001.html
de/public/posts/formula/lines/line-0002.html

es/public/posts/formula/index.html
es/public/posts/formula/lines/index.html
es/public/posts/formula/lines/line-0001.html
es/public/posts/formula/lines/line-0002.html

fr/public/posts/formula/index.html
fr/public/posts/formula/lines/index.html
fr/public/posts/formula/lines/line-0001.html
fr/public/posts/formula/lines/line-0002.html
```

## Goal

Complete staticization for the remaining Batch B Formula pages.

Each completed page must contain visible Formula content directly in raw HTML and must not depend on `assets/formula-multilingual.js` for visible content or metadata.

## Required reading

Before editing anything, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_003B_Formula_Staticization_Batch_B.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Formula_Staticization_Batch_B.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003B_Formula_Staticization_Batch_B.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md

Ashraellen/ashraellen:
assets/formula.css
assets/formula-multilingual.js
assets/formulas/pl.json
assets/formulas/de.json
assets/formulas/es.json
assets/formulas/fr.json
all remaining target HTML files listed below
```

## Allowed live-site changes

You may edit only these 13 remaining Batch B Formula HTML files:

```text
pl/public/posts/formula/lines/line-0001.html

de/public/posts/formula/index.html
de/public/posts/formula/lines/index.html
de/public/posts/formula/lines/line-0001.html
de/public/posts/formula/lines/line-0002.html

es/public/posts/formula/index.html
es/public/posts/formula/lines/index.html
es/public/posts/formula/lines/line-0001.html
es/public/posts/formula/lines/line-0002.html

fr/public/posts/formula/index.html
fr/public/posts/formula/lines/index.html
fr/public/posts/formula/lines/line-0001.html
fr/public/posts/formula/lines/line-0002.html
```

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
```

## Retry order

Proceed in this order:

```text
1. pl/public/posts/formula/lines/line-0001.html
2. DE language group
3. ES language group
4. FR language group
```

If the PL retry fails, stop and report.

If PL succeeds but a later language fails, stop at that language boundary and report.

Do not proceed after a failed file write.

## Forbidden live-site changes

Do not edit:

```text
- RU, EN, PT pages
- already completed PL pages unless absolutely necessary and explicitly reported
- UK, BE pages
- sitemap.xml manually
- .github/workflows/*.yml
- scripts/*.js
- scripts/*.py
- assets/formula.css
- assets/formula-multilingual.js
- assets/formulas/*.json
- Public Thoughts pages
- legacy thought URLs
- non-Formula pages
- robots.txt
- README.md
- reports/apm/* inside live repo
```

Do not delete any file.

Do not run or trigger the emergency metadata repair workflow.

Do not use broad automatic repair scripts.

## Content source

Use current approved JSON sources:

```text
PL: assets/formulas/pl.json
DE: assets/formulas/de.json
ES: assets/formulas/es.json
FR: assets/formulas/fr.json
```

Use the accepted Batch A and completed PL pages as structural pattern.

Do not invent new formulas.

If a source text seems weak, use it for this staticization pass and record it as later editorial-review material.

## Required static page behavior

Each completed page must contain:

```text
- static visible body content inside HTML;
- H1;
- lead/intro text;
- line title/theme;
- 15 visible Formula cards;
- navigation links without final href="#" placeholders;
- seal block preserving fixed label `— mark of presence`;
- static <title>;
- static <meta name="description">;
- static <meta name="keywords"> without code garbage;
- static canonical;
- one static JSON-LD block with page-specific name/description/url/inLanguage/breadcrumb;
- static OG title/description;
- static Twitter title/description;
- stylesheet link to assets/formula.css;
- no loading of formula-multilingual.js;
- no empty formulaRoot shell.
```

## Metadata cleanup required

For completed pages only, remove emergency-generated residue such as:

```text
- Page context: ...
- language/path labels used only for dedupe
- doctype, html, function, const, github.io, location.pathname, filter, boolean, window, repo in keywords
```

Use natural page-specific metadata in each language.

## Validation requirements

After editing, read back representative files and compare changed files.

Minimum representative read-back:

```text
pl/public/posts/formula/lines/line-0001.html
de/public/posts/formula/index.html
es/public/posts/formula/index.html
fr/public/posts/formula/lines/line-0002.html
```

Verify:

```text
- raw HTML contains visible Formula cards;
- there are 15 Formula cards per completed page;
- formulaRoot is absent or not used as empty content shell;
- formula-multilingual.js is absent;
- static title/description/keywords/canonical exist;
- keywords do not contain code garbage;
- JSON-LD is page-specific;
- `.html/` breadcrumb URL error is absent;
- no non-approved file was changed.
```

Do not run emergency repair scripts.

## Required output report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
```

Use:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Report must include:

```text
1. Files read.
2. Files changed.
3. Commit hashes.
4. Whether PL line-0001 succeeded.
5. Whether DE, ES and FR all completed.
6. Confirmation that no forbidden live file changed.
7. Confirmation that workflows/scripts/sitemap/assets/formula JSON/JS were not changed.
8. Validation performed.
9. Any unresolved language/transcreation quality issues.
10. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION_BATCH_C
REQUEST_MORE_ARCHITECT_REVIEW
```

If all remaining Batch B files complete cleanly, request approval for Batch C.

If not, request architect review.

## Success condition

This command is complete when:

```text
- all feasible remaining Batch B Formula pages are self-contained static HTML;
- completed pages no longer depend on formula-multilingual.js;
- completed page metadata no longer contains emergency code/path residue;
- no forbidden files were changed;
- REPORT_003B_Retry_Formula_Staticization_Batch_B_Remaining.md exists in APM.
```
