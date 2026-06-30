# COMMAND 004 — Formula Staticization Final Audit

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Audit and verification only.

Do not edit the live site in this command.

## Context

Formula staticization has been completed through staged batches:

```text
Batch A: RU, EN, PT
Batch B: PL, DE, ES, FR
Batch C: UK, BE
Manual handoff: final three BE Formula pages
```

The manual BE handoff was accepted in:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003C_Manual_BE_Handoff_Accepted.md
```

## Goal

Perform a final all-language audit of Formula staticization before moving to the next phase.

This audit must verify that all 36 Formula HTML pages are now self-contained static HTML and no longer depend on the Formula runtime renderer for visible content or metadata.

## Repositories

```text
Live site: Ashraellen/ashraellen
Memory:    Ashraellen/apm
```

## Required reading

Before auditing, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_003_Formula_Staticization.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003A_Formula_Staticization_Batch_A.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003B_Retry_Formula_Staticization_Batch_B_Remaining.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_003C_Manual_BE_Handoff_Accepted.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/LOCAL_FILE_HANDOFF_FALLBACK_RULE.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
.github/workflows/sitemap.yml
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
sitemap.xml
all 36 Formula HTML pages listed below
```

## Pages to audit

Languages:

```text
ru, en, pl, de, es, fr, pt, uk, be
```

Routes per language:

```text
/public/posts/formula/index.html
/public/posts/formula/lines/index.html
/public/posts/formula/lines/line-0001.html
/public/posts/formula/lines/line-0002.html
```

Total:

```text
9 languages × 4 routes = 36 pages
```

## Forbidden actions

Do not edit:

```text
- any live HTML file
- sitemap.xml
- workflow files
- scripts
- assets/formula.css
- assets/formula-multilingual.js
- assets/formulas/*.json
- Public Thoughts pages
- legacy thought URLs
- reports inside live repo
```

Do not run emergency repair scripts.

Do not trigger emergency metadata repair workflow.

Do not create local replacement files unless explicitly requested later.

## Audit checklist

For each of the 36 pages, verify:

```text
- page exists;
- raw HTML contains visible Formula content;
- page contains 15 `formula-card` blocks;
- page does not load `formula-multilingual.js`;
- page does not contain `formulaRoot` as an empty shell;
- static <title> exists;
- static meta description exists;
- static meta keywords exists;
- keywords do not contain code garbage such as doctype, html, function, const, github.io, location.pathname, filter, boolean, window, repo;
- static canonical exists;
- JSON-LD exists;
- JSON-LD url matches canonical;
- current breadcrumb item has the same URL as canonical;
- no `.html/` trailing slash appears in page URL fields;
- OG title and description exist;
- Twitter title and description exist;
- stylesheet points to `/assets/formula.css`;
- seal label `— mark of presence` exists.
```

## Generated files check

Also verify current safe generated files state:

```text
- sitemap.xml exists;
- reports/page-metadata-audit.md exists;
- reports/page-keyword-workbench.md exists;
- reports/page-keyword-workbench.json exists;
- any changes to those files are consistent with the safe sitemap/report workflow, not emergency metadata repair.
```

## Required output report

Create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_004_Formula_Staticization_Final_Audit.md
```

Use the report template:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Report must include:

```text
1. Files read.
2. Audit method.
3. Summary table by language.
4. Any failing Formula pages, if found.
5. Confirmation whether all 36 pages are static.
6. Confirmation whether Formula runtime dependency is removed from all 36 pages.
7. Confirmation whether each page has 15 formula cards.
8. Metadata/JSON-LD issues, if found.
9. Generated sitemap/report status.
10. Confirmation that no live files were changed by this audit.
11. Recommended next phase.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_METADATA_QUALITY_PASS
REQUEST_MORE_ARCHITECT_REVIEW
```

If all 36 Formula pages pass, request approval for the metadata quality pass.

If any Formula page fails, request architect review instead.

## Success condition

This command is complete when:

```text
- all 36 Formula pages have been audited;
- REPORT_004_Formula_Staticization_Final_Audit.md exists in APM;
- no live-site files have been changed by this command.
```
