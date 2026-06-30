# COMMAND 003B — Formula Staticization Batch B

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation, second Formula staticization batch.

This command continues the approved Formula staticization, but only for the Batch B language set.

## Approved decision

Approved from `REVIEW_003A_Formula_Staticization_Batch_A.md`:

```text
Formula staticization batch B: PL, DE, ES, FR only
```

## Batch B scope

Staticize only these 16 Formula HTML files:

```text
pl/public/posts/formula/index.html
pl/public/posts/formula/lines/index.html
pl/public/posts/formula/lines/line-0001.html
pl/public/posts/formula/lines/line-0002.html

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

No other live HTML files are approved in this command.

## Goal

Convert PL, DE, ES and FR Formula pages into self-contained static HTML pages.

The pages must contain the visible Formula content directly in raw HTML and must not depend on `assets/formula-multilingual.js` for visible content or metadata.

## Repositories

```text
Live site: Ashraellen/ashraellen
Memory:    Ashraellen/apm
```

## Required reading

Before editing anything, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
.github/workflows/sitemap.yml
assets/formula.css
assets/formula-multilingual.js
assets/formulas/pl.json
assets/formulas/de.json
assets/formulas/es.json
assets/formulas/fr.json
scripts/audit-page-metadata.js
scripts/export-page-keyword-workbench.js
scripts/generate-sitemap.js
all 16 Batch B Formula HTML files listed above
```

## Allowed live-site changes

You may edit only the 16 Batch B Formula HTML files listed above.

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Formula_Staticization_Batch_B.md
```

## Forbidden live-site changes

Do not edit:

```text
- RU, EN, PT Formula pages already completed in Batch A
- UK, BE Formula pages reserved for Batch C
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

## Implementation method requirement

Use the successful Batch A pattern.

Proceed in controlled language groups or sequential page updates.

Partial completion by whole language is acceptable if a connector limit is reached.

Partial completion by half-written individual page is not acceptable.

If a failure occurs:

```text
- stop;
- report exactly which files were changed;
- do not proceed to another language;
- do not use emergency repair scripts to clean up.
```

## Content source

Use existing approved current JSON sources:

```text
PL: assets/formulas/pl.json
DE: assets/formulas/de.json
ES: assets/formulas/es.json
FR: assets/formulas/fr.json
```

Use the accepted Batch A page structure as the implementation pattern.

Do not invent new formulas.

Do not literal-translate from Russian if JSON already contains current approved language content.

If a JSON text appears weak or suspicious, use it for this staticization pass and record the quality issue in the report for later editorial improvement.

## Required static page behavior

Each Batch B page must contain:

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
- no loading of formula-multilingual.js.
```

Remove the renderer script from Batch B pages after static body content is present:

```html
<script defer src="...assets/formula-multilingual.js..."></script>
```

Remove empty shell dependency:

```html
<div class="page" id="formulaRoot"></div>
```

## Page mapping

```text
/public/posts/formula/                       -> line 0004, current line: path, action, rhythm
/public/posts/formula/lines/                 -> line 0003, previous line: boundaries, measure, form
/public/posts/formula/lines/line-0002.html   -> line 0002, archived line: word, silence, meaning
/public/posts/formula/lines/line-0001.html   -> line 0001, archived line: thought, attention, body, past
```

## Metadata cleanup required inside Batch B

For these 16 pages only, remove emergency-generated residue such as:

```text
- Page context: ...
- language/path labels used only for dedupe
- doctype, html, function, const, github.io, location.pathname, filter, boolean, window, repo in keywords
```

Use natural page-specific metadata in each language.

Do not use path labels as a substitute for meaning.

Metadata should correspond to:

```text
0004 current: path / action / rhythm
0003 previous: boundaries / measure / form
0002 archived: word / silence / meaning
0001 archived: thought / attention / body / past
```

## JSON-LD requirements

Each Batch B page must have one JSON-LD block.

Verify:

```text
- `url` matches canonical exactly;
- current page breadcrumb URL matches canonical exactly;
- no trailing slash after `.html` URLs;
- `name` corresponds naturally to page title;
- `description` corresponds naturally to meta description;
- `inLanguage` matches html lang.
```

## Validation requirements

After editing, read back all changed files if feasible, or at minimum these representative files plus a full changed-file comparison:

```text
pl/public/posts/formula/index.html
de/public/posts/formula/lines/line-0001.html
es/public/posts/formula/index.html
fr/public/posts/formula/lines/line-0002.html
```

Verify:

```text
- raw HTML contains visible Formula cards;
- there are 15 Formula cards per page;
- `formulaRoot` is absent or not used as empty content shell;
- `formula-multilingual.js` is absent;
- static title/description/keywords/canonical exist;
- keywords do not contain code garbage;
- JSON-LD is page-specific;
- `.html/` breadcrumb URL error is absent;
- no non-Batch-B file was changed.
```

Do not run emergency repair scripts.

If using `[skip ci]` on controlled commits, record that in the report.

## Required output report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003B_Formula_Staticization_Batch_B.md
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
4. Exact list of Batch B pages staticized.
5. Whether PL, DE, ES and FR all completed.
6. Confirmation that no non-Batch-B live file changed.
7. Confirmation that workflows/scripts/sitemap/assets/formula JSON/JS were not changed.
8. Representative before/after notes.
9. Validation performed.
10. Any unresolved language/transcreation quality issues.
11. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION_BATCH_C
REQUEST_MORE_ARCHITECT_REVIEW
```

If Batch B completes cleanly, request approval for Batch C.

If not, request architect review.

## Success condition

This command is complete when:

```text
- all feasible PL, DE, ES and FR Formula pages are self-contained static HTML;
- Batch B pages no longer depend on formula-multilingual.js for visible content or metadata;
- Batch B metadata no longer contains emergency code/path residue;
- no forbidden files were changed;
- REPORT_003B_Formula_Staticization_Batch_B.md exists in the APM workspace.
```
