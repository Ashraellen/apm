# MS_SL_Public_Thoughts_Decision_Cleanup_2026-06-23

Date: 2026-06-23  
Project: Ashraellen MainSite  
Repository: `Ashraellen/apm`

## Purpose

Clean up older intermediate `Public Thoughts` / `Опорные мысли` decisions so future chats do not confuse them with the working multilingual architecture accepted on 2026-06-23.

## Canonical source preserved

The canonical decision remains:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
```

This file is the primary source of truth for:

- multilingual support-thought rollout 0001–0012;
- rotating architecture;
- live showcase rules;
- completed arc rules;
- individual support-thought page paths;
- old formula-layer preservation;
- asset rules;
- numbering;
- terminology;
- text-integrity and transcreation rules.

## Canonical architecture

For every language:

```text
/[lang]/public/
→ live showcase of the current six support-thoughts

/[lang]/public/thoughts/
→ newest completed support-thought arc

/[lang]/public/thoughts/index-0001.html
/[lang]/public/thoughts/index-0002.html
→ older completed support-thought arcs after rotation

/[lang]/public/thoughts/arcs/0001-cheerfulness.html
/[lang]/public/thoughts/arcs/0002-still-the-same.html
...
→ individual expanded support-thought pages

/[lang]/public/posts/formula/
→ short formulas, separate branch

/[lang]/public/formulas/
→ old historical formula layer, preserve unless explicitly decided otherwise
```

## Superseded patterns

The following earlier/intermediate patterns must not be used as active architecture:

```text
/[lang]/public/thoughts/01-cheerfulness/
/[lang]/public/thoughts/02-still-the-same/
...
```

as the primary final individual support-thought page pattern.

```text
/[lang]/public/thoughts/arcs/arc-0001.html
```

as the final completed-arc pattern.

```text
/[lang]/public/formulas/arcs/
```

as a new support-thought architecture.

Also obsolete:

- treating `/[lang]/public/thoughts/` as a generic index of all thoughts;
- treating `/[lang]/public/thoughts/arcs/` as a list of completed arcs;
- mixing `/posts/formula/` with the support-thought system.

## Changes made in APM

1. Updated:

```text
Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Migration_2026-06-22.md
```

The old migration note was rewritten as a short `SUPERSEDED historical note`. It now explicitly points to the 2026-06-23 multilingual decision file and warns not to use the older intermediate schemes.

2. Updated:

```text
Projects/Ashraellen/MainSite/INDEX.md
```

The index now marks the 2026-06-23 multilingual decision file as the canonical source of truth and marks the 2026-06-22 migration note as superseded/historical only.

3. Updated:

```text
Projects/Ashraellen/MainSite/MASTER_MainSite.md
```

The master file now contains a dedicated section:

```text
Public Thoughts / Опорные мысли — canonical architecture
```

This section records the accepted working architecture and explicitly lists obsolete intermediate schemes that must not be revived.

## Commit SHAs

- `RU_Public_Thoughts_Migration_2026-06-22.md` updated: `938010bbb477d27f7000d81c8a7e507f40f632ed`
- `INDEX.md` updated: `6b73b5d020ed6efcef208e9ad53bfd71c8f1f84a`
- `MASTER_MainSite.md` updated: `e78b8f361ba542e82798d624396ed9de1f3fca82`

## Result

Future chats should no longer treat the old `/thoughts/01-.../`, `/thoughts/arcs/arc-0001.html`, or `/formulas/arcs/` ideas as active architecture.

For all new work, read first:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
```

Then use:

```text
Projects/Ashraellen/MainSite/MASTER_MainSite.md
Projects/Ashraellen/MainSite/INDEX.md
```

as current navigation and summary support.
