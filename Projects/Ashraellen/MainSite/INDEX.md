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
│   └── 2026-06-22_current_chat_site_decisions.md
├── Inbox_From_Chats/
│   └── README.md
├── Prompts/
│   └── Request_Other_Chats_Site_Memory.md
├── Content/
│   └── README.md
├── Languages/
│   └── README.md
├── Technical/
│   └── README.md
├── Grant_Positioning/
│   └── README.md
├── Assets/
│   └── README.md
├── Working_Notes/
│   ├── RU_Public_Thoughts_Migration_2026-06-22.md
│   └── RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md
├── Session_Logs/
│   ├── MS_SL_RU_Public_Thoughts_2026-06-22.md
│   ├── MS_SL_RU_Public_Thoughts_Arcs_2026-06-22.md
│   ├── MS_SL_RU_Public_Thoughts_Build_2026-06-23.md
│   ├── MS_SL_RU_Public_Thoughts_Assets_2026-06-23.md
│   ├── MS_SL_RU_Public_Thoughts_0007_0012_2026-06-23.md
│   ├── MS_SL_EN_Public_Thoughts_0001_0012_2026-06-23.md
│   └── MS_SL_PL_Public_Thoughts_0001_0012_2026-06-23.md
└── Tasks/
    └── README.md
```

## Current source of truth

Until a full audit is complete, the strongest current sources are:

- `MASTER_MainSite.md` — living master file.
- `Decisions/2026-06-22_current_chat_site_decisions.md` — first consolidated memory from the current chat and known prior site decisions.
- `Prompts/Request_Other_Chats_Site_Memory.md` — reusable prompt for extracting site memory from older chats.
- `Working_Notes/RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md` — current final architecture for the Russian public support-thoughts system: `/ru/public/`, `/ru/public/thoughts/`, rotating completed arcs, and individual support-thought pages.
- `Session_Logs/MS_SL_RU_Public_Thoughts_Build_2026-06-23.md` — implementation log for creating the correct 0001–0006 support-thought pages and rebuilding `/ru/public/thoughts/index.html`.
- `Session_Logs/MS_SL_RU_Public_Thoughts_Assets_2026-06-23.md` — implementation log for moving the new support-thought layer image references to `assets/thoughts/` while preserving the old formula layer.
- `Session_Logs/MS_SL_RU_Public_Thoughts_0007_0012_2026-06-23.md` — implementation log for creating support-thoughts 0007–0012 and updating `/ru/public/` as the current live showcase.
- `Session_Logs/MS_SL_EN_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the English support-thought architecture and transcreating 0001–0012.
- `Session_Logs/MS_SL_PL_Public_Thoughts_0001_0012_2026-06-23.md` — implementation log for creating the Polish support-thought architecture and transcreating 0001–0012.

## Sorting rule

Do not throw old information directly into the master file. First place it in `Inbox_From_Chats/`, then extract:

- confirmed decisions;
- open questions;
- useful text fragments;
- technical paths/files;
- language/version notes;
- outdated or rejected ideas.

This prevents the website memory from becoming a holy landfill with a navigation menu.
