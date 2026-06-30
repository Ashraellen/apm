# COMMAND 003A — Formula Staticization Batch A

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation, smaller batch retry.

This command continues the approved Formula staticization, but only for a limited language batch.

## Approved decision

Approved from `REVIEW_003_Formula_Staticization.md`:

```text
Formula staticization batch A: RU, EN, PT only
```

## Batch A scope

Staticize only these 12 Formula HTML files:

```text
ru/public/posts/formula/index.html
ru/public/posts/formula/lines/index.html
ru/public/posts/formula/lines/line-0001.html
ru/public/posts/formula/lines/line-0002.html

en/public/posts/formula/index.html
en/public/posts/formula/lines/index.html
en/public/posts/formula/lines/line-0001.html
en/public/posts/formula/lines/line-0002.html

pt/public/posts/formula/index.html
pt/public/posts/formula/lines/index.html
pt/public/posts/formula/lines/line-0001.html
pt/public/posts/formula/lines/line-0002.html
```

No other live HTML files are approved in this command.

## Goal

Convert the RU, EN and PT Formula pages into self-contained static HTML pages.

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
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
.github/workflows/sitemap.yml
assets/formula.css
assets/formula-multilingual.js
assets/formulas/en.json
assets/formulas/pt.json
ru/public/posts/formula/index.html
ru/public/posts/formula/lines/index.html
ru/public/posts/formula/lines/line-0001.html
ru/public/posts/formula/lines/line-0002.html
en/public/posts/formula/index.html
en/public/posts/formula/lines/index.html
en/public/posts/formula/lines/line-0001.html
en/public/posts/formula/lines/line-0002.html
pt/public/posts/formula/index.html
pt/public/posts/formula/lines/index.html
pt/public/posts/formula/lines/line-0001.html
pt/public/posts/formula/lines/line-0002.html
scripts/audit-page-metadata.js
scripts/export-page-keyword-workbench.js
scripts/generate-sitemap.js
```

## Allowed live-site changes

You may edit only the 12 Batch A Formula HTML files listed above.

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003A_Formula_Staticization_Batch_A.md
```

## Forbidden live-site changes

Do not edit:

```text
- PL, DE, ES, FR, UK, BE Formula pages
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

Do not attempt another 36-file bulk replacement.

Use a smaller controlled method, such as:

```text
- update files sequentially;
- or commit one language at a time;
- or commit all 12 only if the tool path is demonstrably safe.
```

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

For RU:

```text
Use the existing RU Formula static pages as the content source.
Clean metadata and structure if needed, but preserve the approved Russian formula texts.
```

For EN:

```text
Use assets/formulas/en.json as the approved current English content source.
```

For PT:

```text
Use assets/formulas/pt.json as the approved current Portuguese content source.
```

Do not invent new formulas.

Do not literal-translate from Russian if the JSON already contains the current approved non-RU language content.

If a JSON text appears weak or suspicious, use it for this staticization pass and record the quality issue in the report for later editorial improvement.

## Required static page behavior

Each Batch A page must contain:

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

Remove the renderer script from Batch A pages after static body content is present:

```html
<script defer src="...assets/formula-multilingual.js..."></script>
```

Remove empty shell dependency:

```html
<div class="page" id="formulaRoot"></div>
```

The page may keep a small base-path script only if needed for compatibility, but final navigation should not depend on empty placeholders.

## Page mapping

```text
/public/posts/formula/                       -> line 0004, current line: path, action, rhythm
/public/posts/formula/lines/                 -> line 0003, previous line: boundaries, measure, form
/public/posts/formula/lines/line-0002.html   -> line 0002, archived line: word, silence, meaning
/public/posts/formula/lines/line-0001.html   -> line 0001, archived line: thought, attention, body, past
```

## Metadata cleanup required inside Batch A

For these 12 pages only, remove emergency-generated residue such as:

```text
- Page context: ...
- PT / posts / formula
- language/path labels used only for dedupe
- doctype, html, function, const, github.io, location.pathname, filter, boolean, window, repo in keywords
```

Use natural page-specific metadata.

Recommended EN metadata:

```text
Line 0004:
Title: Ashraellen — Path, Action, Rhythm
Description: Current Ashraellen formula line on path, action and rhythm: short forms of thought where movement learns its measure.

Line 0003:
Title: Ashraellen — Boundaries, Measure, Form
Description: Ashraellen formula line on boundaries, measure and form: short forms of thought on inner limits, rhythm and self-return.

Line 0002:
Title: Ashraellen — Word, Silence, Meaning
Description: Archived Ashraellen formula line on word, silence and meaning: short forms of thought on language, precision and listening.

Line 0001:
Title: Ashraellen — Thought, Attention, Body, Past
Description: Archived Ashraellen formula line on thought, attention, body and past: short forms of observation on inner movement and memory.
```

Create analogous natural RU and PT metadata.

Do not use path labels as a substitute for meaning.

## JSON-LD requirements

Each Batch A page must have one JSON-LD block.

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

After editing, read back all 12 changed files from the repository or, if tool limits require, at least these representative files plus a full changed-file list:

```text
ru/public/posts/formula/index.html
en/public/posts/formula/index.html
en/public/posts/formula/lines/line-0001.html
pt/public/posts/formula/index.html
pt/public/posts/formula/lines/line-0002.html
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
- no non-Batch-A file was changed.
```

If possible, run or wait for the safe sitemap/report workflow after the commit, but do not run emergency repair scripts.

## Required output report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003A_Formula_Staticization_Batch_A.md
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
4. Exact list of Batch A pages staticized.
5. Whether RU, EN and PT all completed.
6. Confirmation that no non-Batch-A live file changed.
7. Confirmation that workflows/scripts/sitemap/assets/formula JSON/JS were not changed.
8. Representative before/after notes for EN and PT pages.
9. Validation performed.
10. Any unresolved language/transcreation quality issues.
11. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION_BATCH_B
REQUEST_MORE_ARCHITECT_REVIEW
```

If Batch A completes cleanly, request approval for Batch B.

If not, request architect review.

## Success condition

This command is complete when:

```text
- all feasible RU, EN and PT Formula pages are self-contained static HTML;
- Batch A pages no longer depend on formula-multilingual.js for visible content or metadata;
- Batch A metadata no longer contains emergency code/path residue;
- no forbidden files were changed;
- REPORT_003A_Formula_Staticization_Batch_A.md exists in the APM workspace.
```
