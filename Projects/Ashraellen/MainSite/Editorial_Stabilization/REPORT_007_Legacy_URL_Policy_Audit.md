# REPORT 007 — Legacy URL Policy Audit

Date: 2026-07-01
Executor: GPT-5.5 Thinking executor chat
Command file used: `COMMAND_007_Legacy_URL_Policy_Audit.md`
Status: complete / audit and policy planning only

## 1. Files read

```text
Ashraellen/apm:
- Projects/Ashraellen/MainSite/Editorial_Stabilization/COMMAND_007_Legacy_URL_Policy_Audit.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/INDEX.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_001_Editorial_Stabilization_Plan.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_001_Editorial_Stabilization_Plan.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_006_Metadata_Review_Notes_Triage.md
- Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_TEMPLATE.md
- Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md

Ashraellen/ashraellen:
- sitemap.xml
- reports/page-metadata-audit.md
- reports/page-keyword-workbench.md
- reports/page-keyword-workbench.json
- robots.txt
- scripts/generate-sitemap.js
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

The command-listed legacy paths with older expected names were also checked:

```text
- ru/public/thoughts/02-belief/index.html — not found
- ru/public/thoughts/03-choice/index.html — not found
- ru/public/thoughts/04-trust/index.html — not found
- ru/public/thoughts/05-waiting/index.html — not found
```

The actual live legacy slug set is:

```text
01-cheerfulness
02-still-the-same
03-let-go
04-mortality-awakens
05-on-your-own
06-insight
```

## 2. Audit method

This command was audit and policy planning only.

Method:

```text
1. Read the active command and required APM/review context.
2. Read current generated metadata audit and keyword workbench outputs.
3. Read robots.txt and sitemap.xml.
4. Checked required command-listed legacy paths.
5. Recorded the actual live legacy slug set where names differed.
6. Read each actual legacy RU thought page.
7. Read each corresponding current RU arc page.
8. Compared URL family, canonical, visible content pattern, noindex/redirect indicators, and sitemap presence.
9. Read generate-sitemap.js to understand whether canonical/noindex changes would affect sitemap inclusion.
10. Made no live-site changes.
```

## 3. Legacy/current URL inventory

| Family | Legacy URL exists? | Current arc URL exists? | Legacy path | Current path |
|---|---|---|---|---|
| 01 cheerfulness | yes | yes | `ru/public/thoughts/01-cheerfulness/index.html` | `ru/public/thoughts/arcs/0001-cheerfulness.html` |
| 02 still-the-same | yes | yes | `ru/public/thoughts/02-still-the-same/index.html` | `ru/public/thoughts/arcs/0002-still-the-same.html` |
| 03 let-go | yes | yes | `ru/public/thoughts/03-let-go/index.html` | `ru/public/thoughts/arcs/0003-let-go.html` |
| 04 mortality-awakens | yes | yes | `ru/public/thoughts/04-mortality-awakens/index.html` | `ru/public/thoughts/arcs/0004-mortality-awakens.html` |
| 05 on-your-own | yes | yes | `ru/public/thoughts/05-on-your-own/index.html` | `ru/public/thoughts/arcs/0005-on-your-own.html` |
| 06 insight | yes | yes | `ru/public/thoughts/06-insight/index.html` | `ru/public/thoughts/arcs/0006-insight.html` |

The command examples using `belief`, `choice`, `trust`, and `waiting` do not match current live filenames. The actual current conceptual sequence is the same one recorded in `REPORT_001_Editorial_Stabilization_Plan.md`.

## 4. Canonical / noindex / redirect / sitemap status

### Canonical status

| Family | Legacy canonical | Current arc canonical |
|---|---|---|
| 01 cheerfulness | `https://www.ashraellen.com/ru/public/thoughts/01-cheerfulness/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0001-cheerfulness.html` |
| 02 still-the-same | `https://www.ashraellen.com/ru/public/thoughts/02-still-the-same/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0002-still-the-same.html` |
| 03 let-go | `https://www.ashraellen.com/ru/public/thoughts/03-let-go/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0003-let-go.html` |
| 04 mortality-awakens | `https://www.ashraellen.com/ru/public/thoughts/04-mortality-awakens/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0004-mortality-awakens.html` |
| 05 on-your-own | `https://www.ashraellen.com/ru/public/thoughts/05-on-your-own/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0005-on-your-own.html` |
| 06 insight | `https://www.ashraellen.com/ru/public/thoughts/06-insight/` | `https://www.ashraellen.com/ru/public/thoughts/arcs/0006-insight.html` |

Current state: both legacy and current arc pages are self-canonical.

### Sitemap status

Both URL families are currently included in `sitemap.xml`.

Legacy URLs included:

```text
https://www.ashraellen.com/ru/public/thoughts/01-cheerfulness/
https://www.ashraellen.com/ru/public/thoughts/02-still-the-same/
https://www.ashraellen.com/ru/public/thoughts/03-let-go/
https://www.ashraellen.com/ru/public/thoughts/04-mortality-awakens/
https://www.ashraellen.com/ru/public/thoughts/05-on-your-own/
https://www.ashraellen.com/ru/public/thoughts/06-insight/
```

Current arc URLs included:

```text
https://www.ashraellen.com/ru/public/thoughts/arcs/0001-cheerfulness.html
https://www.ashraellen.com/ru/public/thoughts/arcs/0002-still-the-same.html
https://www.ashraellen.com/ru/public/thoughts/arcs/0003-let-go.html
https://www.ashraellen.com/ru/public/thoughts/arcs/0004-mortality-awakens.html
https://www.ashraellen.com/ru/public/thoughts/arcs/0005-on-your-own.html
https://www.ashraellen.com/ru/public/thoughts/arcs/0006-insight.html
```

### Noindex status

No `noindex` pattern was found in the inspected legacy/current RU Public Thoughts pages. Repository search for `noindex ru/public/thoughts` returned no results.

### Redirect status

No meta refresh or redirect pattern was found in the inspected legacy/current RU Public Thoughts pages. Repository search for `http-equiv refresh ru/public/thoughts` returned no results.

### Robots status

`robots.txt` currently allows all crawlers and points to the sitemap:

```text
User-agent: *
Allow: /

Sitemap: https://www.ashraellen.com/sitemap.xml
```

### Sitemap generator behavior

`sitemap.xml` is generated by scanning HTML files and normalizing `/index.html` to trailing slash URLs. The generator currently excludes only `.git`, `.github`, `node_modules`, `assets`, `scripts`, `404.html`, `privacy.html`, and Google verification files. It does not inspect canonical tags, noindex tags, or redirect state.

Implication:

```text
A future canonical-only or noindex-only change would not automatically remove legacy URLs from sitemap.xml unless sitemap generation policy is also changed, legacy pages are excluded by path, or legacy pages are redirected/deleted through an approved mechanism.
```

## 5. Duplicate-vs-different assessment

Overall assessment: legacy and current arc pages are near-duplicate pairs, not completely unrelated pages.

Commonalities:

```text
- same conceptual title per family;
- same or very close leading formula line;
- same Public Thoughts / Опорная мысль role;
- same general body structure: kicker, H1, hero image, meaning block, full text, why chosen, research note, navigation, seal;
- same broad metadata image fallback;
- same language: RU;
- same public content function.
```

Differences:

```text
- legacy URLs use short numeric directory routes such as /01-cheerfulness/;
- current URLs use arc file routes such as /arcs/0001-cheerfulness.html;
- legacy pages use `assets/public-formulas/...` images;
- current arc pages use `assets/thoughts/...` images;
- current pages use four-digit arc numbering in visible kicker and navigation;
- some current arc pages contain revised or expanded text compared with the legacy page;
- metadata wording differs because both generations were touched by previous metadata repair passes.
```

The most obvious non-identical example is `06-insight`: the current arc page is textually expanded and stronger than the legacy version. It is therefore safer to treat the current arc page as the preferred editorial version, while preserving the legacy URL for continuity until a full policy is approved.

## 6. Policy recommendation per URL family

Recommended classification for all six audited families:

| Family | Recommended classification | Reason |
|---|---|---|
| 01 cheerfulness | KEEP_SELF_CANONICAL_FOR_NOW | Near duplicate, but current sitemap/generator behavior makes isolated canonical change incomplete. |
| 02 still-the-same | KEEP_SELF_CANONICAL_FOR_NOW | Near duplicate, but implementation should wait for coordinated policy. |
| 03 let-go | KEEP_SELF_CANONICAL_FOR_NOW | Near duplicate, but current and legacy remain live and linked differently. |
| 04 mortality-awakens | KEEP_SELF_CANONICAL_FOR_NOW | Near duplicate, but sitemap includes both. |
| 05 on-your-own | KEEP_SELF_CANONICAL_FOR_NOW | Near duplicate, but no redirect/noindex/canonical implementation should be partial. |
| 06 insight | KEEP_SELF_CANONICAL_FOR_NOW | Current arc is likely preferred, but content differs enough that automatic canonicalization should wait. |

Secondary planning classification:

```text
INSUFFICIENT_EVIDENCE for immediate implementation
```

Reason:

```text
- canonical-only implementation would leave both URL families in sitemap.xml;
- noindex-only implementation would leave self-canonical pages in sitemap.xml unless generator policy changes;
- redirect implementation on a static site needs explicit redirect mechanism approval;
- deleting legacy pages is explicitly not recommended and not approved;
- some current arc pages are revisions, not exact byte-for-byte duplicates;
- old legacy links may exist outside the site.
```

## 7. Policy options assessed

### KEEP_SELF_CANONICAL_FOR_NOW

Recommendation: yes, safest immediate policy.

Pros:

```text
- no live-site behavior changes;
- no accidental loss of old inbound links;
- no partial canonical/noindex/sitemap mismatch introduced now;
- preserves current generated audit status;
- gives architect time to define full legacy URL policy.
```

Cons:

```text
- duplicate/near-duplicate URL families remain indexed signals;
- both legacy and current arc URLs remain in sitemap.xml;
- current arc pages are not yet clearly declared as preferred versions.
```

### CANONICALIZE_LEGACY_TO_CURRENT

Recommendation: possible future policy, but not recommended as a standalone first implementation.

Reason:

```text
This would make current arc pages the preferred versions without breaking legacy pages. However, the sitemap generator would still include legacy pages unless a separate sitemap exclusion policy is approved. Canonical-only implementation would improve signals but not fully resolve URL-family duplication.
```

### NOINDEX_LEGACY_FOLLOW

Recommendation: not recommended as a first step.

Reason:

```text
Noindex would remove legacy pages from index over time but would leave them in sitemap.xml under the current generator. Combining noindex and canonical also risks mixed signals and was explicitly avoided in the earlier plan.
```

### REDIRECT_LEGACY_TO_CURRENT

Recommendation: not recommended without a separate redirect architecture decision.

Reason:

```text
This static site does not currently show an approved legacy redirect mechanism for these pages. Meta refresh / JavaScript redirects would be a visible behavior change and require explicit approval. Server-level 301 redirects may not be available through the current static hosting setup.
```

### MERGE_OR_REWRITE_REQUIRED

Recommendation: not now.

Reason:

```text
The current arc pages already appear to be the stronger editorial route, but merging/rewrite work would touch Public Thoughts content and should be handled only after a dedicated Public Thoughts editorial command.
```

## 8. Risk assessment

### Leave unchanged for now

Risk: low.

```text
- No immediate technical metadata issues are present.
- No new inconsistency is introduced.
- Legacy URLs remain accessible.
- Duplicate signals remain, but they already exist and are stable.
```

### Canonicalize legacy to current now

Risk: medium.

```text
- Improves preferred URL signal.
- Does not remove legacy URLs from sitemap.xml under the current generator.
- Would require exact per-family mapping and careful update of six legacy files.
- Could create inconsistency if only canonical changes while JSON-LD and OG URLs remain legacy self-URLs.
```

### Noindex legacy now

Risk: medium.

```text
- Removes legacy pages from indexing over time.
- Leaves sitemap mismatch unless generator policy changes.
- Should not be combined casually with canonical changes.
```

### Redirect legacy now

Risk: medium to high.

```text
- Changes user-facing behavior.
- Requires redirect method decision.
- May affect old inbound links and navigation chains.
```

## 9. Recommended future policy path

Recommended next policy path:

```text
1. Leave all legacy Public Thoughts URLs unchanged for now.
2. Record the exact one-to-one legacy-to-current mapping from this report.
3. Do not change canonical/noindex/redirect/sitemap until a single coherent policy is approved.
4. If future implementation is approved, prefer a narrow pilot on one family first, not all legacy routes at once.
5. Before any implementation, decide whether sitemap generator should exclude noncanonical/noindex legacy pages or whether legacy URLs should remain sitemap-visible.
```

Potential future implementation options, in safest order:

```text
Option A — Accept legacy URLs as permanent alternate archive pages:
- keep self-canonical;
- keep sitemap inclusion;
- optionally improve visible labels later;
- no redirect/noindex.

Option B — Prefer current arcs while preserving legacy access:
- canonicalize each legacy page to its current arc counterpart;
- align JSON-LD/OG URL policy if approved;
- decide whether sitemap generator should exclude canonicalized legacy routes.

Option C — Retire legacy from index but keep access:
- noindex,follow legacy pages;
- update sitemap generation policy so noindex pages are excluded;
- avoid combining with canonical unless explicitly approved.

Option D — Redirect legacy to current:
- only if a static-site redirect mechanism is approved;
- update sitemap behavior accordingly;
- test on one URL family before broader rollout.
```

## 10. Confirmation that no live files were changed

Confirmed.

This command did not change:

```text
- any live HTML file;
- canonical tags;
- noindex tags;
- redirects;
- sitemap.xml;
- robots.txt;
- workflow files;
- scripts;
- assets;
- Formula pages;
- generated reports in the live repo.
```

No live-site commits were created by this command. No emergency repair script or workflow was run.

Only this APM report was created.

## 11. Open questions

No blocker remains for the audit itself.

Policy question for architect:

```text
Should legacy Public Thoughts URLs be treated as permanent alternate archive pages, or should current /arcs/ URLs become the preferred canonical family later?
```

Implementation should not begin until that policy is explicitly accepted.

## 12. Decision request

REQUEST_APPROVAL_LEGACY_URLS_LEAVE_UNCHANGED_FOR_NOW

The safest immediate policy is to leave legacy Public Thoughts URLs unchanged for now. Legacy and current arc pages are near-duplicate pairs, but a partial canonical/noindex/redirect change would create additional sitemap and metadata-policy questions. A coherent future implementation needs explicit mapping, sitemap behavior decision, and a narrow pilot.

## 13. Recommended next command

Recommended next command:

```text
COMMAND_008_Accept_Legacy_URLs_Leave_Unchanged.md
```

Scope:

```text
Record acceptance that legacy Public Thoughts URLs remain unchanged for now, and define that any future legacy URL implementation must be a separate narrow command with explicit canonical/noindex/redirect and sitemap-generator policy.
```
