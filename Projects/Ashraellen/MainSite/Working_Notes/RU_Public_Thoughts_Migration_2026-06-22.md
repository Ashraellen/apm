# RU Public Thoughts Migration — Working Notes

Status: working note created before live-site implementation  
Date: 2026-06-22  
Memory repository: `Ashraellen/apm`  
Live website repository: `Ashraellen/ashraellen`  
Memory path: `Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Migration_2026-06-22.md`

## 1. Task

Prepare a controlled migration / creation track for a new Russian public-thoughts branch on the main Ashraellen website:

```text
/ru/public/thoughts/
```

The task is to keep the work inside the MainSite memory layer first, then only after that touch the live website repository.

The working direction is not to destroy or overwrite the existing Public / Posts architecture, but to add a clearer Russian public-thoughts layer that can hold fuller public texts, selected observations, and expanded thought-pages without flattening them into thin formula cards.

## 2. Author decision

Author decision from the current instruction:

- read MainSite memory before implementation;
- keep task memory inside `Projects/Ashraellen/MainSite/`;
- do not change global `Projects/Ashraellen/MemorySystem/` unless separately necessary;
- create this working note before live-site changes;
- if the live website repository `Ashraellen/ashraellen` is changed, create a session log in `Projects/Ashraellen/MainSite/Session_Logs/`;
- if new `/ru/public/thoughts/` pages are created, immediately record their paths here;
- if `/ru/public/index.html` is changed, record exactly which block was changed and what it was changed to.

Working interpretation:

- `/ru/public/thoughts/` should become a separate Russian public-thoughts branch, not a chaotic dump into the existing `posts/` layer;
- existing formula / essay / fragment pages remain intact until a specific replacement or migration is approved;
- the first implementation should be conservative: static HTML pages, existing visual canon, analytics, canonical links, JSON-LD and normal navigation.

## 3. Old pages / existing site pages to use as templates

Primary live-site templates / reference pages:

```text
/ru/public/index.html
```

Use as the main Public entrance reference. Later it may receive a new card / block pointing to `/ru/public/thoughts/`.

```text
/ru/public/posts/index.html
```

Use as a structural reference for a public subsection index: header, lead, grid/list logic, seal, base script, navigation pattern.

```text
/ru/public/posts/formula/index.html
```

Use only as a reference for compact formula-list logic. Do not let the new thoughts branch become another thin formula scaffold.

```text
/ru/public/posts/essay/index.html
```

Use as a reference for fuller public-text cards and expandable / long-form logic, if needed.

```text
/ru/public/posts/fragment/index.html
```

Use as a reference for archive / fragment framing and placeholder discipline.

```text
/ru/public/formulas/01-cheerfulness/index.html
/ru/public/formulas/02-still-the-same/index.html
```

Use as detail-page references: title, meta description, canonical, public.css, inline detail-page style, hero / meaning / full text / research note / navigation / seal.

Important: existing formula pages currently live under `/ru/public/formulas/`, while older structured post pages live under `/ru/public/posts/...`. The new branch should avoid increasing this ambiguity unless we deliberately decide to normalize the whole Public structure later.

## 4. Planned new paths

Planned branch root:

```text
/ru/public/thoughts/
```

Planned files / routes, not yet created in the live site at the moment of this note:

```text
/ru/public/thoughts/index.html
```

Planned future individual pages, exact slugs still open:

```text
/ru/public/thoughts/<slug>/index.html
```

Possible first-path pattern:

```text
/ru/public/thoughts/01-<short-latin-slug>/index.html
/ru/public/thoughts/02-<short-latin-slug>/index.html
/ru/public/thoughts/03-<short-latin-slug>/index.html
```

No actual `/ru/public/thoughts/` live pages have been created yet in this session at the time this note is created.

## 5. Website files expected to be created later

In `Ashraellen/ashraellen`:

```text
ru/public/thoughts/index.html
```

Potential individual pages:

```text
ru/public/thoughts/01-<slug>/index.html
ru/public/thoughts/02-<slug>/index.html
ru/public/thoughts/03-<slug>/index.html
```

Possible CSS decision:

```text
assets/thoughts.css
```

or reuse:

```text
assets/public.css
```

Conservative first decision: reuse `assets/public.css` and, if necessary, small page-local inline CSS based on the existing formula detail pages. Create a dedicated `assets/thoughts.css` only if the branch grows enough to justify it.

## 6. Website files expected to be changed later

If the branch is implemented, likely files to change in `Ashraellen/ashraellen`:

```text
ru/public/index.html
```

Expected change: add a third public-entry card or dedicated block linking to:

```text
/ru/public/thoughts/
```

Candidate public label:

```text
Мысли
```

Candidate description:

```text
Развёрнутые публичные наблюдения, где короткая формула получает дыхание, контекст и смысловое давление.
```

The exact final wording should be approved / refined during implementation.

Potential later changes:

```text
sitemap.xml
llms.txt
```

However, the current memory says sitemap generation is automatic. Prefer running / relying on the existing sitemap workflow rather than hand-editing `sitemap.xml`, unless the repository workflow requires manual update.

Potential later language expansion:

```text
/en/public/thoughts/
/pl/public/thoughts/
...
```

Not part of the first Russian migration unless explicitly approved.

## 7. What must not be touched yet

Do not touch without separate reason / approval:

```text
Projects/Ashraellen/MemorySystem/
```

Do not alter global memory for this task. Keep notes inside:

```text
Projects/Ashraellen/MainSite/
```

Do not touch yet in the live website:

```text
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

Do not rewrite all language versions automatically. This task is Russian-first.

Do not delete or rename existing Public branches:

```text
/ru/public/posts/
/ru/public/posts/formula/
/ru/public/posts/essay/
/ru/public/posts/fragment/
/ru/public/posts/sources/
/ru/public/formulas/
```

Do not turn the new branch into motivational content, generic blog posts, SEO filler, or short decorative cards. The public-thoughts layer should preserve authorial density and the Ashraellen research framing.

## 8. Open questions

1. What exact old pages / old posts / old texts are being migrated into `/ru/public/thoughts/` first?
2. Should `/ru/public/thoughts/` contain only expanded public observations, or also selected formulas with full commentary?
3. Should individual pages use numbered slugs (`01-...`) or clean thematic slugs without numbers?
4. Should the branch be visually closer to `/ru/public/formulas/<id>/` detail pages or to `/ru/public/posts/essay/` cards?
5. Should `/ru/public/index.html` receive a third card beside `Выступления` and `Публикации`, or a separate block below the existing two-card grid?
6. Should the existing `/ru/public/formulas/` ambiguity be preserved for now, or later normalized under `/ru/public/thoughts/` / `/ru/public/posts/`?
7. Should images be required for each thought page, or should the first migration be text-first?
8. Should the first implementation include JSON-LD as `Article` / `CreativeWork` for individual thought pages rather than only `CollectionPage`?
9. Should English / Polish versions be planned immediately after the Russian version, or postponed until the Russian structure stabilizes?
10. Should old formula pages link forward to the new thoughts branch after migration, or remain isolated as selected public formulas?

## 9. Session-log rule for this task

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

At the time this note is created, no live-site changes have been made in `Ashraellen/ashraellen` during this session.
