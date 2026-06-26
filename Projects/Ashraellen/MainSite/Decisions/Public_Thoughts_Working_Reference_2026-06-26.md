# Public Thoughts — Working Reference

Date: 2026-06-26  
Project: Ashraellen.com / MainSite  
Scope: Public Thoughts / Опорные мысли only  
Status: active working reference

## 1. Purpose

This file is the compact working reference for future work on the `Public Thoughts / Опорные мысли` section.

It is not a historical explanation and not a full audit record.

Its function is simple:

```text
Use the current successful structure.
Use the latest successful page of the same type as the practical template.
Check the required rules before committing.
```

Detailed background remains in the larger decision files.

## 2. Current range

Current published support thoughts:

```text
0001–0024
```

Next working range:

```text
0025–0030 / ДУГА 0005
```

Current Russian layout:

```text
/ru/public/
→ live showcase: 0019–0024 / ДУГА 0004

/ru/public/thoughts/
→ newest completed archive arc: 0013–0018 / ДУГА 0003

/ru/public/thoughts/index-0002.html
→ ДУГА 0002: 0007–0012

/ru/public/thoughts/index-0001.html
→ ДУГА 0001: 0001–0006

/ru/public/thoughts/arcs/
→ individual support-thought pages 0001–0024
```

## 3. Page architecture

For each language, Public Thoughts use this structure:

```text
/[lang]/public/
→ live showcase of the current six support thoughts

/[lang]/public/thoughts/
→ newest completed archive arc

/[lang]/public/thoughts/index-000N.html
→ older completed archive arc by historical arc number

/[lang]/public/thoughts/arcs/0001-title.html
→ individual support-thought page
```

Historical arc mapping:

```text
ДУГА 0001 → 0001–0006
ДУГА 0002 → 0007–0012
ДУГА 0003 → 0013–0018
ДУГА 0004 → 0019–0024
ДУГА 0005 → 0025–0030
```

Archive rule:

```text
The larger the historical arc number, the newer the arc.
/[lang]/public/thoughts/ holds the newest completed archive arc.
index-0001.html holds ДУГА 0001.
```

## 4. Golden-template method

For new Public Thoughts work, use the latest successful page of the same type as the practical template.

Page types:

```text
/[lang]/public/
→ live showcase page

/[lang]/public/thoughts/
→ newest archive arc page

/[lang]/public/thoughts/index-000N.html
→ numbered archive arc page

/[lang]/public/thoughts/arcs/0001-title.html
→ individual support-thought page
```

Working method:

```text
1. Choose the latest successful page of the same type.
2. Copy its structure.
3. Replace content, numbers, slugs, metadata, links, image paths and alt text.
4. Check CSS, seal, cards, navigation, assets and anti-duplication register.
5. Commit changes.
6. Update the register, scan log, INDEX and session log.
```

## 5. CSS for Public Thoughts

Individual support-thought pages use:

```text
assets/public.css
assets/arcs.css
```

Arc and index pages use:

```text
assets/public.css
assets/thoughts.css
```

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Support_Thoughts_CSS_Split_2026-06-25.md
```

## 6. Site-wide CSS principle

This principle applies to the whole Ashraellen.com site, not only to Public Thoughts:

```text
New section or new page type → shared page-type CSS file.
```

`assets/public.css` remains the common foundation.

A page-type stylesheet contains only the rules specific to that page family.

Examples:

```text
assets/research.css
→ Research pages

assets/arcs.css
→ individual support-thought pages

assets/thoughts.css
→ support-thought arc and index pages
```

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Site_Page_Type_Stylesheet_Rule_2026-06-25.md
```

## 7. Seal / mark of presence

All language versions use the same symbolic seal label:

```text
— mark of presence
```

The label remains in English because it is a symbolic site formula, not an interface string.

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Mark_Of_Presence_Label_Rule_2026-06-24.md
```

## 8. Arc cards

Each support-thought card on an arc/index page contains:

```text
image
support-thought number
title
short formula / description
visible open button
```

Button examples:

```text
RU: Открыть мысль →
EN: Open thought →
PL: Otwórz myśl →
```

The whole card may remain clickable. The visible button gives the reader a clear action point.

## 9. Navigation

Arc/index pages use arc-level navigation:

```text
← Предыдущая дуга
Следующая дуга →
```

Individual support-thought pages use thought-level navigation:

```text
← Предыдущая мысль
Следующая мысль →
```

On the last thought of an arc, the transition goes to the next arc page as a whole:

```text
Следующая дуга →
```

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Arc_Page_Navigation_Rule_2026-06-24.md
```

## 10. Assets

Public Thoughts images live in:

```text
assets/thoughts/
```

Filename pattern:

```text
0024-true-enemy-not-ignorance.jpg
0025-next-slug.jpg
```

The old formula-layer images remain separate:

```text
assets/public-formulas/
```

## 11. Text structure

Russian master page blocks:

```text
Смысл
Полный текст
Почему выбрано
Исследовательская заметка
```

`Полный текст` is the authorial master text.

When the author supplies `Полный текст`, preserve it exactly.

Other language versions use literary transcreation.

Transcreation keeps:

```text
meaning
rhythm
image
philosophical density
final strike
```

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
```

## 12. Anti-duplication

Before selecting or numbering a new arc, use:

```text
Projects/Ashraellen/MainSite/Decisions/Support_Thoughts_Anti_Duplication_System_2026-06-25.md
Projects/Ashraellen/MainSite/Content/Support_Thoughts_Source_Register.md
Projects/Ashraellen/MainSite/Content/Telegram_Channel_Scan_Log.md
```

Candidate check fields:

```text
formula
central image
core theme
emotional mechanism
final turn
source reuse
slug/title collision
```

Official numbers are assigned after this check.

## 13. Files to update after Public Thoughts work

After creating or rotating a Public Thoughts arc, update:

```text
Projects/Ashraellen/MainSite/Content/Support_Thoughts_Source_Register.md
Projects/Ashraellen/MainSite/Content/Telegram_Channel_Scan_Log.md
Projects/Ashraellen/MainSite/INDEX.md
Projects/Ashraellen/MainSite/Session_Logs/<new_session_log>.md
```

If the work creates a reusable rule, add or update a decision file in:

```text
Projects/Ashraellen/MainSite/Decisions/
```

## 14. Core references

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Current_Status_Addendum_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Arc_Page_Navigation_Rule_2026-06-24.md
Projects/Ashraellen/MainSite/Decisions/Mark_Of_Presence_Label_Rule_2026-06-24.md
Projects/Ashraellen/MainSite/Decisions/Support_Thoughts_CSS_Split_2026-06-25.md
Projects/Ashraellen/MainSite/Decisions/Site_Page_Type_Stylesheet_Rule_2026-06-25.md
Projects/Ashraellen/MainSite/Decisions/Support_Thoughts_Anti_Duplication_System_2026-06-25.md
Projects/Ashraellen/MainSite/Content/Support_Thoughts_Source_Register.md
Projects/Ashraellen/MainSite/Content/Telegram_Channel_Scan_Log.md
```

## 15. Scope boundary

This reference governs only:

```text
Public Thoughts / Опорные мысли
```

Other Ashraellen.com sections may use different page architecture, navigation and templates.

The shared CSS principle for new page types applies site-wide.
