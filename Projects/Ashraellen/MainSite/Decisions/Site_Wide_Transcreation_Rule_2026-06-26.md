# Site-wide transcreation rule

Date: 2026-06-26
Project: Ashraellen MainSite
Status: active site-wide content rule

## 1. Core rule

All public-facing multilingual content for Ashraellen.com must be created through transcreation, not literal translation.

This applies to every new content type and page type unless a specific technical or legal exception is explicitly stated.

## 2. What transcreation means here

Transcreation means that each language version must preserve:

```text
- the inner meaning
- the function of the text
- the emotional temperature
- the rhythm
- the cultural naturalness
- the silence or aftertaste after the phrase
- the intended reader effect
```

The target language text should sound as if it was originally written in that language.

Do not force Russian sentence structure, idioms, word order or rhetorical rhythm into other languages.

## 3. Site-wide scope

This rule applies to:

```text
- home pages
- section pages
- research pages
- public pages
- Public Thoughts / Опорные мысли
- Public Posts / Formula
- Books / MONOLITH pages
- grant-facing pages
- language landing pages
- navigation-visible descriptions
- page leads and summaries
- SEO descriptions where they carry meaning, tone or positioning
- future content types unless explicitly exempted
```

## 4. Default creation workflow

When creating multilingual content:

```text
1. Create or approve the source-language meaning.
2. Identify what the text must do for the reader.
3. Create each language version as a natural-language original.
4. Preserve the same function, tone and inner movement.
5. Do not publish raw literal translation as final content.
```

The default creative source language may be Russian, but the target language version is not a subordinate copy. It is a language-specific version of the same work.

## 5. Page creation rule

For final published pages, prefer self-contained static HTML with the transcreated text already present in the page.

Avoid creating empty language shells that depend on client-side text injection unless there is a concrete technical reason.

Data files or shared renderers may be used as a temporary working layer or as a source for generation, but the preferred final publication state is:

```text
transcreated content → embedded in the published page
```

not:

```text
empty page → JavaScript → JSON → visible text
```

## 6. Exceptions

Literal preservation is allowed or required for:

```text
- URLs and slugs
- file paths
- code
- canonical labels that were explicitly fixed
- product/project names
- personal names
- legal or administrative wording where exactness matters
- schema/metadata fields that require stable identifiers
- the fixed seal label: — mark of presence
```

Even when exact terms must be preserved, surrounding explanatory text should still be transcreated.

## 7. Relation to Formula posts

The Formula section follows this site-wide rule.

Formula-specific files such as:

```text
assets/formula-multilingual.js
assets/formulas/<lang>.json
```

exist because the multilingual formula layer was first built technically and then corrected through transcreation.

They are acceptable as the current working implementation, but they must not become the default assumption for all future content.

For future Formula lines, transcreation should happen before publication, and the final pages should preferably be self-contained unless there is a technical reason to keep shared data rendering.

## 8. Relation to Public Thoughts

Public Thoughts also follow this rule.

A support thought in another language should not be a literal translation of the Russian page. It should preserve the same:

```text
- central image
- inner turn
- contemplative rhythm
- final movement
- reader effect
```

while sounding native to that language.

## 9. Future-chat instruction

Future chats must not ask whether transcreation is needed for Ashraellen.com multilingual content.

It is the default.

Ask only when there is uncertainty about:

```text
- tone
- target audience
- institutional vs poetic register
- whether a fixed term must remain unchanged
- whether a page is final publication or temporary working material
```
