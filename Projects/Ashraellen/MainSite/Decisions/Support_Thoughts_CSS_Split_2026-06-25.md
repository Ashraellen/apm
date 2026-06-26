# MainSite — CSS split for support thoughts

Date: 2026-06-25  
Updated: 2026-06-26  
Project: Ashraellen.com / MainSite / Public Thoughts  
Status: active technical rule

## Decision

Support-thought pages use two separate CSS files by page type:

```text
assets/arcs.css
→ individual support thought pages inside /public/thoughts/arcs/
→ examples: 0019-do-not-bomb.html, 0024-true-enemy-not-ignorance.html

assets/thoughts.css
→ support-thought arc/index pages
→ examples: /ru/public/thoughts/, index-0001.html, index-0002.html
```

The naming follows the existing site path logic:

- individual thought files live in the `arcs/` directory, therefore they use `arcs.css`;
- arc overview pages are the `thoughts` index layer, therefore they use `thoughts.css`.

## Current working rule

New Public Thoughts pages and any regenerated Public Thoughts pages use the current shared CSS split.

Working legacy pages may remain unchanged while they work. Cleanup is driven by active regeneration, repair, rotation, or a concrete visual/technical need.

The project does not clean old pages only for the sake of cleanup.

## Current CSS files

Current files in `Ashraellen/ashraellen`:

```text
assets/arcs.css
assets/thoughts.css
```

Individual support-thought pages use:

```html
<link rel="stylesheet" href="../../../../assets/public.css">
<link rel="stylesheet" href="../../../../assets/arcs.css">
```

Support-thought arc/index pages use:

```html
<link rel="stylesheet" href="../../../assets/public.css">
<link rel="stylesheet" href="../../../assets/thoughts.css">
```

## Implementation status on 2026-06-25

Created in `Ashraellen/ashraellen`:

```text
assets/arcs.css
assets/thoughts.css
```

Cleaned from inline `<style>` and switched to `assets/arcs.css` during the original split pass:

```text
ru/public/thoughts/arcs/0019-do-not-bomb.html
ru/public/thoughts/arcs/0020-people-and-mass.html
ru/public/thoughts/arcs/0021-mating-games.html
ru/public/thoughts/arcs/0022-spirituality-is-not-forced.html
ru/public/thoughts/arcs/0023-price-of-transition.html
ru/public/thoughts/arcs/0024-true-enemy-not-ignorance.html
```

Cleaned from inline `<style>` and switched to `assets/thoughts.css` during the original split pass:

```text
ru/public/thoughts/index.html
ru/public/thoughts/index-0002.html
ru/public/thoughts/index-0001.html
```

Later multilingual alignment work may extend the same structure to other languages. The current working reference for Public Thoughts is:

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md
```

## Style control

Paragraph spacing on individual thought pages is controlled in `assets/arcs.css`:

```css
.post-text,
.block p {
  line-height: 1.35;
  margin: 0 0 10px;
}
```

Card and intro paragraph spacing on arc/index pages is controlled in `assets/thoughts.css`:

```css
.thought-card p,
.intro-block p {
  line-height: 1.35;
  margin: 0 0 10px;
}
```

## Relation to the site-wide CSS rule

The site-wide stylesheet rule remains:

```text
New section or new page type → shared page-type CSS file.
```

Reference:

```text
Projects/Ashraellen/MainSite/Decisions/Site_Page_Type_Stylesheet_Rule_2026-06-25.md
```
