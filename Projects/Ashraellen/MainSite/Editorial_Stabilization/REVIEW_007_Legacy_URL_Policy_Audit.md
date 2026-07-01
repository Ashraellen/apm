# REVIEW 007 — Legacy URL Policy Audit

Date: 2026-07-01
Reviewer: Architect / reviewer chat
Report reviewed: `REPORT_007_Legacy_URL_Policy_Audit.md`
Status: accepted

## Review result

`REPORT_007_Legacy_URL_Policy_Audit.md` is accepted.

The audit confirms that the six legacy RU Public Thoughts URL families and the six current arc URL families both exist.

Actual live legacy slug set:

```text
01-cheerfulness
02-still-the-same
03-let-go
04-mortality-awakens
05-on-your-own
06-insight
```

Current arc set:

```text
0001-cheerfulness.html
0002-still-the-same.html
0003-let-go.html
0004-mortality-awakens.html
0005-on-your-own.html
0006-insight.html
```

## Accepted findings

```text
- legacy pages are currently self-canonical;
- current arc pages are currently self-canonical;
- both URL families are currently included in sitemap.xml;
- no noindex was found on the inspected pages;
- no redirect/meta refresh was found on the inspected pages;
- legacy/current pairs are near-duplicates, not unrelated pages;
- some current arc pages appear stronger or expanded, so automatic canonicalization should not be done casually;
- sitemap generation currently scans HTML files and does not exclude pages based on canonical/noindex state.
```

## Decision

Approved now:

```text
REQUEST_APPROVAL_LEGACY_URLS_LEAVE_UNCHANGED_FOR_NOW
```

Decision:

```text
Leave legacy RU Public Thoughts URLs unchanged for now.
```

Rationale:

```text
- no current metadata audit issue requires immediate action;
- changing canonical only would leave sitemap mismatch;
- adding noindex would require sitemap-generator policy decisions;
- redirecting would require a separate redirect architecture decision;
- deleting legacy URLs is not approved;
- old inbound links may exist;
- partial implementation would create more policy debt than it removes.
```

## Future policy constraint

Any future legacy URL implementation must be a separate narrow command and must define together:

```text
- exact one-to-one URL mapping;
- canonical policy;
- noindex policy;
- redirect policy, if any;
- sitemap-generator behavior;
- JSON-LD / OG URL alignment;
- pilot URL family before broader rollout.
```

## Scope-control note

No live files were changed by COMMAND 007.

Not approved:

```text
- changing canonical tags now;
- adding noindex now;
- adding redirects now;
- deleting legacy pages;
- editing sitemap.xml manually;
- changing sitemap generator;
- changing Public Thoughts content;
- changing Formula pages;
- emergency metadata repair workflow.
```

## Next phase

The main Editorial Stabilization sequence can now move to closeout.

Next command:

```text
COMMAND_008_Editorial_Stabilization_Closeout.md
```
