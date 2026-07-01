# Legacy Public Thoughts URLs — Leave Unchanged For Now

Date: 2026-07-01
Scope: Ashraellen.com / Public Thoughts / RU legacy URLs
Status: active decision

## Decision

Legacy RU Public Thoughts URLs remain unchanged for now.

No canonical, noindex, redirect, sitemap-generator, or content changes are approved at this stage.

## Accepted URL mapping

```text
Legacy: ru/public/thoughts/01-cheerfulness/
Current: ru/public/thoughts/arcs/0001-cheerfulness.html

Legacy: ru/public/thoughts/02-still-the-same/
Current: ru/public/thoughts/arcs/0002-still-the-same.html

Legacy: ru/public/thoughts/03-let-go/
Current: ru/public/thoughts/arcs/0003-let-go.html

Legacy: ru/public/thoughts/04-mortality-awakens/
Current: ru/public/thoughts/arcs/0004-mortality-awakens.html

Legacy: ru/public/thoughts/05-on-your-own/
Current: ru/public/thoughts/arcs/0005-on-your-own.html

Legacy: ru/public/thoughts/06-insight/
Current: ru/public/thoughts/arcs/0006-insight.html
```

## Rationale

The legacy/current pairs are near-duplicates, but they are not guaranteed byte-for-byte duplicates. Some current arc pages may be stronger or expanded.

Current state:

```text
- legacy pages are self-canonical;
- current arc pages are self-canonical;
- both URL families are in sitemap.xml;
- no noindex is present;
- no redirect is present;
- sitemap generation does not currently exclude pages based on canonical/noindex state.
```

A partial implementation would create policy inconsistency.

## Not approved now

```text
- canonicalizing legacy pages to current arcs;
- adding noindex to legacy pages;
- redirecting legacy pages;
- deleting legacy pages;
- manually editing sitemap.xml;
- changing sitemap generator behavior;
- changing Public Thoughts content.
```

## Future requirement

Any future legacy URL implementation must be a separate narrow command and must define:

```text
- exact one-to-one mapping;
- canonical policy;
- noindex policy;
- redirect mechanism, if any;
- sitemap-generator behavior;
- JSON-LD / OG URL alignment;
- one-family pilot before broader rollout.
```

## Source report

```text
Projects/Ashraellen/MainSite/Editorial_Stabilization/REPORT_007_Legacy_URL_Policy_Audit.md
Projects/Ashraellen/MainSite/Editorial_Stabilization/REVIEW_007_Legacy_URL_Policy_Audit.md
```
