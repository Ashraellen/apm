# Ashraellen Website — Technical Memory

Last updated: 2026-06-12

## Purpose

This file records the current technical state of the Ashraellen website and the SEO / AI-readiness work completed on 2026-06-12, so future chats, Codex sessions and contributors can continue from the same point without rediscovering the site structure.

## Main website repository

```text
Ashraellen/ashraellen
```

Live site:

```text
https://www.ashraellen.com/
```

The site is a static multilingual GitHub Pages site.

## Language roots

The current language roots are:

```text
/
/en/
/ru/
/pl/
/de/
/es/
/fr/
/pt/
/uk/
/be/
```

The main language sections are repeated across language roots:

```text
books
public
research
professional
monolith
```

## Strategic framing of the site

The site must present Ashraellen as:

```text
an independent multilingual literary-philosophical and artistic research practice
```

It must not primarily frame the project as:

```text
blog
YouTube project
spiritual teaching
therapy
motivational platform
infobusiness
self-help platform
request for personal rescue
```

Preferred public author name:

```text
Ashraellen
```

Formal / legal name when needed:

```text
Nikolai Kostyshev
```

Do not use `Ashraellen Live` as the current public author name unless quoting a specific legacy publication record.

## Work completed on 2026-06-12

### 1. AI-readiness / SEO audit interpretation

A RankCaster / AI-readiness audit was reviewed.

Key initial audit signals:

```text
Overall: healthy, but with technical gaps.
Strong GEO / AI-readiness direction.
Critical issues included missing H1, missing JSON-LD on homepage and thin machine-readable structure.
Medium issues included low visible content volume and missing llms.txt.
Low issues included canonical / landmark refinements.
```

The work focused on making the site readable to search engines, Bing, Google, and AI crawlers while preserving the visual minimalism of the site.

### 2. Google Search Console / Bing Webmaster Tools

Google Search Console status seen during the session:

```text
The main page was already indexed by Google.
The last crawl shown in GSC was from before the current technical updates.
Google selected the inspected URL as canonical, but user-declared canonical was not yet reflected because Google had not recrawled after the updates.
A sitemap processing warning was visible, but it appeared to be stale / temporary rather than a site-breaking issue.
```

Bing Webmaster Tools actions completed:

```text
Site accepted in Bing Webmaster Tools.
Sitemap submitted:
https://www.ashraellen.com/sitemap.xml

Priority URLs submitted manually, including:
/
/en/
/ru/
/pl/
/en/research/
/ru/research/
/pl/research/
/en/professional/
/ru/professional/
/pl/professional/
/en/books/
/ru/books/
/pl/books/
/en/public/
/ru/public/
/pl/public/
/en/books/monolith/
/ru/books/monolith/
/en/books/monolith/beton/
/ru/books/monolith/beton/
/en/books/monolith/sludge/
/ru/books/monolith/sludge/
/llms.txt
/sitemap.xml
```

Bing Live URL inspection after the first fixes showed:

```text
URL can be indexed by Bing.
No SEO / GEO issues found for checked English entry page.
JSON-LD detected.
```

A later Bing check on Polish entry showed a stale/missing H1 issue, which led to fixing H1 across all language roots.

### 3. H1 and visible project summaries

All language entry pages now use:

```html
<h1 class="brand">Ashraellen</h1>
```

instead of a non-semantic brand div / paragraph where applicable.

Visible project summary paragraphs were added to language entry pages so the site has a readable semantic description, not only visual navigation.

The English homepage summary frames Ashraellen as:

```text
an independent multilingual literary-philosophical and artistic research practice exploring consciousness, language, systems, satire, digital pressure, inner autonomy and the loss of direct perception through books, public texts, videos, sound and visual forms.
```

The Russian homepage summary frames Ashraellen as:

```text
независимая многоязычная литературно-философская и художественно-исследовательская практика: книги, исследования, публичные тексты, видео, звук, визуальные формы и наблюдение за тем, как человек теряет и возвращает контакт со смыслом.
```

Other language roots received compact matching summaries.

### 4. Canonical links

Canonical links were added / automated across HTML pages.

Automation file:

```text
scripts/apply-canonical.js
```

Rules:

```text
root index.html -> https://www.ashraellen.com/
xx/path/index.html -> https://www.ashraellen.com/xx/path/
other .html files -> corresponding full URL
404.html is skipped
```

The canonical generator also protects language entry H1s.

### 5. Static link hygiene

A control pass found old `href="#"` and `src="#"` remnants on a miniified book page, especially English BETON.

Instead of manually fixing one page, a systematic static-link hygiene generator was added.

Automation file:

```text
scripts/apply-static-links.js
```

Purpose:

```text
Replace known old placeholder links/images with real static URLs in HTML.
Prevent JavaScript-only navigation placeholders from returning.
Keep important navigation visible in the raw HTML before browser JavaScript runs.
```

Important principle:

```text
Meaningful site structure must exist in static HTML.
Do not rely on client-side JavaScript to create core navigation, canonical signals, structured data or Open Graph metadata.
```

### 6. JSON-LD structured data

A static JSON-LD generator was added.

Automation file:

```text
scripts/apply-jsonld.js
```

It generates JSON-LD directly into HTML files.

Coverage:

```text
root homepage
language roots
key pages under language folders
research
professional
books
public
monolith
book pages such as BETON and SLUDGE
```

JSON-LD entities used:

```text
Person
WebSite
WebPage
CollectionPage
ProfilePage
BreadcrumbList
Book
BookSeries
```

Core entity:

```json
{
  "@type": "Person",
  "@id": "https://www.ashraellen.com/#person",
  "name": "Ashraellen",
  "alternateName": "Nikolai Kostyshev",
  "url": "https://www.ashraellen.com/"
}
```

Important rule:

```text
The author is one entity.
Pages are different language and section manifestations of the same project.
```

Book pages now receive `Book` structured data where applicable, with `author` pointing to `https://www.ashraellen.com/#person`.

### 7. Sitemap and robots.txt

The site has:

```text
robots.txt
sitemap.xml
```

robots.txt:

```text
User-agent: *
Allow: /

Sitemap: https://www.ashraellen.com/sitemap.xml
```

Sitemap generation is automated.

Automation file:

```text
scripts/generate-sitemap.js
```

### 8. llms.txt

A public `llms.txt` file was created and expanded.

Purpose:

```text
Give AI crawlers and future AI systems a compact, preferred description of the project.
Clarify correct framing.
List key English, Russian and other language entry points.
Clarify public author name.
```

Current preferred framing in `llms.txt`:

```text
Ashraellen is an independent multilingual literary-philosophical and artistic research practice exploring consciousness, language, systems, satire, digital culture, inner autonomy, meaning, interpretation and direct perception.
```

The file explicitly says not to describe Ashraellen primarily as:

```text
blog
coaching
therapy
motivation
self-help
religious instruction
commercial personal-development content
```

### 9. IndexNow automation

IndexNow support was added.

Key file in website root:

```text
b2cda9f3e8714a6db926f48c7251ea65.txt
```

Script:

```text
scripts/submit-indexnow.js
```

Workflow behavior:

```text
Read URLs from sitemap.xml.
Submit them by POST to api.indexnow.org.
Use host, key, keyLocation and urlList.
Do not break deploy if IndexNow is temporarily unavailable.
```

The script accepts HTTP 200 / 202 as successful submission and treats network errors / timeouts as warnings only.

### 10. Open Graph / Twitter Cards

Open Graph support was added.

Default OG image created and uploaded by the user:

```text
assets/og/ashraellen-og-home-default-1200x630.jpg
```

Dimensions:

```text
1200 x 630
```

The image is based on the dark Ashraellen visual with textured formal clothing, tie and the hand-with-eye symbol.

Open Graph generator:

```text
scripts/apply-og.js
```

Initial version covered root and language entry pages.

It was then expanded to cover all HTML pages inside language folders:

```text
/en/...
/ru/...
/pl/...
/de/...
/es/...
/fr/...
/pt/...
/uk/...
/be/...
```

Current Open Graph tags inserted include:

```html
<meta property="og:type" content="website">
<meta property="og:site_name" content="Ashraellen">
<meta property="og:title" content="...">
<meta property="og:description" content="...">
<meta property="og:url" content="...">
<meta property="og:image" content="https://www.ashraellen.com/assets/og/ashraellen-og-home-default-1200x630.jpg">
<meta property="og:image:secure_url" content="https://www.ashraellen.com/assets/og/ashraellen-og-home-default-1200x630.jpg">
<meta property="og:image:type" content="image/jpeg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:image:alt" content="Ashraellen — dark formal image with the hand and eye symbol">
<meta property="og:locale" content="...">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="...">
<meta name="twitter:description" content="...">
<meta name="twitter:image" content="https://www.ashraellen.com/assets/og/ashraellen-og-home-default-1200x630.jpg">
<meta name="twitter:image:alt" content="Ashraellen — dark formal image with the hand and eye symbol">
```

For pages under `/books/`, the generator sets:

```html
<meta property="og:type" content="book">
```

For other pages, it uses:

```html
<meta property="og:type" content="website">
```

The Open Graph preview was tested by sending the root URL in Telegram. The preview displayed correctly with title, description and image.

### 11. PWA / app icons

The site can be installed as an app and already uses specially prepared app icons.

Important distinction:

```text
PWA / app icons must remain separate from Open Graph images.
Open Graph images live under assets/og/.
Do not reuse small app icons directly as OG images.
```

Current OG folder:

```text
assets/og/
```

Current default OG image:

```text
assets/og/ashraellen-og-home-default-1200x630.jpg
```

Future OG images should follow the same folder convention.

## Current GitHub Actions workflow

Workflow file:

```text
.github/workflows/sitemap.yml
```

Current order:

```text
1. Apply canonical links
2. Apply static link hygiene
3. Apply JSON-LD structured data
4. Apply Open Graph tags
5. Generate sitemap.xml
6. Submit sitemap URLs to IndexNow
7. Commit changed generated files if needed
```

Trigger paths include:

```text
**/*.html
scripts/apply-canonical.js
scripts/apply-static-links.js
scripts/apply-jsonld.js
scripts/apply-og.js
scripts/generate-sitemap.js
scripts/submit-indexnow.js
b2cda9f3e8714a6db926f48c7251ea65.txt
assets/og/**
.github/workflows/sitemap.yml
```

## Files created / updated on the website repository

Important generated / automation files:

```text
scripts/apply-canonical.js
scripts/apply-static-links.js
scripts/apply-jsonld.js
scripts/apply-og.js
scripts/generate-sitemap.js
scripts/submit-indexnow.js
.github/workflows/sitemap.yml
robots.txt
sitemap.xml
llms.txt
b2cda9f3e8714a6db926f48c7251ea65.txt
assets/og/.gitkeep
assets/og/ashraellen-og-home-default-1200x630.jpg
```

Important HTML-wide effects:

```text
H1 corrected on all language roots.
Canonical links applied.
Static navigation links normalized.
JSON-LD inserted.
Open Graph / Twitter Card tags inserted.
Sitemap regenerated.
IndexNow submission automated.
```

## Current status after the work

Current practical status:

```text
The site is technically much more readable for Google, Bing and AI crawlers.
The root URL and language pages produce social preview cards.
Telegram preview was tested successfully.
Bing Live URL inspection showed clean result for checked page after updates.
Google already had the root page indexed, but needs time to recrawl after updates.
```

What should be expected:

```text
Search Console and Bing reports may lag behind the actual deployed state.
Do not panic if old warnings remain visible for a while.
Give crawlers time to recrawl.
```

## Next recommended steps

### Short-term checks

```text
1. Re-check selected pages in Bing Live URL after deploy delay.
2. Re-check Google URL Inspection for root, /en/, /ru/, /pl/ after several days.
3. Check that sitemap is processed successfully in Google Search Console.
4. Test a few internal links in Telegram after cache refresh.
```

### Next technical layer

Create separate OG images and update `scripts/apply-og.js` to choose images by page type:

```text
assets/og/research.jpg
assets/og/professional.jpg
assets/og/books.jpg
assets/og/monolith.jpg
assets/og/beton.jpg
assets/og/sludge.jpg
```

Suggested mapping:

```text
/research/ -> research.jpg
/professional/ -> professional.jpg
/books/ -> books.jpg
/books/monolith/ -> monolith.jpg
/books/monolith/beton/ -> beton.jpg
/books/monolith/sludge/ -> sludge.jpg
fallback -> ashraellen-og-home-default-1200x630.jpg
```

### Next content layer

Create thematic pillar pages for better semantic discovery:

```text
Artistic Research
Literary-Philosophical Research
Digital Autonomy
Inner Observation
Satire as Method of Observation
MONOLITH as Social Fiction
Consciousness, Language and Systems
```

These pages should remain faithful to Ashraellen's actual framing and must not become SEO filler.

## Working rules for future chats

1. Before changing the site, read this file and inspect the current website repository state.
2. Do not add `href="#"` or `src="#"` placeholders.
3. Do not rely on client-side JavaScript for essential search / AI / preview metadata.
4. Keep semantic information available in static HTML.
5. Keep PWA icons and OG images separate.
6. Use `Ashraellen` as the public author name.
7. Preserve the project framing as independent artistic / literary-philosophical research.
8. Avoid turning the site into SEO filler or a generic personal brand page.
