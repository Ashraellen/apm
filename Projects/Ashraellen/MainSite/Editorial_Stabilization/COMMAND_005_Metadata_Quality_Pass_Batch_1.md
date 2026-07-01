# COMMAND 005 — Metadata Quality Pass Batch 1

Date: 2026-06-30
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Controlled implementation.

This is the first narrow metadata quality pass after Formula staticization.

## Approved decision

Approved from:

```text
REVIEW_004_Formula_Staticization_Final_Audit.md
```

Approved scope:

```text
Metadata Quality Pass Batch 1: fix only current generated-audit issue pages.
```

## Target pages

Edit only these two live-site files:

```text
index.html
privacy.html
```

These are the only current pages with issues in:

```text
reports/page-metadata-audit.md
```

Current generated audit state:

```text
Pages checked: 550
Pages with issues: 2
Total issues: 9
```

Current issue pages:

```text
index.html
privacy.html
```

## Goal

Resolve the generated metadata audit issues for the two target pages without changing site behavior.

## Required reading

Before editing anything, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_004_Formula_Staticization_Final_Audit.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_004_Formula_Staticization_Final_Audit.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
index.html
privacy.html
en/privacy.html
.github/workflows/sitemap.yml
scripts/audit-page-metadata.js
```

Read `en/privacy.html` only as context for the root redirect page. Do not edit it in this command.

## Allowed live-site changes

You may edit only:

```text
index.html
privacy.html
```

The safe sitemap/report workflow may later update generated artifacts automatically:

```text
sitemap.xml
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
```

Do not edit these generated files manually.

You may create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_005_Metadata_Quality_Pass_Batch_1.md
```

## Forbidden live-site changes

Do not edit:

```text
- any Formula page
- any Public Thoughts page
- any legacy thought URL
- any localized homepage
- en/privacy.html
- sitemap.xml manually
- .github/workflows/*.yml
- scripts/*.js
- scripts/*.py
- assets/*
- robots.txt
- README.md
- live reports manually
```

Do not run emergency repair scripts.

Do not trigger the emergency metadata repair workflow.

Do not perform broad search/replace.

## Required fixes for index.html

Current generated issue:

```text
MISSING_KEYWORDS
```

Also inspect and correct the known quality issue in JSON-LD breadcrumb if present:

```text
Index.html breadcrumb item pointing to https://www.ashraellen.com/index.html/
```

Required outcome:

```text
- add natural static keywords for root language-entry page;
- keep canonical as https://www.ashraellen.com/;
- keep language chooser behavior;
- keep current browser-language redirect behavior unless a clear safety issue is found and reported;
- keep analytics script as currently used;
- ensure JSON-LD breadcrumb current item does not use `.html/` trailing slash;
- keep OG/Twitter metadata present;
- do not turn this into a broad homepage rewrite.
```

Recommended root keywords:

```text
Ashraellen, Nikolai Kostyshev, books, research, public texts, multilingual archive, literary-philosophical research, inner observation
```

## Required fixes for privacy.html

Current generated issues:

```text
MISSING_KEYWORDS
MISSING_JSON_LD
MISSING_OG_TITLE
MISSING_OG_DESCRIPTION
MISSING_OG_IMAGE
MISSING_TWITTER_CARD
MISSING_TWITTER_IMAGE
DESCRIPTION_TOO_SHORT
```

Required outcome:

```text
- preserve noindex,follow;
- preserve redirect to /en/privacy.html;
- add a longer description;
- add natural static keywords;
- add page-specific JSON-LD;
- add OG title/description/image;
- add Twitter card/title/description/image;
- keep canonical intentional and report what was kept;
- do not change the visible redirect purpose;
- do not edit en/privacy.html.
```

Recommended privacy metadata:

```text
Title: Privacy Policy — Ashraellen
Description: Privacy information for Ashraellen.com, including how the site handles basic analytics, language redirection and user contact data.
Keywords: Ashraellen, privacy policy, website privacy, analytics, language redirection, contact data
OG/Twitter image: https://www.ashraellen.com/assets/og/ashraellen-og-home-default-1200x630.jpg
```

## Validation requirements

After editing, read back both files and verify:

```text
index.html:
- keywords exist;
- canonical remains https://www.ashraellen.com/;
- OG/Twitter metadata still exists;
- JSON-LD exists;
- breadcrumb no longer contains https://www.ashraellen.com/index.html/;
- language chooser and redirect script remain present.

privacy.html:
- noindex,follow remains;
- redirect to /en/privacy.html remains;
- description length is no longer too short;
- keywords exist;
- JSON-LD exists;
- OG title/description/image exist;
- Twitter card/title/description/image exist;
- canonical exists;
- no broad content rewrite occurred.
```

Then either:

```text
- wait for the safe sitemap/report workflow to update generated reports, if it runs automatically;
```

or:

```text
- report that generated reports will update on the next safe workflow run.
```

Do not manually edit generated report files.

## Required output report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_005_Metadata_Quality_Pass_Batch_1.md
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
4. Exact fixes made to index.html.
5. Exact fixes made to privacy.html.
6. Validation performed.
7. Generated report status after commit, if available.
8. Confirmation that no forbidden files were changed manually.
9. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_METADATA_QUALITY_PASS_BATCH_2
REQUEST_MORE_ARCHITECT_REVIEW
```

If both target pages are fixed cleanly, request approval for Metadata Quality Pass Batch 2.

If anything is uncertain, request architect review.

## Success condition

This command is complete when:

```text
- index.html and privacy.html metadata issues are corrected;
- no other live files are manually changed;
- REPORT_005_Metadata_Quality_Pass_Batch_1.md exists in APM.
```
