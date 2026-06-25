# MainSite — CSS split for support thoughts

Date: 2026-06-25  
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

## Implementation status on 2026-06-25

Created in `Ashraellen/ashraellen`:

```text
assets/arcs.css
assets/thoughts.css
```

Cleaned from inline `<style>` and switched to `assets/arcs.css`:

```text
ru/public/thoughts/arcs/0019-do-not-bomb.html
ru/public/thoughts/arcs/0020-people-and-mass.html
ru/public/thoughts/arcs/0021-mating-games.html
ru/public/thoughts/arcs/0022-spirituality-is-not-forced.html
ru/public/thoughts/arcs/0023-price-of-transition.html
ru/public/thoughts/arcs/0024-true-enemy-not-ignorance.html
```

Cleaned from inline `<style>` and switched to `assets/thoughts.css`:

```text
ru/public/thoughts/index.html
ru/public/thoughts/index-0002.html
ru/public/thoughts/index-0001.html
```

## Important remaining work

Older individual RU thought pages `0001–0018` still need a cleanup pass.

Multilingual thought pages in EN, PL, UK, BE, PT, ES, FR and DE also need to be converted before future mass updates, or at least before their next regeneration.

Do not continue creating new pages with inline CSS. All new individual support-thought pages must use:

```html
<link rel="stylesheet" href="../../../../assets/public.css">
<link rel="stylesheet" href="../../../../assets/arcs.css">
```

All support-thought arc/index pages must use:

```html
<link rel="stylesheet" href="../../../assets/public.css">
<link rel="stylesheet" href="../../../assets/thoughts.css">
```

## Style control

Line spacing inside paragraphs on individual thought pages is now controlled in `assets/arcs.css`:

```css
.post-text,
.block p {
  line-height: 1.78;
  margin: 0 0 12px;
}
```

Arc/index page card and intro spacing is controlled in `assets/thoughts.css`.
