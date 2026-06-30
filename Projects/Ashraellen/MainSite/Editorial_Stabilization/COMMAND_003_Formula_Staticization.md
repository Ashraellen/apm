# COMMAND 003 — Formula Staticization

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation.

This command approves only Formula page staticization.

Do not perform general metadata quality rewriting outside Formula pages.

Do not implement legacy canonical/noindex policy.

Do not edit workflows or metadata repair scripts in this command.

## Approved decision

Approved from `REVIEW_002_Workflow_Split.md`:

```text
REQUEST_APPROVAL_FORMULA_STATICIZATION
```

Not approved for implementation in this command:

```text
- general metadata quality pass outside Formula pages
- legacy URL canonical/noindex policy
- emergency repair script hardening
- deletion or decommissioning of Formula JSON/JS source files
```

## Goal

Convert the current Formula pages from JS/JSON-rendered shells into self-contained static HTML pages.

The final Formula pages must contain the public visible Formula content directly in HTML and must not depend on `assets/formula-multilingual.js` for the main page meaning.

## Repositories

```text
Live site: Ashraellen/ashraellen
Memory:    Ashraellen/apm
```

## Required reading

Before editing anything, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_001_Editorial_Stabilization_Plan.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_002_Workflow_Split.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_002_Workflow_Split.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/INDEX.md
Projects/Ashraellen/Website_Static_Metadata_Repair_2026-06-30.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
.github/workflows/sitemap.yml
assets/formula.css
assets/formula-multilingual.js
assets/formulas/en.json
assets/formulas/pl.json
assets/formulas/de.json
assets/formulas/es.json
assets/formulas/fr.json
assets/formulas/pt.json
assets/formulas/uk.json
assets/formulas/be.json
scripts/audit-page-metadata.js
scripts/export-page-keyword-workbench.js
scripts/generate-sitemap.js
```

Also read the current Formula HTML files listed below before editing them.

## Allowed live-site changes

You may edit only these 36 HTML files:

```text
ru/public/posts/formula/index.html
ru/public/posts/formula/lines/index.html
ru/public/posts/formula/lines/line-0001.html
ru/public/posts/formula/lines/line-0002.html

en/public/posts/formula/index.html
en/public/posts/formula/lines/index.html
en/public/posts/formula/lines/line-0001.html
en/public/posts/formula/lines/line-0002.html

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

pt/public/posts/formula/index.html
pt/public/posts/formula/lines/index.html
pt/public/posts/formula/lines/line-0001.html
pt/public/posts/formula/lines/line-0002.html

uk/public/posts/formula/index.html
uk/public/posts/formula/lines/index.html
uk/public/posts/formula/lines/line-0001.html
uk/public/posts/formula/lines/line-0002.html

be/public/posts/formula/index.html
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0001.html
be/public/posts/formula/lines/line-0002.html
```

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003_Formula_Staticization.md
```

## Forbidden live-site changes

Do not edit:

```text
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

Do not use broad automatic repair scripts for this task.

## Content source and transcreation rule

The Formula pages must follow the site-wide transcreation rule.

Use the current Formula content as the approved source material:

```text
- RU static pages for Russian visible structure and current content
- assets/formulas/*.json for existing non-RU language content
```

Do not create literal machine translations.

If an existing non-RU JSON line appears weak, mechanical, untranslated, missing, or suspicious, do not invent a replacement silently. Record it in the report as a quality issue and use the best available current approved text for this pass.

This command is primarily staticization, not a full literary retranscreation pass.

## Required static page behavior

Each of the 36 Formula HTML files must become a self-contained static HTML page containing:

```text
- static visible body content inside HTML;
- language-specific header/navigation labels;
- H1;
- lead/intro text;
- formula line title/theme;
- all 15 Formula cards for that page line;
- previous/next/archive navigation as appropriate;
- seal block preserving the fixed label `— mark of presence`;
- static <title>;
- static <meta name="description">;
- static <meta name="keywords"> without code garbage;
- static canonical link;
- static JSON-LD with page-specific name, description, url, breadcrumb and inLanguage;
- static OG title/description;
- static Twitter title/description;
- existing stylesheet link to assets/formula.css;
- no dependency on formula-multilingual.js for main visible content or metadata.
```

Remove this Formula renderer script from the 36 Formula pages after the static body is present:

```html
<script defer src="...assets/formula-multilingual.js..."></script>
```

Keep the small base-path script only if it is still needed for GitHub Pages path compatibility or navigation. Prefer static absolute URLs where practical and safe.

## Page mapping

Current Formula line mapping:

```text
/public/posts/formula/                       -> line 0004, current line: path, action, rhythm
/public/posts/formula/lines/                 -> line 0003, previous line: boundaries, measure, form
/public/posts/formula/lines/line-0002.html   -> line 0002, archived line: word, silence, meaning
/public/posts/formula/lines/line-0001.html   -> line 0001, archived line: thought, attention, body, past
```

Do not confuse Formula with Public Thoughts.

Do not move Formula pages into Public Thoughts.

## Metadata quality requirements for this command

For Formula pages only:

Remove emergency-generated residues such as:

```text
- Page context: ...
- PT / posts / formula
- Russian / Belarusian / Spanish labels inserted only to dedupe titles
- doctype, html, function, const, github.io, location.pathname.split, filter, boolean, window, repo in keywords
```

Metadata should be natural in each language, based on current Formula line meaning.

Recommended English examples:

```text
Line 0004 title:
Ashraellen — Path, Action, Rhythm

Line 0004 description:
Current Ashraellen formula line on path, action and rhythm: short forms of thought where movement learns its measure.

Line 0003 title:
Ashraellen — Boundaries, Measure, Form

Line 0002 title:
Ashraellen — Word, Silence, Meaning

Line 0001 title:
Ashraellen — Thought, Attention, Body, Past
```

Use analogous natural transcreated metadata for other languages.

Do not use language/path labels as a substitute for meaning.

## JSON-LD requirements

Each page should have one JSON-LD block.

The JSON-LD must not have generic unrelated description if page-specific meaning is known.

Check:

```text
- @id matches the page URL with #webpage or equivalent
- url matches canonical URL exactly
- name matches or naturally corresponds to <title>
- description matches or naturally corresponds to meta description
- breadcrumb item for current page uses correct URL
- no trailing slash after `.html` URLs
- inLanguage matches the HTML language
```

## Navigation requirements

Keep Formula navigation functional.

Recommended structure:

```text
- current line links to previous line archive where appropriate;
- previous line links back to current and older archived lines where appropriate;
- archived line pages link to the Formula index/line archive as appropriate;
- language navigation/header links remain valid.
```

Do not introduce `href="#"` as final navigation.

## Validation requirements

After editing, read back representative files from the repository, including at least:

```text
ru/public/posts/formula/index.html
en/public/posts/formula/index.html
en/public/posts/formula/lines/line-0001.html
pt/public/posts/formula/index.html
be/public/posts/formula/lines/line-0002.html
```

Verify by inspection:

```text
- visible Formula content is present in raw HTML;
- `formulaRoot` empty shell is no longer the main body;
- `formula-multilingual.js` is not loaded by Formula pages;
- page has static title/description/keywords/canonical;
- keywords do not contain code garbage;
- JSON-LD is page-specific;
- no `.html/` breadcrumb URL error appears;
- no non-Formula files were changed.
```

If possible, run or rely on the safe audit workflow only after changes, but do not run emergency repair scripts.

If you cannot run scripts locally or through a safe workflow, record validation by repository read-back.

## Required output report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_003_Formula_Staticization.md
```

Use:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Your report must include:

```text
1. Files read.
2. Files changed.
3. Commit hashes.
4. Exact list of Formula pages staticized.
5. Whether any Formula page could not be staticized and why.
6. Confirmation that no non-Formula live HTML files changed.
7. Confirmation that workflows/scripts/sitemap/assets/formula JSON/JS were not changed.
8. Representative before/after notes for EN and PT pages.
9. Validation performed.
10. Any unresolved language/transcreation quality issues.
11. Recommended next command.
```

## Forbidden report behavior

Do not paste huge full HTML files into the report.

Use concise excerpts only when needed, such as:

```text
- title
- description
- first formula card text
- removed script reference status
```

## Decision boundary

If you discover that staticization requires editing scripts, CSS, JSON, workflow files, or non-Formula pages, stop and report the blocker. Do not exceed the approved scope.

If the implementation becomes too large to do safely in one pass, report partial completion and recommend splitting by language or line number.

## Success condition

This command is complete when:

```text
- all feasible Formula pages are self-contained static HTML;
- Formula pages no longer depend on formula-multilingual.js for visible content or metadata;
- Formula metadata no longer contains emergency-generated code/path residue;
- no forbidden files were changed;
- REPORT_003_Formula_Staticization.md exists in the APM workspace.
```
