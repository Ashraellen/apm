# RU Public Thoughts Migration — Working Notes

Status: updated working note before live-site implementation  
Date: 2026-06-22  
Memory repository: `Ashraellen/apm`  
Live website repository: `Ashraellen/ashraellen`  
Memory path: `Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Migration_2026-06-22.md`

## 1. Task

Prepare a controlled migration / creation track for a new Russian public-thoughts branch on the main Ashraellen website:

```text
/ru/public/thoughts/
```

The new branch is now defined more precisely as the system of:

```text
Опорные мысли
```

This is not a generic blog branch. It is a Russian public layer for larger semantic cards that previously existed as selected public formulas, but are now being separated into a clearer structural level.

## 2. Author decision

Author decision from the current task clarification:

1. Work only with the Ashraellen.com website and the repositories:

```text
Ashraellen/ashraellen
Ashraellen/apm
```

2. Create a new structure:

```text
/ru/public/thoughts/
```

3. Create the following pages as duplicates of existing old formula pages, with terminology and links updated:

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
```

4. Also create the index page:

```text
/ru/public/thoughts/index.html
```

Visible page title:

```text
Ashraellen — Опорные мысли
```

Meaning of the page:

```text
Это раздел опорных мыслей публичного поля Ashraellen. Здесь собраны большие смысловые карточки, которые раньше назывались публичными формулами, но теперь выделяются в отдельный слой.
```

5. Do not delete old pages:

```text
/ru/public/formulas/.../
```

6. Do not change this file without a separate approval:

```text
/ru/public/index.html
```

7. Do not touch:

```text
Error404
grants
other language versions
redirects
```

8. Keep memory for this task inside:

```text
Projects/Ashraellen/MainSite/
```

Do not change global:

```text
Projects/Ashraellen/MemorySystem/
```

unless separately necessary.

## 3. Old pages used as templates

The following existing live-site pages are the exact source templates for the first six new `thoughts` pages:

```text
ru/public/formulas/01-cheerfulness/index.html
ru/public/formulas/02-still-the-same/index.html
ru/public/formulas/03-let-go/index.html
ru/public/formulas/04-mortality-awakens/index.html
ru/public/formulas/05-on-your-own/index.html
ru/public/formulas/06-insight/index.html
```

Reference SHAs observed during analysis:

```text
ru/public/formulas/03-let-go/index.html                 sha: 8b0bdc396623e25148b23be49cfebf9552876deb
ru/public/formulas/04-mortality-awakens/index.html     sha: 1e5d81183aa249f19dd8f48588dbaba5d3a49fce
ru/public/formulas/05-on-your-own/index.html           sha: db4eba7edcff362d99bfea271740b3fd9531669f
ru/public/formulas/06-insight/index.html               sha: c81f2fb70946dc519f9bd10d080ca3972f833503
```

Earlier inspected references:

```text
ru/public/formulas/01-cheerfulness/index.html
ru/public/formulas/02-still-the-same/index.html
```

The pages share the same implementation pattern:

- static HTML;
- Russian language page;
- `assets/public.css`;
- inline `.formula-page` / `.formula-hero` detail-page styles;
- `script defer src="/assets/analytics.js"`;
- canonical URL;
- JSON-LD block;
- Open Graph / Twitter metadata;
- breadcrumb list;
- top navigation;
- image from `assets/public-formulas/`;
- blocks: meaning / full text / why selected / research note;
- previous / next navigation;
- seal `— mark of presence`.

## 4. New paths planned for live site

Files to create in `Ashraellen/ashraellen`:

```text
ru/public/thoughts/index.html
ru/public/thoughts/01-cheerfulness/index.html
ru/public/thoughts/02-still-the-same/index.html
ru/public/thoughts/03-let-go/index.html
ru/public/thoughts/04-mortality-awakens/index.html
ru/public/thoughts/05-on-your-own/index.html
ru/public/thoughts/06-insight/index.html
```

Live-site existence check during analysis:

```text
ru/public/thoughts/index.html                  not found before implementation
ru/public/thoughts/01-cheerfulness/index.html  not found before implementation
```

The rest of the `thoughts` branch is assumed new and should be treated as create-only, not update, unless a fresh fetch shows otherwise immediately before implementation.

## 5. Replacement rules for duplicated pages

For each duplicated detail page:

### 5.1 Terminology

Replace visible and metadata terminology:

```text
Публичная формула → Опорная мысль
```

Examples:

```text
Публичная формула 01 → Опорная мысль 01
Публичная формула Ashraellen: ... → Опорная мысль Ashraellen: ...
```

### 5.2 Paths

Replace all old formula-path references:

```text
/ru/public/formulas/.../ → /ru/public/thoughts/.../
```

This applies to:

- canonical link;
- JSON-LD `@id`;
- JSON-LD `url`;
- JSON-LD breadcrumb items;
- Open Graph URL;
- Twitter / other URL-dependent metadata if present;
- internal previous / next links;
- JavaScript navigation assignments.

### 5.3 Breadcrumbs

Replace old breadcrumb label:

```text
Formulas
```

with:

```text
Опорные мысли
```

or, if an English semantic marker is needed internally:

```text
Thoughts
```

Preferred visible Russian breadcrumb:

```text
Опорные мысли
```

### 5.4 Titles and descriptions

Keep the individual page title after the dash, but update the collection label where relevant:

Example:

```text
Ashraellen — Весёлость как диагностика человека
```

may remain as page title.

Descriptions should change from:

```text
Публичная формула Ashraellen: ...
```

to:

```text
Опорная мысль Ashraellen: ...
```

### 5.5 CSS and assets

Keep:

```text
../../../../assets/public.css
```

Keep old images for now:

```text
assets/public-formulas/01-cheerfulness.jpg
assets/public-formulas/02-still-the-same.jpg
assets/public-formulas/03-let-go.jpg
assets/public-formulas/04-mortality-awakens.jpg
assets/public-formulas/05-on-your-own.jpg
assets/public-formulas/06-insight.jpg
```

Do not create `assets/thoughts.css` during the first pass unless required.

## 6. Index page plan

Create:

```text
ru/public/thoughts/index.html
```

Page title:

```text
Ashraellen — Опорные мысли
```

Suggested H1:

```text
Опорные мысли
```

Suggested lead:

```text
Раздел опорных мыслей публичного поля Ashraellen. Здесь собраны большие смысловые карточки, которые раньше назывались публичными формулами, но теперь выделяются в отдельный слой.
```

Suggested internal explanation:

```text
Опорная мысль — это не короткая цитата и не декоративная фраза. Это смысловой узел: наблюдение, полный текст, причина выбора и исследовательская заметка. Такой формат позволяет видеть не только ударную формулировку, но и внутренний механизм, из которого она возникла.
```

Index should link to the six pages:

```text
01-cheerfulness
02-still-the-same
03-let-go
04-mortality-awakens
05-on-your-own
06-insight
```

Use existing visual canon. First pass: reuse `assets/public.css` with small inline CSS if needed.

## 7. Website files expected to be changed later

Do not change now without separate approval:

```text
ru/public/index.html
```

Possible later change, if approved:

- add a card or block linking to `/ru/public/thoughts/`;
- label: `Опорные мысли`;
- description: `Большие смысловые карточки публичного поля Ashraellen: наблюдение, полный текст, причина выбора и исследовательская заметка.`

If this file is changed later, the session log must explicitly state which block was changed and what it was changed to.

Possible later pipeline files:

```text
sitemap.xml
llms.txt
```

But existing memory says sitemap generation is automated. Do not hand-edit unless the current repository workflow requires it.

## 8. What must not be touched yet

Do not touch:

```text
Projects/Ashraellen/MemorySystem/
```

Do not touch in the live website:

```text
Error404
/404.html
/index.html
site.webmanifest
assets/analytics.js
assets/formula.css
robots.txt
monolith/
*/books/
*/research/
*/professional/
```

Do not touch other languages:

```text
en/
pl/
de/
es/
fr/
pt/
uk/
be/
```

Do not delete, rename, redirect or replace existing old pages:

```text
/ru/public/formulas/01-cheerfulness/
/ru/public/formulas/02-still-the-same/
/ru/public/formulas/03-let-go/
/ru/public/formulas/04-mortality-awakens/
/ru/public/formulas/05-on-your-own/
/ru/public/formulas/06-insight/
```

Do not make redirects without a separate explicit decision.

Do not simplify the pages into motivational / SEO filler content.

## 9. Links to verify after implementation

Manual verification list after live-site changes:

```text
https://www.ashraellen.com/ru/public/thoughts/
https://www.ashraellen.com/ru/public/thoughts/01-cheerfulness/
https://www.ashraellen.com/ru/public/thoughts/02-still-the-same/
https://www.ashraellen.com/ru/public/thoughts/03-let-go/
https://www.ashraellen.com/ru/public/thoughts/04-mortality-awakens/
https://www.ashraellen.com/ru/public/thoughts/05-on-your-own/
https://www.ashraellen.com/ru/public/thoughts/06-insight/
```

Check on each page:

- page loads;
- CSS loads;
- image loads;
- canonical points to `/ru/public/thoughts/.../`;
- OG URL points to `/ru/public/thoughts/.../`;
- JSON-LD URL / breadcrumb use `/ru/public/thoughts/.../`;
- visible terminology says `Опорная мысль`, not `Публичная формула`;
- breadcrumb label says `Опорные мысли`;
- previous / next links move inside `thoughts`, not back to `formulas`;
- `Назад` / section link goes to `/ru/public/thoughts/` or `/ru/public/` according to final implementation;
- old `/ru/public/formulas/.../` pages still exist.

## 10. Risks

1. Old pages are not all equally formatted: some are minified into one long line. Replacement must be string-safe, not line-number based.
2. Some text may include the word `формула` as part of conceptual content. Only deliberate public-label replacements should be done; avoid damaging authorial text unless the label is clearly structural.
3. Breadcrumbs currently use the English label `Formulas` in Russian pages. This should be corrected in the new branch but not necessarily in old pages yet.
4. Navigation may accidentally point back to `/ru/public/formulas/`. Must verify previous / next links.
5. The index page must not look like a thin duplicate of `/ru/public/posts/formula/`; it should explain why `Опорные мысли` are a separate layer.
6. Do not accidentally update `/ru/public/index.html` during first implementation.
7. Do not create redirects. Old pages must remain available.
8. Do not touch other language versions.
9. Do not manually edit global SEO files unless separately approved.
10. Do not report live-site changes without commit SHAs returned by GitHub.

## 11. Open questions

Mostly resolved by the latest author clarification:

- first six pages are known;
- slugs are known;
- old pages remain;
- Russian-only implementation;
- no redirect;
- no `/ru/public/index.html` change before separate approval.

Remaining open questions:

1. Should the new detail pages use `CollectionPage`, `Article`, `CreativeWork`, or another schema type in JSON-LD? Conservative first option: preserve current structure and only update URLs / descriptions.
2. Should the index link back to `/ru/public/`, `/ru/public/posts/`, or both?
3. Should visible buttons say `Назад к Публичному` or `Назад к Опорным мыслям` on detail pages? Preferred: detail pages should include `← К опорным мыслям`, with optional public link in the header.
4. Should old formula pages later receive small links to the new `thoughts` branch? Not part of first implementation.

## 12. Session-log rule for this task

After any change in the live website repository:

```text
Ashraellen/ashraellen
```

create a session log in:

```text
Projects/Ashraellen/MainSite/Session_Logs/
```

with the name pattern:

```text
MS_SL_RU_Public_Thoughts_YYYY-MM-DD.md
```

The session log must include:

- created files;
- changed files;
- commit SHA values returned by GitHub tools;
- pages to check manually;
- next step.

At the time of this update, no live-site changes have been made in `Ashraellen/ashraellen` during this session.
