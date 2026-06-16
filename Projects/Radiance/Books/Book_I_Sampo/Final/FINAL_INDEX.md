# FINAL_INDEX — Book I: Сампо

Final proofreading index for **Сияние / Radiance — Book I: Сампо**.

This file is the shared working board for the final proofreading process.

---

## 1. Purpose

This index coordinates the work between:

1. The main proofreading chat.
2. The proofreading controller / consultant.
3. The author as final decision-maker.

The workflow must proceed **one chapter at a time**.

Do not run batches of three chapters unless the author explicitly changes this rule.

---

## 2. GitHub text layer

Proofreader protocol:

```text
Projects/Radiance/Books/Book_I_Sampo/Final/PROTOCOL_proofreader.md
```

Controller protocol:

```text
Projects/Radiance/Books/Book_I_Sampo/Final/PROTOCOL_controller.md
```

Source drafts:

```text
Projects/Radiance/Books/Book_I_Sampo/Drafts/
```

Final proofread Markdown files:

```text
Projects/Radiance/Books/Book_I_Sampo/Final/
```

Main book index:

```text
Projects/Radiance/Books/Book_I_Sampo/INDEX.md
```

GitHub rule:

```text
GitHub stores the official text source in .md format only.
```

---

## 3. Google Drive DOCX layer

Google Drive is used for human-readable DOCX working copies after a chapter is accepted in GitHub.

Drive root project folder:

```text
Radiance
```

Folder ID:

```text
1UIG8DSEK4n9K17TzwQj_-kAsAPcSc9E_
```

URL:

```text
https://drive.google.com/drive/folders/1UIG8DSEK4n9K17TzwQj_-kAsAPcSc9E_
```

Book folder:

```text
Radiance / Book_I_Sampo
```

Folder ID:

```text
1c7BZTJJzVpUaY3Sf7rMvRw1ti-odi0b8
```

URL:

```text
https://drive.google.com/drive/folders/1c7BZTJJzVpUaY3Sf7rMvRw1ti-odi0b8
```

Chapter DOCX folder:

```text
Radiance / Book_I_Sampo / Final_DOCX
```

Folder ID:

```text
1IMwk5Jzuu8K0vNRbMEChgAXRRNUjuIvT
```

URL:

```text
https://drive.google.com/drive/folders/1IMwk5Jzuu8K0vNRbMEChgAXRRNUjuIvT
```

Full book DOCX folder:

```text
Radiance / Book_I_Sampo / Full_Book_DOCX
```

Folder ID:

```text
18fdZXa4lJJikF4K-nso-6hTpi2s-MowE
```

URL:

```text
https://drive.google.com/drive/folders/18fdZXa4lJJikF4K-nso-6hTpi2s-MowE
```

DOCX rule:

```text
Google Drive stores only .docx working/readable files and the final full-book .docx.
```

Recommended DOCX workflow:

```text
Final/Chapter_XX_final_vY.md
→ controller approval
→ create Chapter_XX_final_vY.docx
→ upload to Google Drive / Final_DOCX
```

The full book DOCX is created only after all chapters and epilogue are approved final:

```text
Sampo_Book_I_final_v1.docx
→ upload to Google Drive / Full_Book_DOCX
```

---

## 4. Status labels

Use these statuses:

```text
not started
proofreading in progress
awaiting controller approval
approved final
approved final after micro-corrections
returned for another pass
superseded by newer final version
DOCX created on Google Drive
DOCX created locally; Drive upload failed
```

---

## 5. One-chapter workflow

For each chapter:

1. Proofreader reads the active source draft.
2. Proofreader creates `*_final_v1.md` directly in `Final/`.
3. Proofreader updates this index: status becomes `awaiting controller approval`.
4. Controller checks that final file.
5. Controller gives a verdict.
6. If approved, this index is updated to `approved final`.
7. If micro-corrections are needed, proofreader creates `*_final_v2.md`.
8. Older final versions are kept and marked as `superseded by newer final version`.
9. After approval, a DOCX copy may be created and uploaded to Google Drive / `Final_DOCX`.

---

## 6. Current proofreading queue

Current target:

```text
Chapter 02 — Drafts/Chapter_02_v2.md
```

Recommended next action:

```text
Proofreader should start with Chapter 02 only.
```

Do not begin Chapter 03 until Chapter 02 is either approved or explicitly put aside by the author.

---

## 7. Current final files

| Order | Unit | Source draft | Current final file | Status | Controller verdict | Notes |
|---:|---|---|---|---|---|---|
| 0 | Prologue | `Drafts/Prologue_Hook_v1.md` | `Prologue_final_v1.md` | approved final | accepted by author/controller | Accepted by author on 2026-06-16. DOCX may now be created. |
| 1 | Chapter 01 | `Drafts/Chapter_01_v2.md` | `Chapter_01_final_v1.md` | approved final | accepted by author/controller | Accepted by author on 2026-06-16. DOCX created locally; Drive upload failed due connector file-reference validation. |
| 2 | Chapter 02 | `Drafts/Chapter_02_v2.md` | — | not started | — | Start here. |
| 3 | Chapter 03 | `Drafts/Chapter_03_v3.md` | — | not started | — |  |
| 4 | Chapter 04 | `Drafts/Chapter_04_v2.md` | — | not started | — |  |
| 5 | Chapter 05 | `Drafts/Chapter_05_v2.md` | — | not started | — |  |
| 6 | Chapter 06 | `Drafts/Chapter_06_v2.md` | — | not started | — |  |
| 7 | Chapter 07 | `Drafts/Chapter_07_v2.md` | — | not started | — |  |
| 8 | Chapter 08 | `Drafts/Chapter_08_v2.md` | — | not started | — |  |
| 9 | Chapter 09 | `Drafts/Chapter_09_v1.md` | — | not started | — |  |
| 10 | Chapter 10 | `Drafts/Chapter_10_v2.md` | — | not started | — |  |
| 11 | Chapter 11 | `Drafts/Chapter_11_v2.md` | — | not started | — |  |
| 12 | Chapter 12 | `Drafts/Chapter_12_v1.md` | — | not started | — |  |
| 13 | Chapter 13 | `Drafts/Chapter_13_v2.md` | — | not started | — |  |
| 14 | Chapter 14 | `Drafts/Chapter_14_v1.md` | — | not started | — |  |
| 15 | Chapter 15 | `Drafts/Chapter_15_v1.md` | — | not started | — |  |
| 16 | Chapter 16 | `Drafts/Chapter_16_v1.md` | — | not started | — |  |
| 17 | Chapter 17 | `Drafts/Chapter_17_v1.md` | — | not started | — |  |
| 18 | Chapter 18 | `Drafts/Chapter_18_v1.md` | — | not started | — |  |
| 19 | Chapter 19 | `Drafts/Chapter_19_v1.md` | — | not started | — |  |
| 20 | Chapter 20 | `Drafts/Chapter_20_v1.md` | — | not started | — |  |
| 21 | Chapter 21 | `Drafts/Chapter_21_v1.md` | — | not started | — |  |
| 22 | Chapter 22 | `Drafts/Chapter_22_v1.md` | — | not started | — |  |
| 23 | Chapter 23 | `Drafts/Chapter_23_v1.md` | — | not started | — |  |
| 24 | Chapter 24 | `Drafts/Chapter_24_v1.md` | — | not started | — |  |
| 25 | Epilogue | `Drafts/Epilogue_v1.md` | — | not started | — |  |

---

## 8. Google Drive DOCX files

| Unit | Approved Markdown source | DOCX file | Google Drive folder | Status | Notes |
|---|---|---|---|---|---|
| Prologue | `Prologue_final_v1.md` | — | `Final_DOCX` | not created | Can be created after author confirmation. |
| Chapter 01 | `Chapter_01_final_v1.md` | `Chapter_01_final_v1.docx` | `Final_DOCX` | DOCX created locally; Drive upload failed | Local DOCX rendered and visually checked; Drive connector rejected local file path/file reference. Retry upload later. |

---

## 9. Preserved earlier final versions

No earlier final versions yet.

When a newer final version replaces an earlier one, record it here.

Example:

```markdown
- Chapter 01:
  - `Chapter_01_final_v1.md` — superseded by `Chapter_01_final_v2.md`
```

---

## 10. Controller decisions log

## 2026-06-16 — Prologue

Final checked file:

`Prologue_final_v1.md`

Verdict:

`approve`

Notes:

- Accepted by author/controller.
- Proceed to Chapter 01 only.

## 2026-06-16 — Chapter 01

Final checked file:

`Chapter_01_final_v1.md`

Verdict:

`approve`

Notes:

- Accepted by author/controller.
- DOCX created locally as `Chapter_01_final_v1.docx` and rendered for visual QA.
- Google Drive upload failed because the connector rejected the local file reference.
- Proceed to Chapter 02 only.

---

## 11. Main rule

One chapter at a time.

The next chapter begins only after the current chapter receives a controller verdict or the author explicitly decides to move on.
