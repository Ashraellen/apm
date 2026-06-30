# COMMAND 001 — Editorial Stabilization Plan

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Planning and controlled audit only.

Do not make live-site code or HTML changes for this command unless explicitly instructed in a later command.

## Main goal

Prepare a safe editorial stabilization plan after the emergency static metadata repair.

The plan must separate:

```text
- emergency metadata repair tools
from
- permanent editorial workflow
```

The site must not remain dependent on broad automatic repair scripts as the normal way of maintaining page-level meaning, descriptions, titles, keywords, Open Graph, Twitter Card or JSON-LD metadata.

## Repositories

```text
Live site: Ashraellen/ashraellen
Memory:    Ashraellen/apm
```

## Required reading

Before doing anything, read these files:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/INDEX.md
Projects/Ashraellen/WEB.md
Projects/Ashraellen/Website_Static_Metadata_Repair_2026-06-30.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md

Ashraellen/ashraellen:
.github/workflows/sitemap.yml
reports/apm/2026-06-30-static-metadata-repair.md
reports/page-metadata-audit.md
scripts/audit-page-metadata.js
scripts/add-missing-keywords.js
scripts/clean-public-identity-head.py
scripts/repair-title-description-og.py
scripts/repair-structured-social-gaps.py
scripts/dedupe-page-metadata.py
scripts/apply-og-from-page-backgrounds.py
scripts/generate-sitemap.js
scripts/submit-indexnow.js
```

If a file is missing, record that in the report and continue with the available sources.

## What to audit

Create a plan that answers these questions:

### 1. Workflow safety

Which steps in `.github/workflows/sitemap.yml` should remain automatic on every HTML change?

Expected candidate permanent automatic steps:

```text
- audit page metadata
- export keyword workbench if harmless
- generate sitemap.xml
- submit sitemap URLs to IndexNow
- commit sitemap and reports if changed
```

Which steps should become manual-only or emergency-only?

Expected candidate manual/emergency steps:

```text
- add missing static keywords
- clean public identity in ordinary page metadata
- repair title description and OG metadata
- repair structured/social gaps
- dedupe page metadata
- apply OG images from page backgrounds
```

Do not implement this change yet. Propose a clean workflow split.

### 2. Formula pages stabilization

Inspect current Formula pages:

```text
/[lang]/public/posts/formula/
/[lang]/public/posts/formula/lines/
/[lang]/public/posts/formula/lines/line-0002.html
/[lang]/public/posts/formula/lines/line-0001.html
```

Languages:

```text
ru, en, pl, de, es, fr, pt, uk, be
```

Determine what is needed to convert them from JS/JSON-rendered shells into self-contained static HTML pages with:

```text
- visible formulas inside HTML;
- static title;
- static meta description;
- static keywords without code garbage;
- static canonical;
- static JSON-LD description/name aligned with the page;
- static OG/Twitter title and description;
- no reliance on formula-multilingual.js for the main meaning of the page.
```

Do not rewrite these pages yet. Prepare the scope and method.

### 3. Metadata quality audit

Identify representative examples of machine-generated metadata that should be editorially improved.

Look especially for patterns such as:

```text
- Page context: ...
- PT / posts / formula
- language labels instead of natural titles
- generic archive descriptions
- keywords containing doctype, html, const, function, location, github.io or other code terms
```

Do not attempt to fix all examples now. Record patterns and priority groups.

### 4. Legacy URL status

Inspect old duplicate or legacy page families, especially Russian legacy thought URLs such as:

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
```

Compare with:

```text
/ru/public/thoughts/arcs/0001-cheerfulness.html
...
/ru/public/thoughts/arcs/0006-insight.html
```

Prepare recommendation only:

```text
- keep as independent archive pages;
- or mark as legacy with canonical to the current arc pages;
- or noindex/follow;
- or another safer option.
```

Do not implement legacy canonical/noindex changes yet.

## Forbidden actions in this command

Do not:

```text
- edit live HTML pages;
- edit sitemap.xml manually;
- create a new sitemap generator;
- remove formula JSON/JS files;
- delete legacy pages;
- change canonical/noindex status;
- rewrite workflow before approval;
- change APM canon files outside this Editorial_Stabilization workspace;
- make broad repository-wide replacements.
```

## Required output

Create this file in APM:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md
```

Use:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Your report must include:

```text
1. Files read.
2. Current workflow diagnosis.
3. Proposed permanent workflow split.
4. Formula stabilization plan.
5. Metadata quality problem groups.
6. Legacy URL recommendation.
7. Proposed next command for approval.
8. List of exact files that would be changed in the next phase, but without changing them yet.
```

## Decision boundary

The report must end with one of these requests:

```text
REQUEST_APPROVAL_WORKFLOW_SPLIT
REQUEST_APPROVAL_FORMULA_STATICIZATION
REQUEST_APPROVAL_METADATA_QUALITY_PASS
REQUEST_APPROVAL_LEGACY_URL_POLICY
REQUEST_MORE_ARCHITECT_REVIEW
```

If multiple approvals are needed, list them separately.

## Success condition for this command

This command is complete when the report file exists in the APM workspace and gives enough information for the reviewer chat to issue COMMAND 002 without the user copying a long report between chats.
