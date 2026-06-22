# MS_SL_RU_Public_Thoughts_Arcs_2026-06-22

Status: completed architecture correction and arcs creation  
Date: 2026-06-22  
Memory repository: `Ashraellen/apm`  
Live website repository: `Ashraellen/ashraellen`

## 1. Final architecture decision

The branch:

```text
/ru/public/thoughts/
```

is the correct final system for large public support-thoughts.

The branch:

```text
/ru/public/posts/formula/
```

remains the separate system for short formulas.

The branch:

```text
/ru/public/posts/formula/lines/
```

remains the separate system for completed short-formula lines.

The branch:

```text
/ru/public/formulas/
```

is the old layer from which the first six pages are migrated into `/thoughts/`. It must not be developed as the new architecture.

Semantic arcs must live inside:

```text
/ru/public/thoughts/arcs/
```

The branch:

```text
/ru/public/formulas/arcs/
```

is not the final architecture.

## 2. What was created in `Ashraellen/ashraellen`

Created:

```text
ru/public/thoughts/arcs/index.html
ru/public/thoughts/arcs/arc-0001.html
```

`ru/public/thoughts/arcs/index.html`:

- title: `Ashraellen — Смысловые дуги`;
- H1: `Смысловые дуги`;
- meaning: list of completed semantic selections in the Ashraellen public field;
- first card: `Первая дуга`;
- card text: `Весёлость, старые силы, пробуждение, конечность, страх и прозрение.`;
- card link: `/ru/public/thoughts/arcs/arc-0001.html`.

`ru/public/thoughts/arcs/arc-0001.html`:

- title: `Ashraellen — Первая дуга`;
- H1: `Первая дуга`;
- description: `Первая завершённая смысловая дуга публичного поля Ashraellen: шесть опорных мыслей о человеке, страхе, пробуждении, конечности, власти и внутреннем взгляде.`;
- six cards link to:

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
```

## 3. Erroneous branches / files checked

Checked and not found before creation:

```text
ru/public/formulas/arcs/index.html
ru/public/formulas/arcs/arc-0001.html
```

Therefore no erroneous `/ru/public/formulas/arcs/` files were created in this correction pass.

Checked and not found before creation:

```text
ru/public/thoughts/arcs/index.html
ru/public/thoughts/arcs/arc-0001.html
```

They were then created in the correct location.

## 4. What was not touched

Not changed:

```text
ru/public/index.html
ru/public/posts/formula/
ru/public/posts/formula/lines/
ru/public/formulas/01-cheerfulness/index.html
ru/public/formulas/02-still-the-same/index.html
ru/public/formulas/03-let-go/index.html
ru/public/formulas/04-mortality-awakens/index.html
ru/public/formulas/05-on-your-own/index.html
ru/public/formulas/06-insight/index.html
```

No redirects were created.

No other language versions were touched.

Error404, grants, books, research, professional pages, root files, analytics, robots and manifest were not touched.

## 5. Commit SHA values

Live-site commits returned by GitHub tools:

```text
c3867b4a52611b692fe1ccda1795a34c77a10cf5  create ru/public/thoughts/arcs/index.html
b600a6f13a17d97aef794da37650d74fc13741c0  create ru/public/thoughts/arcs/arc-0001.html
```

Memory commits returned by GitHub tools:

```text
a6bc56fbcb846f84beb7eceac11090b422ca164b  update Working_Notes with Architecture correction — final
```

## 6. Pages to check manually

Check after GitHub Pages deployment:

```text
https://www.ashraellen.com/ru/public/thoughts/arcs/
https://www.ashraellen.com/ru/public/thoughts/arcs/arc-0001.html
```

Also verify links from `arc-0001.html`:

```text
https://www.ashraellen.com/ru/public/thoughts/01-cheerfulness/
https://www.ashraellen.com/ru/public/thoughts/02-still-the-same/
https://www.ashraellen.com/ru/public/thoughts/03-let-go/
https://www.ashraellen.com/ru/public/thoughts/04-mortality-awakens/
https://www.ashraellen.com/ru/public/thoughts/05-on-your-own/
https://www.ashraellen.com/ru/public/thoughts/06-insight/
```

## 7. Next safe step

1. Wait for GitHub Pages deployment.
2. Open `/ru/public/thoughts/arcs/` and `/ru/public/thoughts/arcs/arc-0001.html` manually.
3. Check that all six cards in `arc-0001.html` lead to `/ru/public/thoughts/.../`, not `/ru/public/formulas/.../`.
4. Only after manual verification decide whether to update `/ru/public/index.html` and how to route the current public showcase to `/ru/public/thoughts/` and/or `/ru/public/thoughts/arcs/`.
5. Do not delete old `/ru/public/formulas/.../` pages or add redirects without separate author confirmation.
