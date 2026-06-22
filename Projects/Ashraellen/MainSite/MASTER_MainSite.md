# MASTER_MainSite — Ashraellen

Status: draft master file / to be expanded after chat memory import  
Created: 2026-06-22  
Project: Ashraellen main website  
Repository memory path: `Projects/Ashraellen/MainSite/`

## 1. Core definition

The Ashraellen website is not merely a portfolio, blog, link page, or YouTube support page.

Working definition:

> Ashraellen is an independent multilingual artistic-research and literary-philosophical public archive. The site presents a practice of seeing, formulating, recording, translating, and publicly testing meaning through literature, satire, philosophical texts, video, sound, visual formulas, and digital publication.

Preferred external framing:

- independent artistic research;
- literary-philosophical research;
- practice-based cultural research;
- multilingual public research archive;
- artistic research into meaning, perception, language, inner autonomy, and cultural forms.

Avoid presenting the project as:

- a blog;
- a YouTube project;
- spiritual teaching;
- therapy;
- motivational platform;
- infobusiness;
- charity request or personal plea.

## 2. Conceptual hierarchy

Current structural idea for professional and grant-facing pages:

1. mode of seeing;
2. inquiry into meaning;
3. forms of recording;
4. public platform;
5. production infrastructure.

This hierarchy is useful when explaining why the site contains literature, research notes, public texts, books, video/audio traces, multilingual versions, and infrastructure costs.

## 3. Main public structure

Known current site architecture includes:

- `Research`;
- `Public`;
- `Books`;
- `MONOLITH` as a book/universe gateway;
- professional/grant-facing pages;
- multilingual versions.

Known language folders from prior decisions:

- `/ru/`;
- `/en/`;
- `/pl/`;
- `/de/`;
- `/es/`;
- `/fr/`;
- `/pt/`;
- `/uk/`;
- `/fi/` — introduced or discussed for Kone / Finnish-facing landing context.

The site is multilingual and public-facing. It should remain coherent rather than becoming nine disconnected mini-sites.

## 4. Language strategy

General rule:

- Russian remains the primary creative/development language.
- English is the main international/professional/grant-facing language.
- Polish is important for communication in Poland and local institutions.
- Finnish may be used strategically for Kone Foundation and Finland-facing entry points.

Finnish decision currently recorded:

- Do not necessarily translate the entire site into Finnish immediately.
- Create a Finnish landing page / long explanatory page where strategically useful.
- The Finnish page may function as a clear bridge into the full English version.
- Translation may be done through the assistant for now, without hiring a professional translator, unless later grant/publishing needs require professional revision.

## 5. Entry and language behaviour

Known technical/UX decisions:

- Root `/index.html` is the site entrance.
- Manual language selector is preserved via `?manual=1`.
- Browser-language auto-detection / auto-redirect is preserved.
- Unknown browser language may fall back to English.
- PWA manifest/icons remain intact.
- Manual language choice should remain possible even when auto-detection exists.

## 6. SEO and metadata decisions

Known decisions:

- Visible small SEO/project-summary block only on `/en/` and `/ru/`.
- JSON-LD is required.
- `llms.txt` is required or desired as part of AI-readable project context.
- Do not multiply JavaScript placeholders.
- JSON-LD should be static in HTML, not inserted as client-side placeholder JS.
- Workflow order: canonical handling → JSON-LD → sitemap.
- Sitemap generation is automatic.

## 7. MONOLITH gateway decision

Known decisions:

- `https://ashraellen.com/monolith` should be a central gateway, not a blind redirect.
- It should introduce the MONOLITH universe and link to books.
- It should support English and Russian for now.
- It should contain short language description and button-links.
- It should cover BETON, SLUDGE, and future GAS.
- MONOLITH belongs under `Books`, but the short `/monolith/` route remains useful as a public gateway.

## 8. Kone / Finnish landing decision

Current working decision from this chat:

- The site has advanced enough that Kone Foundation should not be approached with only a raw project description.
- A Finnish-facing landing page can be useful.
- The Finnish page should not pretend that the whole project is Finnish-language.
- Better solution: a long, clear Finnish landing page with a link to the detailed English version.
- The landing should serve as a respectful entrance for Finnish readers while the full professional detail remains in English.

## 9. Repository memory workflow

This MainSite folder is not the live website codebase. It is a memory and coordination layer.

Workflow:

1. Ask old chats to produce site-memory files.
2. Place those files in `Inbox_From_Chats/`.
3. Sort and extract confirmed decisions.
4. Update this master file.
5. Move implementation details into `Technical/`.
6. Move public text fragments into `Content/`.
7. Move language strategy into `Languages/`.
8. Move grant/institutional positioning into `Grant_Positioning/`.
9. Maintain open tasks in `Tasks/`.

## 10. Open work

To be done after importing old chat summaries:

- identify all existing site-related files and live website repositories;
- confirm the current live site structure;
- collect all language versions already created;
- collect all professional pages already created;
- collect all Kone-specific pages/texts;
- collect all metadata/SEO/JSON-LD decisions;
- identify what is implemented, what is drafted, and what is only discussed;
- produce a clean `MASTER_MainSite_v1` after sorting incoming materials.

## 11. Rule for future additions

Every future site-related decision should be recorded with:

- date;
- chat/source;
- decision;
- reason;
- status: proposed / accepted / implemented / rejected / outdated;
- affected paths or pages;
- next action.
