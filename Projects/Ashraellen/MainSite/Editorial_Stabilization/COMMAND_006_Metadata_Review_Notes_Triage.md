# COMMAND 006 — Metadata Review Notes Triage

Date: 2026-07-01
From: Architect / reviewer chat
To: Executor chat
Status: active command

## Task type

Audit and planning only.

Do not edit the live site in this command.

## Context

Metadata Quality Pass Batch 1 resolved all current generated metadata audit issues.

Current generated audit state:

```text
Pages checked: 550
Pages with issues: 0
Total issues: 0
```

Remaining generated items are review notes only:

```text
DUPLICATE_OG_IMAGE_REVIEW
DUPLICATE_TWITTER_IMAGE_REVIEW
FALLBACK_OG_IMAGE_USED
FALLBACK_TWITTER_IMAGE_USED
```

These are not blocking issues.

## Goal

Triage the remaining image-related review notes and decide whether they require future controlled work or should be accepted as intentional shared/fallback image usage.

This command must produce a plan/report only.

## Required reading

Before auditing, read:

```text
Ashraellen/apm:
Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_005_Metadata_Quality_Pass_Batch_1.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_005_Metadata_Quality_Pass_Batch_1.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md

Ashraellen/ashraellen:
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
sitemap.xml
scripts/audit-page-metadata.js
assets/og/ashraellen-og-home-default-1200x630.jpg
assets/backgrounds/* if needed for understanding image groups
representative pages from each duplicate/fallback image group
```

## Scope

Audit only.

Allowed output:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_006_Metadata_Review_Notes_Triage.md
```

## Forbidden actions

Do not edit:

```text
- any live HTML file
- sitemap.xml
- reports in the live repo
- workflow files
- scripts
- assets
- Formula pages
- Public Thoughts pages
- legacy thought URLs
```

Do not run emergency repair scripts.

Do not trigger emergency metadata repair workflow.

Do not create new OG images.

Do not replace any image reference.

## Audit questions

Answer these questions in the report:

```text
1. Which review note types remain and how many pages are affected?
2. Which image groups are intentional shared images?
3. Which fallback image usages are acceptable for now?
4. Which fallback image usages might need future page-specific images?
5. Are duplicate image notes mostly caused by intentional section-level image reuse?
6. Are there any obvious high-value pages where fallback image use looks weak?
7. Should the next implementation batch fix anything, or should the review notes be accepted for now?
```

## Suggested classification

Use these categories:

```text
ACCEPT_INTENTIONAL_SHARED_IMAGE
ACCEPT_TEMPORARY_FALLBACK
NEEDS_FUTURE_IMAGE_ASSET
NEEDS_METADATA_IMAGE_REFERENCE_REVIEW
NO_ACTION_RECOMMENDED
```

## Required report

Create:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_006_Metadata_Review_Notes_Triage.md
```

Use:

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
```

Report must include:

```text
1. Files read.
2. Audit method.
3. Review note counts.
4. Main image groups and examples.
5. Classification by group.
6. Risk assessment.
7. Recommendation: implement a next batch or accept review notes for now.
8. Confirmation that no live files were changed.
9. Recommended next command.
```

## Decision request

End with one of:

```text
REQUEST_APPROVAL_METADATA_IMAGE_PASS
REQUEST_APPROVAL_ACCEPT_REVIEW_NOTES_FOR_NOW
REQUEST_MORE_ARCHITECT_REVIEW
```

If future image work is clearly needed and low-risk, request a controlled metadata image pass.

If review notes are acceptable for now, request approval to accept review notes for now.

If uncertain, request architect review.

## Success condition

This command is complete when:

```text
- current image-related review notes are triaged;
- REPORT_006_Metadata_Review_Notes_Triage.md exists in APM;
- no live-site files are changed.
```
