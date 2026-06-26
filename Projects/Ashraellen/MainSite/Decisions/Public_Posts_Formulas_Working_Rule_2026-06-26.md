# Public Posts — Formulas working rule

Date: 2026-06-26
Project: Ashraellen MainSite / Public / Posts / Formula
Status: active working rule

## Scope

This rule governs:

```text
/[lang]/public/posts/formula/
/[lang]/public/posts/formula/lines/
/[lang]/public/posts/formula/lines/line-000N.html
```

It does not govern Public Thoughts / Опорные мысли.

## Core distinction

Formulas are their own public format.

They must not be an echo, extract, summary, or repetition of Public Thoughts.

Public Thoughts and Formulas may share the wider Ashraellen field, but they are separate publication types:

```text
Public Thoughts / Опорные мысли
→ support-thought pages, arcs, images, individual pages, archive rotation

Posts / Formula
→ short formula cards, current line, completed lines archive
```

## Current structure

The current Russian implementation uses:

```text
/ru/public/posts/formula/
→ current formula line

/ru/public/posts/formula/lines/
→ index of completed formula lines

/ru/public/posts/formula/lines/line-0001.html
→ first completed formula line
```

The current formula section uses:

```text
assets/formula.css
```

## Line logic

The formula section works by lines.

A line is a compact set of short formulas united by tone, theme or inner movement.

Working model:

```text
/formula/
→ current active line

/formula/lines/
→ list of completed lines

/formula/lines/line-000N.html
→ completed line archive page
```

When a current line is completed, preserve it as the next `line-000N.html`, add it to `/lines/`, and place the next active line on `/formula/`.

## Source rule

Formula candidates may come from:

1. Telegram channel material.
2. New formulas written specifically for this format.
3. Author-approved adaptations that do not repeat Public Thoughts.

Do not automatically derive formulas from current Public Thoughts.

Do not use the formula section as a mirror of the support-thought arc currently visible on `/public/`.

## Selection rule

Before publishing a new formula line, check that candidates do not duplicate current Public Thoughts by:

```text
exact final line
central image
core theme
same rhetorical turn
same wording with shorter length
```

A formula may be philosophically adjacent to the wider Ashraellen system, but it should have its own angle and not feel like a cut-down support thought.

## Card structure

Each formula card follows the current practical structure:

```html
<article class="formula-card">
  <p class="kicker">Формула</p>
  <p class="formula-text">...</p>
  <div class="formula-tags">...</div>
</article>
```

## Current next task

The next formula task is to create a second formula line for:

```text
/ru/public/posts/formula/
```

This second line should not be based on support thoughts `0019–0024`.

Use Telegram material and/or new standalone formulas. Keep the first completed line preserved as:

```text
/ru/public/posts/formula/lines/line-0001.html
```
