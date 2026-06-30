# REPORT 001 — Editorial Stabilization Plan

Date: 2026-06-30
Executor: GPT-5.5 Thinking executor chat
Command file used: `COMMAND_001_Editorial_Stabilization_Plan.md`
Status: complete — needs approval

## 1. Files read

```text
Ashraellen/apm:
- Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_001_Editorial_Stabilization_Plan.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
- Projects/Ashraellen/MainSite/INDEX.md
- Projects/Ashraellen/WEB.md
- Projects/Ashraellen/Website_Static_Metadata_Repair_2026-06-30.md
- Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
- Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md
- Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
- Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md

Ashraellen/ashraellen:
- .github/workflows/sitemap.yml
- reports/apm/2026-06-30-static-metadata-repair.md
- reports/page-metadata-audit.md
- scripts/audit-page-metadata.js
- scripts/export-page-keyword-workbench.js
- scripts/add-missing-keywords.js
- scripts/clean-public-identity-head.py
- scripts/repair-title-description-og.py
- scripts/repair-structured-social-gaps.py
- scripts/dedupe-page-metadata.py
- scripts/apply-og-from-page-backgrounds.py
- scripts/generate-sitemap.js
- scripts/submit-indexnow.js
- assets/formula-multilingual.js
- assets/formulas/en.json
- ru/public/posts/formula/index.html
- en/public/posts/formula/index.html
- en/public/posts/formula/lines/index.html
- en/public/posts/formula/lines/line-0001.html
- en/public/posts/formula/lines/line-0002.html
- pl/public/posts/formula/index.html
- de/public/posts/formula/index.html
- es/public/posts/formula/index.html
- fr/public/posts/formula/index.html
- pt/public/posts/formula/index.html
- uk/public/posts/formula/index.html
- be/public/posts/formula/index.html
- ru/public/thoughts/01-cheerfulness/index.html
- ru/public/thoughts/02-still-the-same/index.html
- ru/public/thoughts/03-let-go/index.html
- ru/public/thoughts/04-mortality-awakens/index.html
- ru/public/thoughts/05-on-your-own/index.html
- ru/public/thoughts/06-insight/index.html
- ru/public/thoughts/arcs/0001-cheerfulness.html
- ru/public/thoughts/arcs/0002-still-the-same.html
- ru/public/thoughts/arcs/0003-let-go.html
- ru/public/thoughts/arcs/0004-mortality-awakens.html
- ru/public/thoughts/arcs/0005-on-your-own.html
- ru/public/thoughts/arcs/0006-insight.html
```

No required command-source file was missing. The target report file did not exist before this command and was created in the APM workspace.

## 2. Scope performed

```text
- audit only
- planning only
- no live-site HTML changed
- no live-site workflow changed
- no sitemap changed
- no canonical/noindex policy changed
- no broad repository-wide replacement performed
- one APM report file created in the allowed Editorial_Stabilization workspace
```

## 3. Findings

### Workflow

The current live workflow in `.github/workflows/sitemap.yml` still runs the full emergency metadata repair sequence automatically on every qualifying push to `main`, including every HTML change. The active automatic sequence is:

```text
1. Add missing static keywords
2. Clean public identity in ordinary page metadata
3. Repair title description and OG metadata
4. Repair structured data and social gaps
5. Dedupe page metadata
6. Apply OG images from page backgrounds
7. Audit page metadata
8. Export page keyword workbench
9. Generate sitemap.xml
10. Submit sitemap URLs to IndexNow
11. Commit repaired HTML, sitemap.xml and reports if changed
```

This was correct as an emergency repair bridge after the 2026-06-30 metadata incident, but it is not safe as the permanent editorial model. The workflow currently commits `**/*.html`, which means an ordinary content edit can trigger broad automated rewriting of page metadata across the site.

The metadata audit is currently clean in the narrow technical sense:

```text
Pages checked: 550
Pages with issues: 0
Total issues: 0
```

However, the same audit records 550 pages with review notes and 2056 total review notes. The most important review notes are shared/fallback OG and Twitter images:

```text
DUPLICATE_OG_IMAGE_REVIEW: 550
DUPLICATE_TWITTER_IMAGE_REVIEW: 550
FALLBACK_OG_IMAGE_USED: 478
FALLBACK_TWITTER_IMAGE_USED: 478
```

These are not emergency errors, but they are editorial quality signals.

### Current workflow diagnosis

Permanent automation should not rewrite meaning-bearing metadata. The following scripts are broad repair tools and should not remain automatic on every HTML change:

```text
- scripts/add-missing-keywords.js
- scripts/clean-public-identity-head.py
- scripts/repair-title-description-og.py
- scripts/repair-structured-social-gaps.py
- scripts/dedupe-page-metadata.py
- scripts/apply-og-from-page-backgrounds.py
```

Observed risks:

```text
- `scripts/add-missing-keywords.js` can extract keyword candidates from raw HTML and script text, which explains keywords such as doctype, html, function, const, github.io and location.pathname.split on Formula pages.
- `scripts/repair-title-description-og.py` appends language/path labels to titles. It also lacks `pt` in its language-name map, which helps explain PT / posts / formula style titles.
- `scripts/repair-structured-social-gaps.py` can insert generic archive descriptions and generic WebPage JSON-LD.
- `scripts/dedupe-page-metadata.py` appends `Page context: ...` to descriptions and path terms to keywords. This removes duplicate warnings, but leaves editorially mechanical metadata.
- `scripts/apply-og-from-page-backgrounds.py` is useful as a repair tool, but as an automatic step it keeps choosing fallback/shared images rather than forcing an editorial OG-image decision.
```

The following steps are safe candidates for permanent automatic operation:

```text
- scripts/audit-page-metadata.js
- scripts/export-page-keyword-workbench.js
- scripts/generate-sitemap.js
- scripts/submit-indexnow.js
- commit sitemap.xml and reports only if changed
```

`export-page-keyword-workbench.js` appears safe as an automatic report generator because it writes reports only and strips script/style/navigation/footer text before extracting workbench terms. It should remain a workbench, not an automatic keyword writer.

### Proposed permanent workflow split

Recommended split:

```text
A. Permanent automatic workflow on HTML/content changes
   - checkout
   - setup Node/Python only as needed
   - run metadata audit
   - export page keyword workbench
   - generate sitemap.xml
   - submit sitemap URLs to IndexNow
   - commit sitemap.xml and report files only if changed
   - never git add `**/*.html` in the permanent automatic workflow

B. Manual/emergency repair workflow
   - trigger only by workflow_dispatch
   - clear name such as `Emergency static metadata repair`
   - run broad repair scripts only after explicit operator choice
   - require a confirmation input such as `confirm: RUN_EMERGENCY_REPAIR`
   - commit HTML only in that explicitly dispatched emergency workflow
```

This preserves sitemap automation without leaving the site dependent on broad repair scripts as normal editorial maintenance.

### Formula pages

Formula section source rules say Formula is separate from Public Thoughts, governed by site-wide transcreation, and the preferred final publication state is self-contained static HTML with transcreated content already present in the page.

Current observed state:

```text
- RU active Formula page is already static enough in the body: visible formulas are present in HTML.
- Non-RU Formula pages are still JS/JSON-rendered shells.
- Non-RU pages load `assets/formula-multilingual.js` and render the visible body into `<div id="formulaRoot"></div>` after page load.
- `formula-multilingual.js` also mutates document.title, meta description, OG description and Twitter description after load.
- Formula JSON files are the current data source for non-RU formula lines.
```

This means the non-RU Formula pages are technically readable by metadata audit, but their main visible meaning is not self-contained static HTML. This conflicts with the stabilized publication principle.

Representative examples:

```text
- en/public/posts/formula/index.html: empty body shell with `formulaRoot`, visible formulas injected by JS.
- en/public/posts/formula/lines/index.html: same shell model.
- en/public/posts/formula/lines/line-0001.html: same shell model.
- en/public/posts/formula/lines/line-0002.html: same shell model.
- pl/de/es/fr/pt/uk/be active Formula index pages also use the same shell + formula-multilingual.js model.
```

Additional Formula metadata defects observed:

```text
- RU formula keywords include code terms such as doctype, html, function, const, github.io and location.pathname.split.
- DE/ES/FR/PT/UK/BE formula pages contain generic archive descriptions and/or code-garbage keywords.
- PT formula page contains `Page context: pt / public / posts / formula` in description and `PT — posts / formula` style title fragments.
- Some `.html` Formula breadcrumb item URLs contain a trailing slash after `.html`.
```

### Formula stabilization plan

Do not delete the JSON/JS layer in the first implementation pass. Stabilize pages first, then decommission the renderer only after proving no live page depends on it.

Recommended method:

```text
1. Treat current Formula JSON files as source material for the non-RU staticization pass.
2. Use the existing RU static Formula page as a structural reference, not as a language source for literal translation.
3. Build all Formula routes as self-contained static HTML for all nine languages.
4. Embed visible H1, lead, line heading, formula cards, tags, navigation and seal directly into each HTML file.
5. Keep `assets/formula.css` as the shared page-type stylesheet.
6. Replace runtime metadata mutation with static `<title>`, description, keywords, canonical, JSON-LD, OG and Twitter metadata.
7. Fix JSON-LD `name`, `description`, `url`, breadcrumb labels and `.html` URL trailing-slash mistakes.
8. Remove `<script defer src="...assets/formula-multilingual.js...">` from Formula pages only after the static body is present.
9. Keep `assets/formula-multilingual.js` and `assets/formulas/*.json` temporarily for rollback/history until a later explicit cleanup command.
10. Run the metadata audit after staticization, but do not let repair scripts rewrite the pages automatically.
```

Scope size:

```text
9 languages × 4 Formula routes = 36 HTML pages
```

### Metadata quality

The site has passed the emergency metadata audit, but several metadata groups need editorial improvement. Priority groups:

```text
1. Code-garbage keywords
   Examples: doctype, html, title, function, const, isgithub, location.hostname.endswith, github.io, repo, location.pathname.split, filter.
   Cause: keyword scripts reading raw HTML/script text.

2. Generic archive descriptions
   Examples: `is part of the Ashraellen multilingual public archive of literary, artistic and research work`.
   Risk: passes length checks but gives weak page meaning.

3. Mechanical `Page context: ...` descriptions
   Useful for deduping, poor as public metadata.

4. Language labels instead of natural titles
   Examples: `Russian`, `Belarusian`, `Spanish`, `PT`, `posts / formula`, `arcs / 0003 / let / go`.

5. JSON-LD too generic or not aligned with page-specific meaning
   Some pages use generic CollectionPage/WebPage descriptions while visible content has specific meaning.

6. Formula pages whose static metadata is better than their static body
   Search/social metadata exists, but the visible content appears only after JS.

7. Fallback/shared OG images
   Not an error, but a high-volume review signal. Important pages should eventually receive page-type or page-specific OG images.
```

Recommended priority order:

```text
P1: Formula pages, because they combine JS-rendered main content with generated metadata artifacts.
P2: Russian legacy thought URLs and current arc pages, because duplicate families compete semantically.
P3: High-value entry/section/book/research pages with generic descriptions or fallback OG images.
P4: Remaining long-tail pages, guided by page-keyword-workbench and audit review notes.
```

### Legacy URLs

The old Russian thought URL family exists and currently self-canonicalizes:

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
```

The current arc pages also exist and self-canonicalize:

```text
/ru/public/thoughts/arcs/0001-cheerfulness.html
/ru/public/thoughts/arcs/0002-still-the-same.html
/ru/public/thoughts/arcs/0003-let-go.html
/ru/public/thoughts/arcs/0004-mortality-awakens.html
/ru/public/thoughts/arcs/0005-on-your-own.html
/ru/public/thoughts/arcs/0006-insight.html
```

Representative comparison of 0001 shows the same title/meaning/text family, but different asset paths and navigation model:

```text
Old legacy URL uses: assets/public-formulas/01-cheerfulness.jpg
Current arc URL uses: assets/thoughts/0001-cheerfulness.jpg
```

Recommendation:

```text
- Keep old legacy files for compatibility and possible backlinks.
- Do not delete them.
- Do not leave them as independent canonical pages if they duplicate current arc pages.
- After approval, set old legacy pages to canonicalize to the current `/arcs/000N-*.html` page where content parity is confirmed.
- Use `noindex,follow` only if the reviewer decides that legacy pages should remain reachable but should not compete in search, especially where content is similar but not exact enough for canonical confidence.
- Prefer not to combine canonical-to-current and noindex/follow in the same first pass unless a specific SEO policy is approved.
```

Safest first implementation policy:

```text
legacy duplicate with confirmed equivalent content -> canonical to current arc page
legacy page with meaningful divergent content -> noindex/follow or preserve for architect review
```

## 4. Proposed changes

### Proposed change 1 — Workflow split

```text
Target repository: Ashraellen/ashraellen
Target files:
- .github/workflows/sitemap.yml
- .github/workflows/metadata-repair.yml

Type of change:
- reduce existing sitemap workflow to permanent safe automation only
- create a separate manual emergency metadata repair workflow

Reason:
- sitemap generation must remain automatic
- broad metadata repair must not run on every HTML change
- permanent workflow must not auto-commit broad HTML rewrites

Risk level: medium
Approval required before implementation: yes
```

### Proposed change 2 — Formula staticization

```text
Target repository: Ashraellen/ashraellen
Target files:
- all 36 Formula HTML pages listed in section 8 below

Type of change:
- convert Formula pages from JS/JSON-rendered shells into self-contained static HTML
- embed visible formulas directly in each HTML page
- replace machine-generated Formula metadata with page-specific static metadata
- remove Formula renderer dependency from those pages after static content is present

Reason:
- public multilingual Formula content should follow transcreation and static HTML publication rules
- main page meaning should not depend on `formula-multilingual.js`

Risk level: high
Approval required before implementation: yes
```

### Proposed change 3 — Metadata quality pass

```text
Target repository: Ashraellen/ashraellen
Target files:
- Formula pages first
- then selected high-priority public/research/book/legacy pages from workbench

Type of change:
- manual/editorial metadata improvements
- remove code-garbage keywords
- remove `Page context` fragments from public descriptions
- replace language/path labels with natural page titles
- align JSON-LD name/description with page meaning

Reason:
- the site is technically clean but still contains emergency-generated editorial residue

Risk level: medium
Approval required before implementation: yes
```

### Proposed change 4 — Legacy URL policy

```text
Target repository: Ashraellen/ashraellen
Target files:
- six old Russian thought legacy pages listed in section 8

Type of change:
- canonicalize confirmed duplicate legacy pages to current arc pages
- or mark selected divergent legacy pages noindex/follow after review

Reason:
- avoid duplicate indexed families while preserving old URLs

Risk level: medium
Approval required before implementation: yes
```

## 5. Files changed

```text
Ashraellen/apm:
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md

Ashraellen/ashraellen:
- No files changed.
- No live-site commits created by this command.
```

This command intentionally created only the required APM report file. No live-site code, HTML, sitemap, workflow, canonical/noindex status or assets were changed.

## 6. Validation performed

```text
- read the command file and report template
- read required APM source files
- inspected current live workflow syntax and step order by reading `.github/workflows/sitemap.yml`
- inspected emergency repair scripts by source reading
- inspected current metadata audit report
- inspected Formula pages across all required language set at least at active index level
- inspected all four English Formula routes as representative non-RU shell pages
- inspected the RU Formula active page as representative static page
- inspected `formula-multilingual.js` and one Formula JSON source file
- inspected the six specified RU legacy thought URL families and matching current arc page headers/canonicals
- confirmed no live-site write action was performed
```

Validation not performed:

```text
- no scripts were run against the live repository
- no generated sitemap comparison was run
- no browser rendering or deployment validation was performed
- no formula staticization was generated
```

These validations were intentionally omitted because COMMAND 001 allowed audit and planning only.

## 7. Open questions

No question blocks the reviewer from issuing COMMAND 002. The next phase is an approval decision, not a clarification dependency.

Decision choices for the reviewer:

```text
- approve workflow split first as the safest next implementation
- approve Formula staticization as a separate content/metadata phase
- approve metadata quality pass priority order
- approve legacy URL canonical/noindex policy
```

## 8. Exact files that would be changed in the next phase

### Workflow split files

```text
.github/workflows/sitemap.yml
.github/workflows/metadata-repair.yml
```

### Formula staticization files

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

### Formula files intentionally not changed in the first staticization pass

```text
assets/formula-multilingual.js
assets/formulas/en.json
assets/formulas/pl.json
assets/formulas/de.json
assets/formulas/es.json
assets/formulas/fr.json
assets/formulas/pt.json
assets/formulas/uk.json
assets/formulas/be.json
assets/formula.css
```

These should be preserved until after static pages are verified.

### Legacy URL policy files

```text
ru/public/thoughts/01-cheerfulness/index.html
ru/public/thoughts/02-still-the-same/index.html
ru/public/thoughts/03-let-go/index.html
ru/public/thoughts/04-mortality-awakens/index.html
ru/public/thoughts/05-on-your-own/index.html
ru/public/thoughts/06-insight/index.html
```

### Emergency scripts that may be edited later if the reviewer wants safer manual repair tools

```text
scripts/add-missing-keywords.js
scripts/repair-title-description-og.py
scripts/repair-structured-social-gaps.py
scripts/dedupe-page-metadata.py
scripts/apply-og-from-page-backgrounds.py
```

These should not be edited in the workflow-split command unless the command explicitly approves script hardening.

## 9. Recommended next command

Recommended next command:

```text
COMMAND_002_Workflow_Split.md
```

Scope:

```text
Implement only the workflow split:
- keep sitemap/audit/report automation on normal HTML changes
- move broad metadata repair scripts to manual emergency workflow_dispatch
- stop automatic commits of `**/*.html` in the permanent sitemap workflow
- do not staticize Formula pages yet
- do not change metadata quality yet
- do not change legacy canonical/noindex policy yet
```

Reason:

```text
Workflow split is the safety lock. It should happen before Formula staticization or metadata quality work, otherwise every ordinary page edit still risks awakening the old emergency machinery.
```

## 10. Decision request

REQUEST_APPROVAL_WORKFLOW_SPLIT

Approve splitting the current sitemap workflow into permanent safe automation and manual emergency metadata repair. This is the recommended COMMAND 002 because it prevents broad repair scripts from remaining the normal maintenance model.

REQUEST_APPROVAL_FORMULA_STATICIZATION

Approve converting the 36 Formula HTML pages into self-contained static pages with visible formulas and static page-specific metadata, while preserving the JSON/JS layer temporarily for rollback until a later cleanup command.

REQUEST_APPROVAL_METADATA_QUALITY_PASS

Approve an editorial metadata quality pass after workflow split, starting with Formula pages and then prioritizing generated descriptions, code-garbage keywords, path-label titles and high-value pages.

REQUEST_APPROVAL_LEGACY_URL_POLICY

Approve the legacy URL policy: keep the old Russian thought URLs, do not delete them, and canonicalize confirmed duplicates to the current arc pages or mark divergent legacy pages noindex/follow after review.