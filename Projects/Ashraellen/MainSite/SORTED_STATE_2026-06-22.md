# MainSite — sorted state after MS_01–MS_17 imports

Status: working synthesis
Date: 2026-06-22
Source files: `Inbox_From_Chats/MS_01.md` through `MS_17.md`

## 1. Current site identity

Ashraellen.com is now treated as the main public and institutional website for Ashraellen.

Stable framing:

- independent multilingual literary-philosophical and artistic research practice;
- multilingual public research archive;
- books, research, public formulas, mini-essays, videos, audiobooks, visual materials and professional dossier in one system;
- not a blog, not a YouTube portfolio, not therapy, not motivation, not infobusiness, not a spiritual-service site.

Public author name: `Ashraellen`.
Formal/legal name when needed: `Nikolai Kostyshev`.
Do not use `Ashraellen Live` as current public author name except for legacy context.

## 2. Main live site repository and memory repository

Live website repository:

`Ashraellen/ashraellen`

Project memory repository:

`Ashraellen/apm`

MainSite memory path:

`Projects/Ashraellen/MainSite/`

Imported raw chat memories:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/MS_01.md` through `MS_17.md`

## 3. Current site language set

Current active language roots:

```text
en
ru
pl
de
es
fr
pt
uk
be
```

Earlier stages used 8 languages without Belarusian. Later stages include Belarusian as part of the practical site system, though some mirror automation still explicitly checks:

```text
ru, en, pl, de, es, fr, pt, uk
```

Working rule:

- major structural pages should be implemented across all main languages;
- avoid placeholder pages for important conceptual pages;
- Russian is often the master / development version;
- English is the main international/professional version;
- translations must not become summaries where the source page is full.

## 4. Current top-level architecture

Stable main layers:

```text
Entry
Public
Books
Research
Professional dossier
Contact
Privacy
```

Entry remains visitor-facing, not grant-first. Professional dossier is accessible but not allowed to dominate the homepage.

The site evolved from the earlier formula:

```text
One site. One axis. Two modes of presence.
Research / Public
```

Current accepted entry logic:

```text
Research / Public / Books
```

with Professional dossier, Contact and Privacy as quieter auxiliary doors.

## 5. Core public branches

### Research

Current research architecture:

```text
/<lang>/research/
/<lang>/research/method/
/<lang>/research/projects/
/<lang>/research/archive/
```

Conceptual split:

- `/research/` = entrance / map: what and why;
- `/research/method/` = methodological foundation: how and why this is research;
- `/research/projects/` = large project models / research directions;
- `/research/archive/` = traces, versions, process remains.

`/research/texts/` was removed or rejected as duplicating the Public/Posts layer.

Method page has full multilingual implementation. It includes a collapsed Manifest block, not a separate manifesto page.

### Public

Current public architecture includes:

```text
/<lang>/public/
/<lang>/public/talks/
/<lang>/public/posts/
/<lang>/public/posts/formula/
/<lang>/public/posts/formula/lines/
/<lang>/public/posts/essay/
/<lang>/public/posts/essay/cycles/
/<lang>/public/posts/fragment/
/<lang>/public/posts/sources/
```

Public is not a link dump. It is the public field where thought meets living response.

Important distinction:

- formulas = lines;
- mini-essays = cycles;
- fragments = strong excerpts / semi-literary pieces;
- sources = external references / source points.

Current problem:

- automatically generated multilingual formula pages are scaffolding only;
- they are too thin/compressed and must be manually rewritten, one language at a time.

### Books

Current Books layer includes:

```text
/<lang>/books/
/<lang>/books/monolith/
/<lang>/books/monolith/beton/
/<lang>/books/monolith/sludge/
/<lang>/books/you-are-already-online/
/<lang>/books/the-book-of-whinesis/
/<lang>/books/seccus/
```

Polish Error 404 pages exist / are in progress:

```text
/pl/books/error-404-god-not-found/
/pl/books/error-404-god-not-found/why-me/
```

Book-page canonical structure:

- title / lead;
- about section;
- video / audiobook block when available;
- video description above embedded video;
- multilingual audio-note below video;
- excerpt with read-more/collapse;
- status block;
- muted back-to-books button;
- seal.

## 6. MONOLITH structure

Stable split:

```text
/monolith/                     = public language gateway / social-media hub
/<lang>/monolith/              = short language portal
/<lang>/books/monolith/        = detailed Books-series page
/<lang>/books/monolith/beton/  = detailed BETON volume page
/<lang>/books/monolith/sludge/ = detailed SLUDGE volume page
```

Stable formula:

```text
Books → MONOLITH → Volume → Store
```

Do not turn `/monolith/` into the detailed Books page. It is already used publicly and should remain a fast gateway.

Store policy:

- RU: Russian Google Play + English Amazon;
- EN: English Amazon;
- PL / DE / ES / FR / PT: English Amazon until local editions exist;
- UK: English Amazon + Russian Google Play until Ukrainian editions exist.

Future: add GAS pages when ready.

## 7. Professional / institutional layer

Professional dossier exists across the nine-language site system:

```text
/ru/professional/
/en/professional/
/pl/professional/
/de/professional/
/fr/professional/
/es/professional/
/pt/professional/
/uk/professional/
/be/professional/
```

English is the main international version. Russian remains the working/style reference version.

Professional dossier structure:

1. author;
2. position of observation;
3. method of observation;
4. selected works and fields;
5. public forms of the project;
6. current project seeking support;
7. development plan;
8. technical infrastructure;
9. expected outcomes;
10. audience value;
11. public response;
12. cooperation and support;
13. contact.

Grant framing:

Support is not personal rescue. It enables sustained working time and infrastructure for an already existing artistic-research platform.

## 8. Contact / Privacy / brand rules

Contact pages exist in all main languages. Canonical Telegram distinction:

```text
@AshraellenLive      = direct contact
@ashraellenchannel   = public Telegram channel
```

Professional/public channels wording:

```text
YouTube — multilingual video archive
Instagram — visual public field
Telegram — Russian-language notes and project updates
```

Non-translatable brand elements:

```text
Ashraellen
— mark of presence
```

`Ashraellen` stays Latin-script everywhere.
`— mark of presence` stays English everywhere and is treated as a seal, not an interface label.

Privacy pages should be full language pages in the common site design, not temporary legal stubs.

## 9. Technical baseline

Hosting:

- GitHub Pages;
- custom domain: `www.ashraellen.com`;
- DNS via Namecheap BasicDNS;
- root A records point to GitHub Pages IPs;
- `www` CNAME points to `ashraellen.github.io`.

Root / language:

- root `/index.html` has automatic browser-language redirect;
- static language links must remain available without JavaScript;
- unsupported language fallback: English;
- manual chooser remains available at `/?manual=1`.

PWA:

- installable web app is active;
- `site.webmanifest` start URL must remain `/`;
- do not revert to `/?manual=1` as PWA start URL;
- PWA icons are separate from favicon and Open Graph images.

Analytics:

- GA4 ID: `G-SMQMGSMWQ3`;
- file: `assets/analytics.js`;
- all new HTML pages should include the analytics script unless global injection already covers them.

SEO / AI-readiness pipeline:

```text
canonical links → static link hygiene → JSON-LD → Open Graph → sitemap → IndexNow
```

Important files:

```text
scripts/apply-canonical.js
scripts/apply-static-links.js
scripts/apply-jsonld.js
scripts/apply-og.js
scripts/generate-sitemap.js
scripts/submit-indexnow.js
.github/workflows/sitemap.yml
robots.txt
sitemap.xml
llms.txt
assets/og/ashraellen-og-home-default-1200x630.jpg
```

Rule: core metadata and navigation must exist in static HTML; do not rely on client-side JavaScript for canonical, JSON-LD, OG/Twitter, important navigation, or semantic project summary.

## 10. Visual / CSS architecture

Stable rule:

- major page types may have dedicated CSS;
- language versions of the same semantic page share the same background intentionally;
- different semantic page types should not all reuse one generic background;
- do not delete CSS files without checking deep pages.

Confirmed background/page mapping:

```text
/public/               -> assets/backgrounds/public-bg.webp via assets/public.css
/books/                -> assets/backgrounds/books-bg.webp via assets/books.css
/research/method/      -> assets/backgrounds/research-method-bg.webp via texts.css + method.css
/research/projects/    -> assets/backgrounds/research-projects-bg.webp via research-projects.css
/research/archive/     -> assets/backgrounds/research-archive-bg.webp via research-archive.css
/professional/         -> assets/backgrounds/professional-bg.webp via professional.css
/research/             -> assets/research-bg.jpg via research.css
/public/posts/formula/ -> assets/formula-bg.jpg via formula.css
/books/seccus/         -> assets/backgrounds/seccus-bg.webp via books-seccus.css
```

Important caution:

`assets/formula.css` is used and must not be deleted.

## 11. SEO / indexing status

Known completed / working:

- `robots.txt` exists and points to sitemap;
- `sitemap.xml` exists;
- sitemap generation is automated;
- `llms.txt` exists;
- Bing accepted the site and sitemap;
- Bing live URL check for `/en/` showed indexable, JSON-LD detected, no SEO/GEO issues;
- Google Search Console shows root indexed, but some data may lag;
- Telegram Open Graph preview works with image/title/description.

Open SEO tasks:

- re-check Google after recrawl;
- re-check selected Bing URLs after deployment delay;
- add section/book-specific OG images later;
- avoid SEO filler pages.

## 12. Current books / series status

### MONOLITH

Exists as multilingual Books series with BETON and SLUDGE volume pages. GAS remains in preparation.

### You Are Already Online / Ты уже в сети

Pages exist across many languages. Ukrainian page was once marked as still open; needs verification against latest repo state.

### The Book of Whinesis / Книга Нытия / Книга Ниття

Pages exist across languages. Title rule:

- most non-Russian languages keep `The Book of Whinesis`;
- Ukrainian visible title: `Книга Ниття`;
- Russian visible title: `Книга Нытия`.

### SECCUS / АХЕПСУ

Unified URL path:

`/<lang>/books/seccus/`

Naming rule:

- RU: `САКРАЛЬНАЯ КНИГА АХЕПСУ`;
- UK: `САКРАЛЬНА КНИГА АХЕПСУ`;
- BE: `САКРАЛЬНАЯ КНІГА АХЕПСУ`;
- EN/PL/DE/ES/FR/PT: `SECCUS` in localized title.

Do not publicly explain the hidden reverse-word mechanism unless user changes this later.

### Error 404

Polish pages started:

- `/pl/books/error-404-god-not-found/`;
- `/pl/books/error-404-god-not-found/why-me/`.

Polish visible titles:

- series: `Błąd 404: Boga nie znaleziono`;
- Book I: `Dlaczego ja?`;
- Book II: `Na wszystko Jego wola`.

Rule: stable English slugs are acceptable; visible titles must be localized.

## 13. High-priority open tasks

1. Create a true `MASTER_MainSite.md` update from this sorted state.
2. Verify live pages after latest deployments, especially:
   - `/books/seccus/` in all languages;
   - `/public/talks/` in all languages;
   - `/404.html`;
   - root language links and redirect.
3. Manual repair of multilingual Public formula pages.
4. Check if `/uk/books/you-are-already-online/` is now rebuilt or still pending.
5. Run broken-link and wrong-language-link pass across the full site.
6. Check all `.seal span` occurrences and normalize to `— mark of presence` if needed.
7. Audit `assets/analytics.js` for old content-injection patches.
8. Continue professional dossier QA in all languages.
9. Prepare a one-page/PDF grant dossier based on `/professional/` if needed.
10. Add section/book-specific OG images later.
11. Asset & Style Consolidation remains medium priority, not urgent.

## 14. Development rules going forward

- Prefer clean HTML pages over temporary JS patches.
- Temporary JS overlays may be used only for drafting/review; final content must be baked into HTML.
- For large HTML updates that tool writes cannot handle, prepare complete downloadable/manual upload files.
- Do not report commit success unless the tool actually returned a commit SHA.
- For GitHub SHA conflicts, refetch current file and retry with current SHA.
- Full-file output is preferred over small “insert this somewhere” fragments.
- Avoid generic redesigns and unrelated templates.
- Keep visual canon consistent.
- Do not simplify dense public texts into motivational content.
- Russian is often master; English is the main international version; translations must preserve density and function.

## 15. Future project-wide memory proposal

Create a project-level entry file for future chats:

`Projects/Ashraellen/START_HERE.md`

It should tell any new chat to read:

1. `Projects/Ashraellen/INDEX.md`
2. `Projects/Ashraellen/MainSite/SORTED_STATE_2026-06-22.md`
3. `Projects/Ashraellen/MainSite/MASTER_MainSite.md`
4. task-specific files, depending on the work area.

For website-specific chats, also read:

- `Projects/Ashraellen/MainSite/Prompts/Request_Other_Chats_Site_Memory.md`
- `Projects/Ashraellen/MainSite/Tasks/README.md`

End-of-chat rule:

Every substantial future chat should create or update a short memory file in the relevant project folder before closing.
