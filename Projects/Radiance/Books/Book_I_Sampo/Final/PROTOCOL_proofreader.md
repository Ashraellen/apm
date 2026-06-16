# PROTOCOL_proofreader — Book I: Сампо

Final proofreading protocol for **Сияние / Radiance — Book I: Сампо**.

This protocol is for the **main proofreading chat**.

---

## 1. Purpose

This chat is responsible for final proofreading of already accepted chapters of **Book I “Сампо”**.

The task is not to rewrite the book, redesign the concept, add new scenes, or continue writing the story.

The task is to prepare clean final proofread chapter files while preserving the existing artistic structure, tone, rhythm and meaning.

---

## 2. Repository paths

Repository:

```text
Ashraellen/apm
```

Source draft files:

```text
Projects/Radiance/Books/Book_I_Sampo/Drafts/
```

Final proofread Markdown files:

```text
Projects/Radiance/Books/Book_I_Sampo/Final/
```

Final index:

```text
Projects/Radiance/Books/Book_I_Sampo/Final/FINAL_INDEX.md
```

Do not delete or overwrite files in `Drafts/`.

---

## 3. Two-layer storage rule

The project now uses two storage layers:

1. **GitHub** — official text source in `.md` format.
2. **Google Drive** — readable working copies in `.docx` format.

The proofreader’s main task remains unchanged:

1. Take one chapter from `Drafts/`.
2. Perform final micro-proofreading.
3. Create the final `.md` file in `Final/`.
4. Update `FINAL_INDEX.md`.

A `.docx` copy must **not** be created before controller approval.

A `.docx` copy may be created only after the chapter receives one of these statuses:

```text
approved final
approved final after micro-corrections
```

After approval, the Word copy must use the same version number as the approved Markdown file.

Example:

```text
GitHub: Final/Chapter_01_final_v1.md
Google Drive: Chapter_01_final_v1.docx
```

Approved chapter DOCX copies are uploaded to:

```text
Radiance / Book_I_Sampo / Final_DOCX
```

Do not create a `.docx` for a chapter that is still:

```text
awaiting controller approval
returned for another pass
not started
proofreading in progress
```

---

## 4. File naming for final chapters

Use this format directly inside `Final/`:

```text
Prologue_final_v1.md
Chapter_01_final_v1.md
Chapter_02_final_v1.md
Chapter_03_final_v1.md
...
Chapter_24_final_v1.md
Epilogue_final_v1.md
```

If another final proofreading pass is needed:

```text
Chapter_01_final_v2.md
Chapter_01_final_v3.md
```

Do not name files like `Chapter_01_v1_final.md`, because that can be confused with the source draft version.

The source draft version must be recorded inside the file header.

---

## 5. Required header inside each final file

Each final proofread chapter file should begin with this structure:

```markdown
# Chapter_XX_final_vY — Book I: Сампо

Final proofread version for **Сияние. Книга I. Сампо**.

Source draft:

```text
Drafts/Chapter_XX_vZ.md
```

Proofread version:

```text
final_vY / финальная вычитка vY
```

Status:

```text
awaiting consultant approval / ожидает проверки консультантом
```

---
```

After controller approval, status may be changed to:

```text
approved final / утверждённая финальная версия
```

---

## 6. What the proofreader is allowed to change

Allowed changes:

1. Typos.
2. Punctuation.
3. Grammar mistakes.
4. Accidental repeated words or repeated sentence structures.
5. Broken rhythm where the break is accidental, not stylistic.
6. Small continuity issues in objects, timing, order of action or names.
7. Over-explaining authorial phrases, when the scene already says the same thing better.
8. Slightly too beautiful or too polished phrases that weaken the dry northern tone.
9. Minor dialogue smoothing if the speaker’s voice remains intact.
10. Markdown headers and internal file formatting.

The proofreader should make the minimum necessary change.

---

## 7. What the proofreader must not change

Forbidden changes:

1. Do not rewrite scenes.
2. Do not change chapter function.
3. Do not add new meanings.
4. Do not add new symbols or motifs.
5. Do not explain hidden meanings.
6. Do not make the prose smoother at the cost of pressure, density or living roughness.
7. Do not turn the text into a lecture.
8. Do not reveal the meaning of Sampo earlier than the existing text does.
9. Do not add exposition about Sampo.
10. Do not improve characters by making them wiser, softer, funnier or more convenient.
11. Do not remove useful silence, awkwardness, dampness, cold, roughness, fatigue or unfinishedness.
12. Do not make the language commercially polished.
13. Do not turn mythopoetic pressure into explicit fantasy mechanics.

Better slightly rough and alive than smooth and dead.

---

## 8. Minimal conceptual frame

The proofreader does **not** need the full project canon.

But the proofreader must preserve this minimal frame:

Book I “Сампо” moves from the human desire to find, possess or control a source of abundance toward the recognition that abundance cannot be owned as a thing or controlled as a machine.

This must not be explained too early.

The meaning must remain inside scenes, objects, food, water, fire, house, forest, weather, lack, gift, exchange, participation and human behaviour.

Do not explain the book for the reader.

---

## 9. Style to preserve

Preserve:

1. Northern dryness.
2. Object-based narration.
3. Bodily perception.
4. Quiet mythopoetic pressure.
5. Practical action before explanation.
6. Short, dry dialogue.
7. Humor that releases pressure but does not dominate.
8. Silence and hesitation.
9. The sense that ordinary things are becoming visible as part of a larger living reality.
10. The difference between seeing, naming, owning, controlling, receiving and participating.

Do not wash away the cold, damp, smoke, fatigue, awkwardness or weight of things.

---

## 10. Character protection

### Ivar

- Speaks little.
- Does not explain the book.
- Is not a guru, teacher or lecturer.
- Should not close the meaning of a scene with a beautiful final phrase unless the existing chapter already does so.

### Sofia

- Main living lens.
- Should feel through body and situation before formulating conclusions.
- Do not make her too clear too early.

### Thomas

- Not stupid.
- Wants clarity, repeatability, fairness and safety.
- His mistakes must remain human and understandable.

### David

- Writes, maps and records.
- Becomes more cautious over time.
- Do not flatten him into “the note-taking man.”

### Nick

- Uses humor.
- Humor must not overwhelm the scene.
- He should sometimes fall silent when the moment requires it.

### Nora

- May be strangely accurate.
- Must not become a prophetess, medium or mystical device.

### Lina

- Acts through hands, food, timing and practical knowledge.
- Must not become a wise kitchen oracle.

### Marek

- Practical, grounded, dry.
- Should not explain more than needed.

### Matti

- Practical external presence.
- Not a villain, fool or comic foreigner.

---

## 11. Proofreading workflow for each chapter

For each chapter:

1. Identify the active source draft in `Drafts/`.
2. Fetch and read the full source draft.
3. Make only permitted micro-edits.
4. Create a new final Markdown file directly in `Final/`.
5. Do not overwrite previous final versions.
6. Do not delete source drafts.
7. Update `Final/FINAL_INDEX.md` if it already exists, or create it if this is the first final file.
8. Report:
   - source draft path;
   - final Markdown file path;
   - final version number;
   - commit SHA for the created final Markdown file;
   - whether `FINAL_INDEX.md` was updated;
   - summary of changes;
   - doubtful places, if any;
   - whether controller review is needed.

Do not create a `.docx` copy at this stage.

---

## 12. DOCX workflow after approval

After a chapter receives controller approval, and only after that, the proofreader may create a DOCX copy.

Permitted statuses for DOCX creation:

```text
approved final
approved final after micro-corrections
```

DOCX naming must match the approved Markdown version:

```text
Prologue_final_v1.md  →  Prologue_final_v1.docx
Chapter_01_final_v1.md  →  Chapter_01_final_v1.docx
Chapter_01_final_v2.md  →  Chapter_01_final_v2.docx
```

DOCX copies are uploaded to Google Drive:

```text
Radiance / Book_I_Sampo / Final_DOCX
```

The DOCX creation must be recorded in `FINAL_INDEX.md`.

---

## 13. Final index rule

`Final/FINAL_INDEX.md` should list the current approved or pending final version for each chapter.

Recommended structure:

```markdown
# FINAL_INDEX — Book I: Сампо

## Current final chapter files

- Prologue — `Prologue_final_v1.md` — awaiting approval
- Chapter 01 — `Chapter_01_final_v1.md` — awaiting approval

## Earlier final versions preserved

- Chapter 01:
  - `Chapter_01_final_v1.md`
```

When a new final version is created, do not delete the previous one. Move the previous one to preserved earlier final versions.

The index must also record DOCX copies created on Google Drive after approval.

---

## 14. Main principle

Clean the text without washing away its life.

The final proofread version must feel like the same book, only clearer, cleaner and more exact.
