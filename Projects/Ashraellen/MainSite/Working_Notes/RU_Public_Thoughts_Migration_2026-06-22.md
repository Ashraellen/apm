# RU Public Thoughts Migration — Working Notes

Status: architecture corrected — final decision recorded  
Date: 2026-06-22  
Memory repository: `Ashraellen/apm`  
Live website repository: `Ashraellen/ashraellen`  
Memory path: `Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Migration_2026-06-22.md`

## 1. Task

Prepare and maintain the Russian public system of large public support-thoughts for Ashraellen.com.

The correct new system is:

```text
/ru/public/thoughts/
```

This branch holds large public support-thoughts, migrated from the older formula layer.

## 2. Architecture correction — final

Final author decision:

```text
/ru/public/thoughts/
```

is the correct final system for large public support-thoughts.

```text
/ru/public/posts/formula/
```

remains a separate system for short formulas.

```text
/ru/public/posts/formula/lines/
```

remains a separate system for completed lines of short formulas.

```text
/ru/public/formulas/
```

is the old layer from which the first six older pages are being migrated into `/thoughts/`. Do not develop `/ru/public/formulas/` as the new architecture.

Semantic arcs must live inside:

```text
/ru/public/thoughts/arcs/
```

The branch:

```text
/ru/public/formulas/arcs/
```

is not the final architecture and must not be created or developed. If it ever appears, treat it as an erroneous temporary branch and do not delete it without author confirmation.

## 3. Correct final structure

```text
/ru/public/
```

Current public showcase: `Опорные мысли`. Do not change without separate approval.

```text
/ru/public/thoughts/
```

Section of large public support-thoughts.

```text
/ru/public/thoughts/01-cheerfulness/
/ru/public/thoughts/02-still-the-same/
/ru/public/thoughts/03-let-go/
/ru/public/thoughts/04-mortality-awakens/
/ru/public/thoughts/05-on-your-own/
/ru/public/thoughts/06-insight/
```

The old six pages migrated into the new system as support-thoughts.

```text
/ru/public/thoughts/arcs/
```

List of completed semantic arcs.

```text
/ru/public/thoughts/arcs/arc-0001.html
```

The old six pages as `Первая дуга`.

```text
/ru/public/posts/formula/
/ru/public/posts/formula/lines/
```

Separate branch for short formulas and completed short-formula lines. Do not touch in this task.

## 4. Existing old layer to preserve for now

Do not delete or redirect without separate author approval:

```text
/ru/public/formulas/01-cheerfulness/
/ru/public/formulas/02-still-the-same/
/ru/public/formulas/03-let-go/
/ru/public/formulas/04-mortality-awakens/
/ru/public/formulas/05-on-your-own/
/ru/public/formulas/06-insight/
```

These are old pages. They may remain available while the new `/thoughts/` system stabilizes.

## 5. Files already created in the correct new system

Created earlier in `Ashraellen/ashraellen`:

```text
ru/public/thoughts/index.html
ru/public/thoughts/01-cheerfulness/index.html
ru/public/thoughts/02-still-the-same/index.html
ru/public/thoughts/03-let-go/index.html
ru/public/thoughts/04-mortality-awakens/index.html
ru/public/thoughts/05-on-your-own/index.html
ru/public/thoughts/06-insight/index.html
```

These are now considered correct, not erroneous.

## 6. Semantic arcs created in the correct location

Created in `Ashraellen/ashraellen`:

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
- six cards linking to the new `/ru/public/thoughts/.../` pages.

## 7. What must not be touched in this task

Do not change without separate confirmation:

```text
/ru/public/index.html
/ru/public/posts/formula/
/ru/public/posts/formula/lines/
/ru/public/formulas/.../
/ru/public/formulas/arcs/
```

Do not touch:

```text
other language versions
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

## 8. Manual verification links

Check after GitHub Pages deployment:

```text
https://www.ashraellen.com/ru/public/thoughts/
https://www.ashraellen.com/ru/public/thoughts/arcs/
https://www.ashraellen.com/ru/public/thoughts/arcs/arc-0001.html
https://www.ashraellen.com/ru/public/thoughts/01-cheerfulness/
https://www.ashraellen.com/ru/public/thoughts/02-still-the-same/
https://www.ashraellen.com/ru/public/thoughts/03-let-go/
https://www.ashraellen.com/ru/public/thoughts/04-mortality-awakens/
https://www.ashraellen.com/ru/public/thoughts/05-on-your-own/
https://www.ashraellen.com/ru/public/thoughts/06-insight/
```

## 9. Notes

The current `/ru/public/thoughts/` branch is correct.

The previously proposed `/ru/public/formulas/arcs/` branch is rejected as final architecture and has not been created during the correction pass.

`/ru/public/index.html` still needs a separate author-approved update later if the public showcase should visibly route users into `/ru/public/thoughts/` and/or `/ru/public/thoughts/arcs/`.

## 10. Session-log rule

After any change in `Ashraellen/ashraellen`, create a session log inside:

```text
Projects/Ashraellen/MainSite/Session_Logs/
```

For the arcs correction, use:

```text
MS_SL_RU_Public_Thoughts_Arcs_2026-06-22.md
```
