# MainSite — page type stylesheet rule

Date: 2026-06-25
Project: Ashraellen.com / MainSite
Status: active site-wide technical rule

## Decision

Ashraellen.com should grow by page families, not by one-off page styling.

When a new section or a new page type is created, it should receive its own shared stylesheet in the assets directory.

The base site stylesheet remains the common foundation. A page-type stylesheet adds only the rules needed by that page family.

## Working model

Base foundation:

- assets/public.css

Existing page-family stylesheets:

- assets/research.css for Research pages
- assets/arcs.css for individual Support Thought pages
- assets/thoughts.css for Support Thought arc and index pages

Future examples may include separate files for Books, Grants, Archive, Projects, Contacts or any other distinct page family.

## Rule for new work

Before creating a new page, decide whether it belongs to an existing page type or starts a new page type.

If it belongs to an existing type, use the existing shared stylesheet.

If it starts a new type, create a new shared stylesheet for that type and use it consistently across all language versions of that page family.

Do not use old legacy pages as styling templates if they contain page-local styling from earlier stages of the site.

Working legacy pages may remain unchanged while they work.

## Principle

One page type means one shared stylesheet.

Visual changes should be made in the shared stylesheet for the relevant page type, not repeated separately on each new page.
