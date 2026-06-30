# LOCAL FILE HANDOFF FALLBACK RULE

Date: 2026-06-30
Scope: Editorial Stabilization / Formula Staticization
Status: active fallback rule

## Purpose

If GitHub connector writes repeatedly fail for a small, clearly scoped set of files, do not keep retrying through the connector indefinitely.

Use a local file handoff instead.

## Rule

After two controlled write attempts fail for the same small file group:

```text
1. Stop live-site write attempts.
2. Do not run emergency repair scripts.
3. Do not broaden scope.
4. Prepare replacement files locally with the exact repository filenames and paths.
5. Package them for manual download.
6. Tell the user exactly where each file must be uploaded in the live repository.
7. The user may then upload the files manually with replacement.
```

## Required handoff format

The handoff package must preserve repository paths.

Example:

```text
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0001.html
be/public/posts/formula/lines/line-0002.html
```

The downloadable package should preferably be a `.zip` containing the same directory structure.

## Required validation before handoff

Before providing files to the user, verify locally or by inspection:

```text
- each file is valid static HTML;
- visible Formula cards are present;
- 15 Formula cards per page;
- no formula-multilingual.js dependency;
- no empty formulaRoot shell;
- static title/description/keywords/canonical exist;
- one page-specific JSON-LD block exists;
- code-garbage keywords are absent;
- seal label `— mark of presence` is preserved.
```

## Current trigger case

This rule applies to the remaining BE Formula pages if `COMMAND_003C_Retry2_Formula_Staticization_BE_Remaining.md` also fails to write them through the connector.

Current target files:

```text
be/public/posts/formula/lines/index.html
be/public/posts/formula/lines/line-0001.html
be/public/posts/formula/lines/line-0002.html
```

## Manual upload instruction pattern

Tell the user:

```text
Unzip the package.
Upload each file to the matching path in Ashraellen/ashraellen, replacing the existing file with the same name.
Do not rename files.
Do not upload the parent folder into the wrong level.
```

## After manual upload

After the user uploads the files, run or wait for the safe sitemap/report workflow if needed.

Do not run the emergency metadata repair workflow unless explicitly approved.
