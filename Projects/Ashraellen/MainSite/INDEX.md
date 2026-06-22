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
└── Tasks/
    └── README.md
```

## Current source of truth

Until a full audit is complete, the strongest current source is:

- `MASTER_MainSite.md` — living master file.
- `Decisions/2026-06-22_current_chat_site_decisions.md` — first consolidated memory from the current chat and known prior site decisions.
- `Prompts/Request_Other_Chats_Site_Memory.md` — reusable prompt for extracting site memory from older chats.

## Sorting rule

Do not throw old information directly into the master file. First place it in `Inbox_From_Chats/`, then extract:

- confirmed decisions;
- open questions;
- useful text fragments;
- technical paths/files;
- language/version notes;
- outdated or rejected ideas.

This prevents the website memory from becoming a holy landfill with a navigation menu.
