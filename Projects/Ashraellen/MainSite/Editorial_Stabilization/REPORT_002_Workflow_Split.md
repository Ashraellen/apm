# REPORT 002 — Workflow Split

Date: 2026-06-30
Executor: GPT-5.5 Thinking executor chat
Command file used: `COMMAND_002_Workflow_Split.md`
Status: complete

## 1. Files read

```text
Ashraellen/apm:
- Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_002_Workflow_Split.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_001_Editorial_Stabilization_Plan.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
- Projects/Ashraellen/Website_Static_Metadata_Repair_2026-06-30.md
- Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
- .github/workflows/sitemap.yml
- .github/workflows/metadata-repair.yml
- scripts/audit-page-metadata.js
- scripts/export-page-keyword-workbench.js
- scripts/generate-sitemap.js
- scripts/submit-indexnow.js
- scripts/add-missing-keywords.js
- scripts/clean-public-identity-head.py
- scripts/repair-title-description-og.py
- scripts/repair-structured-social-gaps.py
- scripts/dedupe-page-metadata.py
- scripts/apply-og-from-page-backgrounds.py
```

`Ashraellen/ashraellen/.github/workflows/metadata-repair.yml` did not exist before this task. It was created during this command, then read back for validation.

## 2. Scope performed

```text
- controlled implementation
- workflow split only
- changed only allowed live-site workflow files
- created required APM report
- no HTML changed
- no Formula pages changed
- no sitemap.xml manual edit
- no metadata scripts changed
- no legacy URL changes
- no canonical/noindex changes
- no emergency repair run or triggered
```

## 3. Findings

### Workflow

Before this command, `.github/workflows/sitemap.yml` was still the emergency-style workflow. It ran broad repair scripts automatically on qualifying pushes and committed `**/*.html` together with sitemap and reports.

After this command, `.github/workflows/sitemap.yml` is now the permanent safe workflow only.

It keeps these tasks:

```text
- checkout
- Node setup
- Audit page metadata: node scripts/audit-page-metadata.js
- Export page keyword workbench: node scripts/export-page-keyword-workbench.js
- Generate sitemap.xml: node scripts/generate-sitemap.js
- Submit sitemap URLs to IndexNow: node scripts/submit-indexnow.js
- Commit sitemap.xml and reports if changed
```

It no longer runs these broad repair scripts:

```text
- node scripts/add-missing-keywords.js
- python3 scripts/clean-public-identity-head.py
- python3 scripts/repair-title-description-og.py
- python3 scripts/repair-structured-social-gaps.py
- python3 scripts/dedupe-page-metadata.py
- python3 scripts/apply-og-from-page-backgrounds.py
```

It no longer commits HTML. Its `git add` is limited to:

```text
sitemap.xml
reports/page-metadata-audit.md
reports/page-keyword-workbench.md
reports/page-keyword-workbench.json
```

### Sitemap / IndexNow

Sitemap generation remains automatic through the existing mechanism. `sitemap.xml` was not manually edited in this command.

`submit-indexnow.js` remains in the permanent safe workflow after sitemap generation. It was not edited.

### Manual emergency repair workflow

A new workflow now exists:

```text
.github/workflows/metadata-repair.yml
```

It is manual-only:

```yaml
on:
  workflow_dispatch:
```

It requires the input:

```yaml
confirm:
  description: 'Type RUN_EMERGENCY_REPAIR to run broad metadata repair scripts'
  required: true
```

It has a job-level guard:

```yaml
if: github.event.inputs.confirm == 'RUN_EMERGENCY_REPAIR'
```

Only this manual emergency workflow may run the broad repair sequence and commit `**/*.html`.

### Risks

The emergency workflow contains broad HTML-writing repair scripts by design. It is safe only because it is manual-only and guarded by the exact confirmation input.

No script-hardening was performed because COMMAND 002 explicitly forbids editing metadata repair scripts.

## 4. Proposed changes

No new implementation changes are proposed inside this command. The approved workflow split was implemented.

Recommended future staged work remains separate:

```text
- Formula staticization
- metadata quality pass
- legacy URL canonical/noindex policy
- optional script hardening for emergency repair tools
```

These were not implemented.

## 5. Files changed

### Ashraellen/ashraellen

```text
Changed file:
- .github/workflows/sitemap.yml

Commit:
- 15c8fa281f15bd04a27aab5108e49c542ead2125

Change summary:
- removed automatic broad repair script steps
- removed emergency repair scripts from push path triggers
- kept audit, keyword workbench export, sitemap generation and IndexNow submission
- changed commit step so it no longer adds or commits `**/*.html`
- changed commit step so it no longer adds `reports/page-backgrounds.md`
```

```text
Changed file:
- .github/workflows/metadata-repair.yml

Commits:
- dbbcc77b8ef96cfc23f7d1fe928990d5aad9c506
- b71dbeaabbba27a49d4ad86f6fe4cd0b41467e5e

Change summary:
- created the new workflow file
- configured it as manual-only workflow_dispatch
- added required `confirm` input
- added job-level guard requiring `RUN_EMERGENCY_REPAIR`
- moved the broad repair sequence into this guarded manual workflow
- allowed HTML commits only inside this emergency workflow
```

The first `metadata-repair.yml` commit created the file as a minimal shell. The second commit replaced it with the final guarded emergency workflow. Final repository state is the configured workflow.

### Ashraellen/apm

```text
Changed file:
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_002_Workflow_Split.md

Commit:
- recorded by GitHub when this report file was created
```

## 6. Validation performed

Read-back validation was performed after the live-site workflow changes.

### `.github/workflows/sitemap.yml`

Verified by inspection:

```text
- contains `workflow_dispatch`
- keeps push trigger for HTML/content-relevant changes
- keeps audit page metadata step
- keeps export page keyword workbench step
- keeps generate sitemap.xml step
- keeps submit IndexNow step
- contains no run step for `scripts/add-missing-keywords.js`
- contains no run step for `scripts/clean-public-identity-head.py`
- contains no run step for `scripts/repair-title-description-og.py`
- contains no run step for `scripts/repair-structured-social-gaps.py`
- contains no run step for `scripts/dedupe-page-metadata.py`
- contains no run step for `scripts/apply-og-from-page-backgrounds.py`
- final git add does not include `**/*.html`
- final git add does not include `reports/page-backgrounds.md`
```

### `.github/workflows/metadata-repair.yml`

Verified by inspection:

```text
- workflow is `workflow_dispatch` only
- includes required `confirm` input
- confirmation description contains `RUN_EMERGENCY_REPAIR`
- job-level guard requires `github.event.inputs.confirm == 'RUN_EMERGENCY_REPAIR'`
- contains broad repair sequence only in this manual emergency workflow
- contains `git add '**/*.html'` only in this emergency workflow
- includes sitemap and report files in its emergency commit step
```

### Commit validation

Verified by commit inspection:

```text
- commit 15c8fa281f15bd04a27aab5108e49c542ead2125 changed only `.github/workflows/sitemap.yml`
- commit dbbcc77b8ef96cfc23f7d1fe928990d5aad9c506 changed only `.github/workflows/metadata-repair.yml`
- commit b71dbeaabbba27a49d4ad86f6fe4cd0b41467e5e changed only `.github/workflows/metadata-repair.yml`
```

### Forbidden-action validation

```text
- no HTML files changed in this command
- no Formula pages changed
- no Formula JSON/JS files changed
- no metadata repair scripts changed
- no Public Thoughts pages changed
- no legacy URLs changed
- no canonical/noindex policy changed
- sitemap.xml was not manually edited
- emergency repair workflow was not run or triggered
```

No workflow was executed from this chat. Validation was by repository read-back and commit inspection only.

## 7. Open questions

No open question blocks review of COMMAND 002 completion.

One later-phase issue remains intentionally unresolved:

```text
The emergency repair scripts are still broad and should remain manual-only. If they need hardening, issue a separate script-hardening command later.
```

## 8. Decision request

REQUEST_APPROVAL_FORMULA_STATICIZATION

Workflow split is complete. The next major approved concept from REVIEW 001 is Formula staticization, but it still requires a separate command before implementation. This request is for the reviewer to decide whether COMMAND 003 should begin Formula staticization or whether a smaller metadata-quality or script-hardening command should come first.

## 9. Recommended next command

Recommended next command:

```text
COMMAND_003_Formula_Staticization.md
```

Scope:

```text
Convert Formula pages from JS/JSON-rendered shells into self-contained static HTML pages with transcreated visible content and static page-specific metadata.
```

Alternative safer next command:

```text
COMMAND_003_Metadata_Repair_Script_Hardening.md
```

Scope:

```text
Harden emergency repair scripts without running them and without changing HTML, so the manual emergency workflow is safer if it is ever used.
```
