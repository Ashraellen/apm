# Unresolved Decisions — Error404 MemorySystem

Status: active conflict tracker
Created: 2026-06-22
Updated: 2026-06-22

Purpose:

This file stores unresolved, contradictory or not-yet-authorized decisions for `Error 404: God Not Found` / `Ошибка 404: Бог не найден`.

Nothing from this file should be promoted into `MASTER_Error404.md`, `Characters/`, `Canon/`, `Chapters/` or `Translations/` without a direct author decision.

---

## Conflict: grey cotton / Window No. 7 acoustics

Status: conflict / needs author decision

### What one source says

Some imported chat memories preserve or strengthen the atmosphere of `серой ваты`, `голос тонет`, acoustic/existential muting, a cotton hall, or voices sinking in Window No. 7.

Some local memory still contains a grey-cotton-like description of the waiting hall, where voices do not become normal dialogue.

### What another source says

Other imported memory says this older mechanism was corrected / rejected:

- no grey wool as a physical/acoustic mechanism;
- no voice sinking as if the hall literally swallows speech;
- Vlad's voice exists;
- he speaks aloud;
- others simply do not hear his words as addressed to them;
- the rule is not acoustic muting, but non-conversation / self-talk intersection.

### Why it matters

This affects how Window No. 7 is staged in Chapters 2 and 21.

If it is written as acoustic muting, Window No. 7 becomes more supernatural and atmospheric.

If it is written as non-addressed speech / intersecting self-monologues, Window No. 7 remains more psychologically and metaphysically precise.

This also affects future uses of Window No. 7 in the cycle.

### Suggested next question for author

Should `серaя вата` remain only as atmosphere / subjective feeling, or should all acoustic-muting language be removed and replaced with the rule:

`Vlad speaks aloud, but others do not hear his words as addressed to them; their self-talk only intersects his question.`

---

## Conflict: repository identity — Ashraellen/ashraellen-apm vs Ashraellen/apm

Status: conflict / needs author decision

### What one source says

Several imported chat memories report work done in:

`Ashraellen/ashraellen-apm`

These imports mention commits, file paths, archive folders, chapter uploads, readable project files, translation rules and chapter versions that may have been created in that repository.

### What another source says

The current MemorySystem work is being performed in:

`Ashraellen/apm`

Current user instruction explicitly uses:

`Ashraellen/apm`

as the target repository for Error404 MemorySystem work.

### Why it matters

If older files exist only in `Ashraellen/ashraellen-apm`, then paths and commit SHAs from raw imports cannot be treated as verified current project state in `Ashraellen/apm`.

This affects:

- chapter file inventory;
- old-version archives;
- translation rules;
- `VOLUME_I/` structure;
- commit SHA references;
- whether some files need migration or should be ignored.

### Suggested next question for author

Is `Ashraellen/apm` now the only canonical repository for Error404, and should any files or commits from `Ashraellen/ashraellen-apm` be migrated, ignored, or treated as historical residue?

---

## Conflict: language system — imported nine-language plan vs README_ABBREVIATIONS.md

Status: conflict / needs author decision

### What one source says

Imported chat memory proposes a nine-language system:

```text
RU — Russian
EN — English
PL — Polish
DE — German
FR — French
ES — Spanish
PT — Portuguese
UK — Ukrainian
BE — Belarusian
```

It also proposes a flexible source-language rule:

- RU is the semantic / authorial base;
- EN v3 is the international support version, especially for bureaucratic-tech interface;
- Slavic languages often use RU as base;
- Western European languages may use EN v3 plus RU cross-check.

### What another source says

The current root `README_ABBREVIATIONS.md` contains a different language abbreviation set:

```text
RU — Russian
EN — English
PL — Polish
DE — German
UA — Ukrainian
FI — Finnish
```

It does not include FR, ES, PT or BE in that visible set, and it uses `UA` rather than `UK` for Ukrainian.

### Why it matters

This affects:

- file naming conventions;
- translation folders;
- abbreviation consistency;
- future multilingual publication workflow;
- whether Finnish remains in the active language plan;
- whether Ukrainian is coded as `UA` or `UK`.

If this is promoted without author decision, the project may split into incompatible language systems.

### Suggested next question for author

What is the current official language set and code system for Error404?

Options to decide:

1. Keep root `README_ABBREVIATIONS.md` set as current.
2. Replace it with the imported nine-language system.
3. Create a revised hybrid language plan with explicit author-approved codes.

---

## Conflict: archive structure — OLD_VERSIONS vs 99_AOV / 98_TRASH_REVIEW

Status: conflict / needs author decision

### What one source says

Imported chat memory mentions language-folder archives such as:

```text
Projects/Error404/VOLUME_I/RU/OLD_VERSIONS/
Projects/Error404/VOLUME_I/EN/OLD_VERSIONS/
Projects/Error404/VOLUME_I/PL/OLD_VERSIONS/
```

### What another source says

The current root `README_ABBREVIATIONS.md` describes archive / review logic using:

```text
99_AOV
98_TRASH_REVIEW
```

### Why it matters

This affects future cleanup, file discovery, version sorting and long-term storage.

If both systems are used without rules, old versions may scatter between archives.

### Suggested next question for author

Should Error404 use language-local `OLD_VERSIONS/` folders, root-style `99_AOV` / `98_TRASH_REVIEW`, or a hybrid rule where current language folders may have local `OLD_VERSIONS/` but root README must be updated later to reflect that?
