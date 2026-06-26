# Session Log — RU Public Posts / Formula line 0002

Date: 2026-06-26
Project: Ashraellen MainSite / Public / Posts / Formula

## Purpose

Record the creation of the second active Russian formula line and the clarification of formula-line mechanics.

## Decisions confirmed

- Individual formulas are not numbered.
- Only formula lines are numbered: `line-0001.html`, `line-0002.html`, etc.
- Formula content remains separate from Public Thoughts.
- The rotation mechanism is similar to Public Thoughts: current visible layer, archive layer, numbered historical pages.

## APM update

Updated:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
```

Commit:

```text
d1e00d0f0f40cd8b4fc3aa9b3c824deb3d38f1c1
```

## Live site updates

Updated current active formula page:

```text
ru/public/posts/formula/index.html
```

Change:

```text
First line replaced by Second line as the current active line.
The first line remains preserved as line-0001.html.
A previous-line link was added from the active formula page to line-0001.html.
```

Commit:

```text
004602a689a923e22a48327eee01294b19f41976
```

Updated first completed formula line:

```text
ru/public/posts/formula/lines/line-0001.html
```

Change:

```text
Added line navigation forward to the current active formula line.
Fixed the breadcrumb item URL for line-0001.html.
```

Commit:

```text
dddc6dcdf931df1d0c60385814341cc4ce98a6f1
```

## CSS note

A separate CSS navigation row was attempted for `assets/formula.css`, but the write was blocked by the connector safety layer.

The implemented navigation uses the existing `.line-button` class and works functionally.

## Current formula rotation state

```text
/ru/public/posts/formula/
→ current active line: Вторая линия

/ru/public/posts/formula/lines/
→ completed formula lines index

/ru/public/posts/formula/lines/line-0001.html
→ completed first line
```
