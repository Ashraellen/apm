# COMMAND 003C — Formula Staticization Batch C

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation, final Formula staticization batch.

This command approves only UK and BE Formula pages.

## Approved decision

Approved from:

```text
REVIEW_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
```

Approved scope:

```text
Formula staticization Batch C: UK and BE only
```

## Batch C target files

Staticize only these 8 Formula HTML files:

```text
uk/public/posts/formula/index.html
uk/public/posts/formula/lines/index.html
uk/public/posts/formula/lines/line-0001.html
uk/public/posts/formula/lines/line-0002.html

be/public/posts/formula/index.html
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0001.html
be/public/posts/formula/lines/line-0002.html
```

No other live HTML files are approved in this command.

## Goal

Complete Formula staticization by converting UK and BE Formula pages into self-contained static HTML pages.

The pages must contain visible Formula content directly in raw HTML and must not depend on `assets/formula-multilingual.js` for visible content or metadata.

## Required reading

Before editing anything, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Formula_Staticization_Batch_B.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003B_Formula_Staticization_Batch_B.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
assets/formula.css
assets/formula-multilingual.js
assets/formulas/uk.json
assets/formulas/be.json
all 8 Batch C target HTML files listed above
```

## Allowed live-site changes

You may edit only the 8 Batch C Formula HTML files listed above.

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Formula_Staticization_Batch_C.md
```

## Forbidden live-site changes

Do not edit:

```text
- RU, EN, PT pages
- PL, DE, ES, FR pages
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

## Implementation method

Use the accepted Batch A and Batch B pattern.

Proceed sequentially or by language group:

```text
1. UK language group
2. BE language group
```

If any file write fails, stop at that point and report the exact state.

Do not proceed to the next language after a failed file write.

## Content source

Use current approved JSON sources:

```text
UK: assets/formulas/uk.json
BE: assets/formulas/be.json
```

Use the accepted previous batches as structural pattern.

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

For UK and BE Formula pages only, remove emergency-generated residue such as:

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
uk/public/posts/formula/index.html
uk/public/posts/formula/lines/line-0001.html
be/public/posts/formula/index.html
be/public/posts/formula/lines/line-0002.html
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
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003C_Formula_Staticization_Batch_C.md
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
4. Whether UK and BE completed.
5. Confirmation that no forbidden live file changed.
6. Confirmation that workflows/scripts/sitemap/assets/formula JSON/JS were not changed.
7. Validation performed.
8. Any unresolved language/transcreation quality issues.
9. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION_FINAL_REVIEW
REQUEST_MORE_ARCHITECT_REVIEW
```

If UK and BE complete cleanly, request final Formula staticization review.

If not, request architect review.

## Success condition

This command is complete when:

```text
- all feasible UK and BE Formula pages are self-contained static HTML;
- completed pages no longer depend on formula-multilingual.js;
- completed page metadata no longer contains emergency code/path residue;
- no forbidden files were changed;
- REPORT_003C_Formula_Staticization_Batch_C.md exists in APM.
```
