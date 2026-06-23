# RU Public Thoughts Migration — SUPERSEDED historical note

Status: superseded / historical only  
Original date: 2026-06-22  
Superseded by: `Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md`

## Do not use this file as current architecture

This file used to contain an intermediate migration plan for the Russian public support-thoughts layer. That intermediate plan is no longer authoritative.

The current source of truth is:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
```

Future chats must read that decision file before touching `Public Thoughts` / `Опорные мысли`.

## Current canonical architecture

For every language:

```text
/[lang]/public/
→ live showcase of the current six support-thoughts

/[lang]/public/thoughts/
→ the newest completed support-thought arc that has left the live showcase

/[lang]/public/thoughts/index-0001.html
/[lang]/public/thoughts/index-0002.html
→ older completed support-thought arcs after rotation

/[lang]/public/thoughts/arcs/0001-cheerfulness.html
/[lang]/public/thoughts/arcs/0002-still-the-same.html
...
→ individual expanded support-thought pages

/[lang]/public/posts/formula/
→ separate branch for short formulas

/[lang]/public/posts/formula/lines/
→ completed lines of short formulas

/[lang]/public/formulas/
→ old historical layer; preserve unless the author explicitly decides otherwise
```

## Explicitly obsolete intermediate ideas

The following ideas are obsolete and must not guide future work:

```text
/[lang]/public/thoughts/01-cheerfulness/
/[lang]/public/thoughts/02-still-the-same/
...
```

as the primary final pattern for individual support-thought pages.

```text
/[lang]/public/thoughts/arcs/arc-0001.html
```

as the final pattern for a completed arc page.

```text
/[lang]/public/formulas/arcs/
```

as a new public-thought architecture.

Also obsolete:

- treating `/[lang]/public/thoughts/` as a generic index of all thoughts;
- treating `/[lang]/public/thoughts/arcs/` as a list of completed arcs;
- mixing the short-formula system `/posts/formula/` with the support-thought system.

## Why this file is kept

This file is retained only as a historical trace of the migration discussion, so that future audits can understand why some temporary paths or older session logs mention different structures.

It must not be treated as a working plan.
