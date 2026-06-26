# MainSite — Ashraellen website memory

Status: active working memory hub  
Created: 2026-06-22  
Repository: `Ashraellen/apm`  
Root path: `Projects/Ashraellen/MainSite/`

## Purpose

This directory is the central memory hub for all work related to the main Ashraellen website: structure, content, multilingual versions, grant positioning, technical decisions, SEO/metadata, assets, landing pages, and incoming summaries from older chats.

The goal is not to replace the live website repository. This directory is a working archive and coordination layer: first gather information from scattered chats, then sort it, then create one clean master file for future site work.

## Working principle

1. Each old chat that contains site-related work should produce a compact handoff file.
2. Those files should be placed in `Inbox_From_Chats/`.
3. After review, stable decisions move into `Decisions/` and/or `MASTER_MainSite.md`.
4. Current tasks and unresolved questions go into `Tasks/`.
5. Technical implementation details go into `Technical/`.
6. Language and translation decisions go into `Languages/`.
7. Content architecture and public positioning go into `Content/` and `Grant_Positioning/`.
8. Active implementation decisions and transitional architecture notes may be placed in `Working_Notes/` before they are merged into the master memory.

## Directory map

```text
Projects/Ashraellen/MainSite/
├── INDEX.md
├── MASTER_MainSite.md
├── Decisions/
│   ├── 2026-06-22_current_chat_site_decisions.md
│   ├── Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
│   ├── Public_Thoughts_Arc_Page_Navigation_Rule_2026-06-24.md
│   ├── Mark_Of_Presence_Label_Rule_2026-06-24.md
│   └── Support_Thoughts_Anti_Duplication_System_2026-06-25.md
├── Inbox_From_Chats/
│   └── README.md
├── Prompts/
│   └── Request_Other_Chats_Site_Memory.md
├── Content/
│   ├── README.md
│   ├── Support_Thoughts_Source_Register.md
│   └── Telegram_Channel_Scan_Log.md
├── Languages/
│   └── README.md
├── Technical/
│   └── README.md
├── Grant_Positioning/
│   └── README.md
├── Assets/
│   └── README.md
├── Working_Notes/
│   ├── RU_Public_Thoughts_Migration_2026-06-22.md  [SUPERSEDED — historical only]
│   └── RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md
├── Session_Logs/
│   ├── MS_SL_RU_Public_Thoughts_2026-06-22.md
│   ├── MS_SL_RU_Public_Thoughts_Arcs_2026-06-22.md
│   ├── MS_SL_RU_Public_Thoughts_Build_2026-06-23.md
│   ├── MS_SL_RU_Public_Thoughts_Assets_2026-06-23.md
│   ├── MS_SL_RU_Public_Thoughts_0007_0012_2026-06-23.md
│   ├── MS_SL_RU_Public_Thoughts_0013_0018_2026-06-24.md
│   ├── MS_SL_EN_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_PL_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_UK_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_BE_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_PT_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_ES_Public_Thoughts_0001_0012_2026-06-23.md
│   ├── MS_SL_FR_Public_Thoughts_0001_0012_2026-06-23.md
│   └── MS_SL_DE_Public_Thoughts_0001_0012_2026-06-23.md
└── Tasks/
    └── README.md
```

## Current source of truth

Until a full audit is complete, the strongest current sources are:

- `MASTER_MainSite.md` — living master file.
- `Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md` — **canonical source of truth** for the completed multilingual support-thought layer 0001–0012. It defines architecture, terminology, rotation rules, text-protection rules, assets, old-formula preservation, multilingual rollout and next-chat instructions.
- `Decisions/Public_Thoughts_Arc_Page_Navigation_Rule_2026-06-24.md` — active addendum defining arc-page navigation: pages of arcs use only arc-level buttons (`← Previous arc` / `Next arc →` and localized equivalents); the oldest arc omits the next-arc button when no older arc exists.
- `Decisions/Mark_Of_Presence_Label_Rule_2026-06-24.md` — active rule: the seal label must always be exactly `— mark of presence` in English on every language version; it is a symbolic site formula, not a translatable interface string.
- `Decisions/Support_Thoughts_Anti_Duplication_System_2026-06-25.md` — active rule for preventing duplicate support thoughts. It defines exact, formula, image/metaphor, thematic and final-turn duplicates; it requires checking candidates before assigning new numbers.
- `Content/Support_Thoughts_Source_Register.md` — active anti-duplication register of published thoughts. It currently records 0001–0024 as `done`, with formulas, core themes, central images, slugs, assets and duplicate guards.
- `Content/Telegram_Channel_Scan_Log.md` — active scan log for the Telegram channel `https://t.me/ashraellenchannel`; it records reviewed layers, candidate examples, the RU publication of 0019–0024, and last reviewed markers for future support-thought arcs.
- `Decisions/2026-06-22_current_chat_site_decisions.md` — first consolidated memory from the current chat and known prior site decisions.
- `Prompts/Request_Other_Chats_Site_Memory.md` — reusable prompt for extracting site memory from older chats.
- `Working_Notes/RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md` — Russian implementation note for the rotating public support-thoughts system. It supports the canonical decision file but does not override it.
- `Working_Notes/RU_Public_Thoughts_Migration_2026-06-22.md` — **superseded historical note only**. Do not use it as an active architecture source.
- `Session_Logs/MS_SL_RU_Public_Thoughts_Build_2026-06-23.md` — implementation log for creating the correct 0001–0006 support-thought pages and rebuilding `/ru/public/thoughts/index.html`.
- `Session_Logs/MS_SL_RU_Public_Thoughts_Assets_2026-06-23.md` — implementation log for moving the new support-thought layer image references to `assets/thoughts/` while preserving the old formula layer.
- `Session_Logs/MS_SL_RU_Public_Thoughts_0007_0012_2026-06-23.md` — implementation log for creating support-thoughts 0007–0012 and updating `/ru/public/` as the current live showcase.
- `Session_Logs/MS_SL_RU_Public_Thoughts_0013_0018_2026-06-24.md` — implementation log for creating support-thoughts 0013–0018, updating `/ru/public/` as the current live showcase, rotating `0007–0012` into `/ru/public/thoughts/`, and archiving `0001–0006` as `index-0001.html`.
- `Session_Logs/MS_SL_EN_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the English support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_PL_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Polish support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_UK_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Ukrainian support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_BE_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Belarusian support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_PT_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Portuguese support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_ES_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Spanish support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_FR_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the French support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_DE_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the German support-thought architecture and transcreating 0001–0012.

## Public Thoughts warning for new chats

For `Public Thoughts` / `Опорные мысли`, do not revive older intermediate schemes.

Current canonical pattern:

```text
/[lang]/public/
→ current live six

/[lang]/public/thoughts/
→ newest completed support-thought arc

/[lang]/public/thoughts/index-000N.html
/[lang]/public/thoughts/index-000(N-1).html
...
/[lang]/public/thoughts/index-0001.html
→ older completed arcs in descending historical order; the larger the arc number, the newer the arc

/[lang]/public/thoughts/arcs/0001-cheerfulness.html
/[lang]/public/thoughts/arcs/0002-still-the-same.html
→ individual support-thought pages

/[lang]/public/posts/formula/
→ short formulas, separate branch

/[lang]/public/formulas/
→ old historical formula layer, preserve unless explicitly decided otherwise
```

Do not use as active architecture:

```text
/[lang]/public/thoughts/01-cheerfulness/
/[lang]/public/thoughts/arcs/arc-0001.html
/[lang]/public/formulas/arcs/
```

## Anti-duplication rule for new arcs

Before creating any new support-thought arc, read:

```text
Decisions/Support_Thoughts_Anti_Duplication_System_2026-06-25.md
Content/Support_Thoughts_Source_Register.md
Content/Telegram_Channel_Scan_Log.md
```

Do not assign new official numbers until candidates have been checked against the register for formula, central image, core theme, final turn and source reuse.

If a candidate has high similarity risk, mark it `review` and ask the user before using it as a new thought.

## Sorting rule

Do not copy raw notes directly into the master file. First place incoming material in `Inbox_From_Chats/`, then extract confirmed decisions, open questions, useful text fragments, technical paths, language/version notes, and outdated or rejected ideas.

This keeps the website memory clean and navigable.
