# RU Public Thoughts — Rotating Architecture

Status: final author decision recorded  
Date: 2026-06-23  
Project: Ashraellen MainSite  
Memory repository: `Ashraellen/apm`  
Live website repository: `Ashraellen/ashraellen`  
Memory path: `Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md`

## 1. Purpose

This file records the final architecture decision for the Russian public support-thoughts system on Ashraellen.com.

The system is not a generic blog and not a simple archive. It is a moving structure:

- `/ru/public/` is the live public showcase for the newest set of six support-thoughts;
- `/ru/public/thoughts/index.html` is the most recent completed arc that has moved away from the live showcase;
- `/ru/public/thoughts/index-0001.html`, `index-0002.html`, etc. are older completed arc pages;
- `/ru/public/thoughts/arcs/` stores the individual expanded support-thought pages.

## 2. Core terms

Use the full wording on content pages:

```text
Опорные мысли
Опорная мысль 0001
Первая дуга опорных мыслей
Вторая дуга опорных мыслей
```

Shorter wording is allowed and preferred in compact navigation and buttons:

```text
Открыть мысль →
К мыслям
Следующая мысль →
Предыдущая мысль ←
Читать дуги мыслей →
```

Do not use `формула` in the new visible support-thought layer, except when explicitly referring to the old historical layer.

## 3. Numbering system

All individual support-thoughts use four-digit numbers:

```text
0001
0002
0003
...
0012
...
0100
```

This leaves enough room for long-term growth and keeps file sorting stable.

The first six old public formulas become:

```text
Опорная мысль 0001 — Весёлость как диагностика человека
Опорная мысль 0002 — Те же силы, новые имена
Опорная мысль 0003 — Пробуждение начинается с невозможности продолжать
Опорная мысль 0004 — Конечность пробуждает вопрос
Опорная мысль 0005 — Страх как механизм контроля
Опорная мысль 0006 — Глубокий взгляд собирает жизнь
```

## 4. Live showcase: `/ru/public/`

`/ru/public/` is the living public showcase.

It always shows the newest current set of six support-thoughts.

Current intended next live showcase:

```text
0007–0012
```

The live showcase should not be treated as a permanent archive of all older support-thoughts.

Under the six live cards, add a button:

```text
Читать дуги мыслей →
```

This button points to:

```text
/ru/public/thoughts/
```

## 5. Completed arcs in `/ru/public/thoughts/`

`/ru/public/thoughts/index.html` is not a permanent first-arc page.

It is the newest completed arc that has moved out of `/ru/public/`.

When a newer six-thought set appears on `/ru/public/`, the previous live set moves into:

```text
/ru/public/thoughts/index.html
```

The previous `index.html` then receives the next free archival filename:

```text
/ru/public/thoughts/index-0001.html
/ru/public/thoughts/index-0002.html
/ru/public/thoughts/index-0003.html
```

Important rule:

```text
index-0001.html is the oldest numbered completed arc page.
```

Newer numbered archive pages receive the next free number. Do not overwrite old numbered pages.

## 6. Example of rotation

### Stage A — current intended state

```text
/ru/public/
→ live showcase: 0007–0012

/ru/public/thoughts/index.html
→ newest completed arc: 0001–0006
```

### Stage B — when 0013–0018 becomes live

```text
/ru/public/
→ live showcase: 0013–0018

/ru/public/thoughts/index.html
→ newest completed arc: 0007–0012

/ru/public/thoughts/index-0001.html
→ older completed arc: 0001–0006
```

### Stage C — when 0019–0024 becomes live

```text
/ru/public/
→ live showcase: 0019–0024

/ru/public/thoughts/index.html
→ newest completed arc: 0013–0018

/ru/public/thoughts/index-0002.html
→ older completed arc: 0007–0012

/ru/public/thoughts/index-0001.html
→ oldest completed arc: 0001–0006
```

The numbered `index-000N.html` pages therefore move from older to newer by number, while `index.html` is always the newest completed arc.

## 7. Individual support-thought pages

Individual expanded support-thought pages live in:

```text
/ru/public/thoughts/arcs/
```

Use filenames like:

```text
/ru/public/thoughts/arcs/0001-cheerfulness.html
/ru/public/thoughts/arcs/0002-still-the-same.html
/ru/public/thoughts/arcs/0003-let-go.html
/ru/public/thoughts/arcs/0004-mortality-awakens.html
/ru/public/thoughts/arcs/0005-on-your-own.html
/ru/public/thoughts/arcs/0006-insight.html
```

Do not use filenames like `arc-0001.html` for individual support-thought pages, because `arc-0001` reads as an arc, not as an individual thought.

The old temporary file:

```text
/ru/public/thoughts/arcs/arc-0001.html
```

should be treated as a temporary/intermediate file and not developed as the final pattern.

## 8. Arc page display convention

On an arc page, visible structure should be human-readable, not overly technical.

Preferred display pattern:

```text
Опорные мысли

ДУГА 0001

Первая дуга опорных мыслей

Весёлость, старые силы, пробуждение, конечность, страх и прозрение.
```

Do not add a separate visible line like:

```text
Опорные мысли 0001–0006
```

This was considered too technical and redundant for the visible page.

The range may be present in metadata, internal notes, hidden comments, or card labels, but not as a central visible headline.

## 9. Card display convention

Cards inside an arc page use full terminology:

```text
Опорная мысль 0001
Весёлость как диагностика человека
```

The button uses short terminology:

```text
Открыть мысль →
```

## 10. Navigation convention

On `/ru/public/`:

```text
Читать дуги мыслей → /ru/public/thoughts/
```

On `/ru/public/thoughts/index.html`:

- link back to `/ru/public/` with short wording such as `К новым мыслям` or `К живой витрине`;
- when older numbered arc pages exist, link to the older arc page.

On numbered arc pages:

- link to newer arc if it exists;
- link to older arc if it exists;
- keep labels simple: `Новее`, `Старее`, `К мыслям`, `К новым мыслям`.

On individual support-thought pages:

- link back to the relevant arc page;
- link to previous support-thought if it exists;
- link to next support-thought if it exists;
- use short navigation labels: `К дуге`, `Предыдущая мысль`, `Следующая мысль`.

## 11. Language rollout rule

Initial implementation is Russian-first.

The support-thought architecture, page structure, navigation logic, card layout, metadata pattern, and completed-arc rotation should be built and stabilized first in Russian:

```text
/ru/public/
/ru/public/thoughts/
/ru/public/thoughts/arcs/
```

Only after the Russian version is stable and approved should the same structural changes be replicated to other language versions by analogy.

This means:

- do not redesign the other languages independently;
- do not start multilingual replication before the Russian layer is stable;
- when replication begins, preserve the same architecture and adapt only language, metadata, links, and local text naturally;
- use the Russian implementation as the master structural pattern.

## 12. Text integrity rule

The full text of each support-thought must not be changed, shortened, compressed, paraphrased, polished, or silently corrected.

When the author provides the section equivalent to:

```text
Полный текст
```

that text is sacred as supplied. It must be inserted exactly as given unless the author explicitly asks for editing.

Allowed work around the supplied full text:

- create or adapt the title if needed;
- write `Смысл`;
- write `Почему выбрано`;
- write `Исследовательская заметка`;
- prepare metadata, descriptions, cards, navigation, and page scaffolding;
- format the page without changing the supplied wording.

Forbidden without explicit author approval:

- shortening the full text;
- rewriting the full text;
- smoothing the full text;
- changing rhythm or paragraph structure;
- replacing words for style;
- removing repetitions;
- merging paragraphs;
- adding explanations inside the full text.

## 13. Editorial completion rule for new support-thoughts

For future/new support-thoughts, the author may provide only the main support-thought body, i.e. the future `Полный текст` section.

In that case, the assistant must complete the surrounding analytical structure by analogy with the old formula page pattern, especially:

```text
Смысл
Полный текст
Почему выбрано
Исследовательская заметка
```

Reference pattern:

```text
https://www.ashraellen.com/ru/public/formulas/01-cheerfulness/
```

The assistant's task is to create the surrounding interpretive frame while preserving the author's supplied `Полный текст` exactly.

The added blocks must serve the thought, not dominate it:

- `Смысл` explains the inner movement and central axis of the thought;
- `Почему выбрано` explains why this thought deserves to become an опорная мысль;
- `Исследовательская заметка` frames the thought within Ashraellen's literary-philosophical / artistic research practice;
- none of these blocks may turn the text into motivation, coaching, therapy, sermonizing, SEO filler, or a simplified lesson.

## 14. Existing old and temporary layers

Old historical layer:

```text
/ru/public/formulas/01-cheerfulness/
/ru/public/formulas/02-still-the-same/
/ru/public/formulas/03-let-go/
/ru/public/formulas/04-mortality-awakens/
/ru/public/formulas/05-on-your-own/
/ru/public/formulas/06-insight/
```

Do not delete or redirect without a separate author decision.

Temporary intermediate layer already created earlier:

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
/ru/public/thoughts/arcs/arc-0001.html
```

Do not delete immediately. First create the correct new pages, update navigation, verify deployment, and only then decide whether to delete or redirect the temporary intermediate pages.

## 15. Immediate implementation plan

Next safe implementation sequence:

1. Create correct individual pages:

```text
/ru/public/thoughts/arcs/0001-cheerfulness.html
/ru/public/thoughts/arcs/0002-still-the-same.html
/ru/public/thoughts/arcs/0003-let-go.html
/ru/public/thoughts/arcs/0004-mortality-awakens.html
/ru/public/thoughts/arcs/0005-on-your-own.html
/ru/public/thoughts/arcs/0006-insight.html
```

2. Rebuild `/ru/public/thoughts/index.html` as the newest completed arc page for 0001–0006, using the final visible terminology.

3. Do not create `index-0001.html` yet, because there is not yet a newer completed arc to force 0001–0006 out of `index.html`.

4. Later, prepare `/ru/public/` as live showcase for 0007–0012.

5. Add `Читать дуги мыслей →` on `/ru/public/`, pointing to `/ru/public/thoughts/`.

6. After verification, decide what to do with the temporary intermediate URLs.

7. Only after the Russian layer is stable and approved, replicate the structure to other language versions by analogy.

## 16. Restrictions

Do not touch without separate author approval:

```text
other language versions before Russian approval
/ru/public/posts/formula/
/ru/public/posts/formula/lines/
redirects
Error404
grants
books
research
professional pages
analytics
robots.txt
site.webmanifest
```

This architecture applies first to the Russian public support-thoughts layer. Multilingual rollout should happen later by analogy after the Russian implementation is stable.
