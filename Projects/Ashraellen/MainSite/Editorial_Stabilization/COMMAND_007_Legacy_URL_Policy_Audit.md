# COMMAND 007 — Legacy URL Policy Audit

Date: 2026-07-01
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Audit and policy planning only.

Do not edit the live site in this command.

## Context

The stabilization sequence so far is complete through:

```text
- workflow safety split;
- Formula staticization;
- generated metadata issue cleanup;
- image review notes triage accepted as non-blocking for now.
```

The remaining unresolved policy area from the original stabilization plan is legacy URL handling.

Original concern:

```text
old RU thought URLs such as /ru/public/thoughts/01-cheerfulness/
current arc pages such as /ru/public/thoughts/arcs/0001-cheerfulness.html
```

Earlier recommendation was not to delete legacy URLs and not to combine canonical + noindex in the first pass.

## Goal

Audit legacy Public Thoughts URL families and prepare a policy recommendation.

This command must not change canonical, noindex, redirects, sitemap, or any live HTML.

## Required reading

Before auditing, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_001_Editorial_Stabilization_Plan.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_006_Metadata_Review_Notes_Triage.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
sitemap.xml
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
robots.txt if present
all relevant legacy and current Public Thoughts pages found during audit
```

## Known URL families to inspect

At minimum, inspect these legacy RU thought URLs if they exist:

```text
ru/public/thoughts/01-cheerfulness/index.html
ru/public/thoughts/02-belief/index.html
ru/public/thoughts/03-choice/index.html
ru/public/thoughts/04-trust/index.html
ru/public/thoughts/05-waiting/index.html
ru/public/thoughts/06-insight/index.html
```

And compare with current arc pages if they exist:

```text
ru/public/thoughts/arcs/0001-cheerfulness.html
ru/public/thoughts/arcs/0002-belief.html
ru/public/thoughts/arcs/0003-choice.html
ru/public/thoughts/arcs/0004-trust.html
ru/public/thoughts/arcs/0005-waiting.html
ru/public/thoughts/arcs/0006-insight.html
```

If names/slugs differ, record the exact paths discovered.

## Audit questions

Answer in the report:

```text
1. Which legacy thought URLs exist?
2. Which current arc URLs exist?
3. Are legacy and current pages duplicates, near-duplicates, or meaningfully different?
4. What canonical URL does each legacy page currently declare?
5. What canonical URL does each current arc page currently declare?
6. Are any legacy URLs included in sitemap.xml?
7. Are any current arc URLs included in sitemap.xml?
8. Are any pages noindex?
9. Are there redirects or meta refreshes?
10. What is the safest policy: keep self-canonical, canonicalize legacy to current, noindex legacy, redirect legacy, or leave unchanged for now?
```

## Policy options to classify

Use these labels:

```text
KEEP_SELF_CANONICAL_FOR_NOW
CANONICALIZE_LEGACY_TO_CURRENT
NOINDEX_LEGACY_FOLLOW
REDIRECT_LEGACY_TO_CURRENT
MERGE_OR_REWRITE_REQUIRED
INSUFFICIENT_EVIDENCE
```

## Forbidden actions

Do not edit:

```text
- any live HTML file
- sitemap.xml
- robots.txt
- workflow files
- scripts
- assets
- Formula pages
- generated reports in the live repo
```

Do not create redirects.

Do not change canonical tags.

Do not add noindex.

Do not delete legacy pages.

Do not run emergency repair scripts.

Do not trigger emergency metadata repair workflow.

## Required output report

Create only this APM report:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_007_Legacy_URL_Policy_Audit.md
```

Use:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Report must include:

```text
1. Files read.
2. Audit method.
3. Legacy/current URL inventory.
4. Canonical/noindex/redirect/sitemap status.
5. Duplicate-vs-different assessment.
6. Policy recommendation per URL family.
7. Risk assessment.
8. Confirmation that no live files were changed.
9. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_LEGACY_URL_POLICY_IMPLEMENTATION
REQUEST_APPROVAL_LEGACY_URLS_LEAVE_UNCHANGED_FOR_NOW
REQUEST_MORE_ARCHITECT_REVIEW
```

If implementation is recommended, keep it narrow and explain exact files and exact canonical/noindex/redirect changes proposed.

If leaving unchanged is safest, request approval to leave legacy URLs unchanged for now.

## Success condition

This command is complete when:

```text
- legacy/current thought URL families are audited;
- REPORT_007_Legacy_URL_Policy_Audit.md exists in APM;
- no live-site files are changed.
```
