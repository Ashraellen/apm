# Telegram Channel Scan Log — Ashraellen support thoughts

Status: active working log  
Project: Ashraellen.com / MainSite / Public Thoughts  
Created: 2026-06-25  
Channel: `https://t.me/ashraellenchannel`  
Public preview: `https://t.me/s/ashraellenchannel`

## Purpose

This file tracks which parts of the Telegram channel have been reviewed for support-thought candidates.

The purpose is not to catalogue the whole channel at once. The purpose is to avoid repeatedly selecting from the same source layer and to prevent duplicate support thoughts.

## Working method

For each new arc:

1. Open the public Telegram preview.
2. Review the nearest available posts or a specific date/message range.
3. Pick 10–12 candidates.
4. Check candidates against `Support_Thoughts_Source_Register.md`.
5. Choose 6 final thoughts for the arc.
6. Record the scan here.
7. Record final published thoughts in `Support_Thoughts_Source_Register.md`.

## Scan record template

```text
## Scan YYYY-MM-DD — Arc 00XX planning

Channel access method:
- Public preview / Telegram export / direct links / user-provided texts

Reviewed range:
- Dates:
- Message links:
- Approximate direction: newest backward / older forward / user-selected cluster

Candidates found:
1.
2.
3.

Duplicate / skip notes:
-

Selected for arc:
-

Last reviewed marker:
- Date:
- Message link or first visible post marker:
- Notes:
```

## Current known scan state

### 2026-06-25 — Arc 0004, thoughts 0019–0024

Channel access method:
- Public Telegram preview.
- Additional user-selected source line for 0024: `Подлинным врагом человека является не его невежество.`

Reviewed range:
- Nearest visible post layer after the material used for 0013–0018.
- Public preview confirmed candidate texts including 0019–0023.
- Exact message links were not backfilled; use public channel source note unless direct links are later needed.

Selected and published in RU:

```text
0019 — Не бомбите
0020 — Народ и масса
0021 — Брачные игры
0022 — Духовность не навязывается
0023 — Цена перехода
0024 — Подлинный враг
```

Duplicate / skip notes:
- Original proposed 0024 from the same post as 0023 (`Исчерпанная роль`) was rejected by the user because it repeated the same source layer.
- Replacement 0024 was accepted from the user-selected first line about ignorance.
- 0023 and 0024 are now independent source centers.

Implementation notes:
- RU individual pages created under `ru/public/thoughts/arcs/0019–0024`.
- RU live showcase `/ru/public/` now points to 0019–0024.
- Previous live arc 0013–0018 moved to `/ru/public/thoughts/` as DUГА 0003.
- Former `/ru/public/thoughts/` arc 0002 moved to `ru/public/thoughts/index-0002.html`.
- `ru/public/thoughts/index-0001.html` navigation updated to point back to `index-0002.html`.
- `0018-image-cannot-be-happy.html` next-arc link updated to `index-0002.html` to avoid a self-loop after rotation.

Duplicate guard:
- These six are now registered as `done` in `Support_Thoughts_Source_Register.md`.
- Do not reuse their formulas, central images or final turns as new thoughts.

Last reviewed marker:
- Exact Telegram message link not logged.
- Next scan should begin after the Arc 0004 source cluster and avoid reusing:
  - returning aggression / bombing;
  - people vs mass;
  - relationship role scripts;
  - spirituality as non-coercion;
  - crisis as price of transition;
  - ignorance vs closed certainty.

### 2026-06-24/25 — Arc 0003, thoughts 0013–0018

Channel access method:
- Public Telegram preview observed in browser-like access during site work.

Reviewed range:
- Nearest available public posts around the material used for 0013–0018.
- Exact message links were not logged during the creative selection pass.

Published from this layer:

```text
0013 — Проблема теряет корону
0014 — Конец лишней войны
0015 — Тонкая мысль требует тишины
0016 — Факт был один
0017 — Свидетель не мешает истине
0018 — Образ не может быть счастлив
```

Duplicate guard:
- These six are now registered as `done` in `Support_Thoughts_Source_Register.md`.
- Do not reuse their formulas, central images or final turns as new thoughts.

Candidate examples visible near this layer, not yet selected:

```text
Не бомбите — и не бомбимы будете
Народ — это не просто большое количество людей
Брачные игры бывают разными
Подлинная духовность не навязывается
Любой переход на новый этап оплачивается кризисом
```

Status of these examples:
- Selected and published later as part of Arc 0004, except original same-source 0024 was replaced.

Last reviewed marker:
- Exact Telegram message link not logged.

## Notes

If exact Telegram message links are needed later, backfill them only from verified public links. Do not invent message IDs.

If a Telegram post has been used but its exact link is missing, write:

```text
Telegram public channel, exact message link to be backfilled.
```

This is acceptable and safer than guessing.
