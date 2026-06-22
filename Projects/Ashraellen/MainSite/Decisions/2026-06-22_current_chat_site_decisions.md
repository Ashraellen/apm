# 2026-06-22 — Current chat site decisions and gathered memory

Status: accepted / initial consolidation  
Source: current MainSite memory setup chat + known prior site decisions from project context  
Project: Ashraellen main website

## 1. Main decision of this chat

Create a dedicated memory structure for the Ashraellen main website inside the APM repository:

`Projects/Ashraellen/MainSite/`

Purpose:

- collect site-related decisions from multiple chats;
- store incoming summaries from old chats;
- sort the material;
- build a future master file;
- preserve technical, language, content, grant, and asset decisions separately;
- avoid losing site logic across many separate conversations.

This directory is a memory/coordination layer, not necessarily the live site codebase.

## 2. Structure accepted in this chat

Created/accepted structure:

```text
Projects/Ashraellen/MainSite/
├── INDEX.md
├── MASTER_MainSite.md
├── Decisions/
├── Inbox_From_Chats/
├── Prompts/
├── Content/
├── Languages/
├── Technical/
├── Grant_Positioning/
├── Assets/
└── Tasks/
```

Meaning of sections:

- `INDEX.md` — navigation and purpose of the MainSite memory hub.
- `MASTER_MainSite.md` — living master file to be improved after importing old chat summaries.
- `Decisions/` — accepted decisions and dated decision logs.
- `Inbox_From_Chats/` — raw exports/summaries from older chats.
- `Prompts/` — reusable prompts for extracting site memory from old chats.
- `Content/` — site texts, page logic, section descriptions, landing copy.
- `Languages/` — multilingual strategy, translation decisions, language-specific notes.
- `Technical/` — GitHub Pages, redirects, JSON-LD, sitemap, PWA, structure.
- `Grant_Positioning/` — professional and institutional framing of the site.
- `Assets/` — visual/audio/branding asset notes.
- `Tasks/` — open tasks and next actions.

## 3. Core site positioning

Accepted/project-consistent framing:

Ashraellen should be presented as:

- independent artistic research;
- literary-philosophical research;
- practice-based cultural research;
- multilingual public research archive;
- a public platform for recording and translating meaning through literature, satire, visual formulas, video, sound, and digital publication.

Do not present the project as:

- a blog;
- a YouTube project;
- spiritual teaching;
- therapy;
- motivational content;
- infobusiness;
- a request for help.

This framing is especially important for Kone Foundation and other grant/institutional contexts.

## 4. Site hierarchy and conceptual logic

Previously accepted hierarchy for professional pages:

1. mode of seeing;
2. inquiry into meaning;
3. forms of recording;
4. public platform;
5. production infrastructure.

This hierarchy should guide the professional site pages and grant-facing explanations.

## 5. Current language decisions

Known language structure includes:

- Russian as primary creative/development language;
- English as main international/professional/grant-facing language;
- Polish as important local/institutional communication language;
- Finnish as a strategic language for Kone-facing entry if needed.

Known/preserved language folders:

- `/ru/`;
- `/en/`;
- `/pl/`;
- `/de/`;
- `/es/`;
- `/fr/`;
- `/pt/`;
- `/uk/`;
- `/fi/` where relevant.

The site has been discussed as a multilingual site across 9 languages.

## 6. Finnish / Kone decision from this chat

Current accepted direction:

- It may be useful to create a Finnish-facing version/page for Kone Foundation.
- We do not need to translate the entire website into Finnish immediately.
- Better approach: a long Finnish landing page with a clear link to the detailed English version.
- The Finnish page should work as a respectful entrance, not as a fake full Finnish website.
- Translation can be done through the assistant for now, without external translator, unless later needed.

Practical direction:

- Finnish landing page: short enough to be readable, long enough to explain the project properly.
- English version remains the detailed professional source.
- Finnish browser-language users may be routed to Finnish material if implemented, but manual language choice must remain available.

## 7. Entry page and language behaviour

Known technical decisions:

- Root `/index.html` is the site entrance.
- Browser-language auto-detection is preserved.
- Manual language selector is preserved.
- Manual selection can use `?manual=1`.
- Unknown browser language falls back to English or language selector depending on final implementation.
- PWA manifest/icons are preserved.
- Language buttons/dropdown should remain available; auto-detection should not trap the user.

## 8. Site sections and architecture

Known structure:

- `Research`;
- `Public`;
- `Books`;
- `MONOLITH` gateway;
- professional pages;
- multilingual language folders.

Prior structure drafts included language folders with sections such as:

- `books`;
- `public`;
- `research`;
- `monolith`.

The site is published through GitHub Pages, and sitemap generation is automatic.

## 9. SEO / structured data / AI-readable context

Known decisions:

- Visible SEO/project-summary block only on `/en/` and `/ru/`.
- JSON-LD should be static in HTML.
- Avoid client-side JavaScript placeholders for JSON-LD.
- `llms.txt` is desired/required as an AI-readable project summary.
- Workflow order: canonical handling → JSON-LD → sitemap.
- Sitemap should be generated automatically.

## 10. MONOLITH gateway

Known decisions:

- `/monolith/` should be a gateway page, not a blind redirect.
- It should introduce the MONOLITH universe.
- It should link to BETON, SLUDGE, and future GAS.
- It should support English and Russian for now.
- It should have a short language description and clear button-links.
- MONOLITH conceptually belongs under `Books`, but the short route `/monolith/` remains useful for public navigation.

## 11. Professional / grant pages

Known prior work:

- Professional pages were drafted/prepared for English and Russian.
- A Finnish Kone-facing page was discussed/prepared as a strategic landing.
- Budget/infrastructure language should explain tools as research infrastructure, not as casual subscriptions.
- The site should support applications and cultural/institutional presentation.

## 12. Method page

Known memory:

- The Method section/page was completed on all 9 languages.
- This should be treated as completed unless later audit proves otherwise.

## 13. Important distinction

The website is not subordinate to YouTube. YouTube can be one public form of the practice, but the website is the larger archive and professional frame.

## 14. Next action

Use the prompt in:

`Projects/Ashraellen/MainSite/Prompts/Request_Other_Chats_Site_Memory.md`

Then collect the resulting files in:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/`

After enough old chat summaries are gathered, sort them into:

- accepted decisions;
- implemented technical files;
- old/outdated ideas;
- open tasks;
- content drafts;
- language/version notes;
- grant-facing material.
