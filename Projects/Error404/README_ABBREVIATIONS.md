# README_ABBREVIATIONS

Project: **ERROR_404 / God Not Found**  
Book I: **Why Me? / Почему я?**

This file explains the abbreviations used in the folder structure, file names, language versions, and version logic of the project.

---

## 1. Core project abbreviations

| Abbreviation | Meaning | Notes |
|---|---|---|
| E404 | Error 404 | Short project code |
| GNF | God Not Found | Full project title: *Error 404: God Not Found* |
| B1 | Book 1 | First book of the cycle |
| WM | Why Me? | Title of Book I / Russian working title: *Почему я?* |
| CH | Chapter | Chapter number in file names |
| V / Vol | Volume | Used for large structural parts |
| v1, v2, v3 | Version number | Higher number means newer version unless stated otherwise |

---

## 2. Language abbreviations

| Abbreviation | Meaning | Notes |
|---|---|---|
| RU | Russian | Original Russian version |
| EN | English | English version / future translation |
| PL | Polish | Polish version / future translation |
| DE | German | German version, if needed later |
| UA | Ukrainian | Ukrainian version, if needed later |
| FI | Finnish | Finnish version, if needed later |

Language code is placed after the main project code and separated with a hyphen.

Example:

```text
E404GNFB1WM-RU_CH13_v2.md
E404GNFB1WM-EN_CH13_v1.md
E404GNFB1WM-PL_CH13_v1.md
```

---

## 3. File format abbreviations

| Abbreviation | Meaning | Notes |
|---|---|---|
| MD | Markdown | Main clean text format |
| TXT | Plain Text | Universal backup/export format |
| DOCX | Microsoft Word document | Editable formatted document |
| PDF | Portable Document Format | Fixed-format export, usually for reading or sending |
| EPUB | Ebook format | Used for ebook publication/export |

---

## 4. Folder abbreviations

| Folder | Meaning | Purpose |
|---|---|---|
| 00_ENGINE | Core Engine / Core Prompt | Main project instructions, prompts, working rules, canon of process |
| 01_LORE | Lore & Universe | Worldbuilding, internal logic, metaphysics, recurring rules and mechanisms |
| 02_VOLUME_I | Volume I / Book I | Materials for Book I: *Why Me? / Почему я?* |
| 03_VOLUME_II | Volume II | Materials for the second volume/book |
| 04_VOLUME_III | Volume III | Materials for the third volume/book |
| 05_PROD_MKT | Production & Marketing | Covers, descriptions, site texts, promotion, publication materials |
| 99_AOV | Archive Old Versions | Archive for older versions of chapters or documents |

---

## 5. Why folder numbers are used

Folder numbers are used for sorting.

- `00` means core/root materials.
- `01`, `02`, `03`, etc. show the main working order.
- `99` means archive or non-current materials.

Example:

```text
00_ENGINE
01_LORE
02_VOLUME_I
03_VOLUME_II
04_VOLUME_III
05_PROD_MKT
99_AOV
```

The `99_` prefix keeps archive folders at the bottom of the list and prevents old files from mixing with current working files.

---

## 6. Short chapter file naming pattern

Recommended short chapter file naming pattern:

```text
E404GNFB1WM-LANG_CHXX_vN.ext
```

Where:

| Part | Meaning |
|---|---|
| E404 | Error 404 |
| GNF | God Not Found |
| B1 | Book 1 |
| WM | Why Me? |
| LANG | Language code: RU, EN, PL, etc. |
| CHXX | Chapter number, always two digits |
| vN | Version number |
| ext | File extension: md, docx, txt, pdf, etc. |

Examples:

```text
E404GNFB1WM-RU_CH01_v1.md
E404GNFB1WM-RU_CH13_v2.docx
E404GNFB1WM-RU_CH22_v2.txt
E404GNFB1WM-EN_CH13_v1.md
E404GNFB1WM-PL_CH13_v1.md
```

Underscores are used only before the chapter number and the version:

```text
_CHXX
_vN
```

The language code is separated with a hyphen:

```text
-LANG
```

Correct:

```text
E404GNFB1WM-RU_CH13_v2.md
```

Not recommended:

```text
E404_GNF_Book1_Why_Me_Glava_13_Korobka_v2.md
E404_GNF_B1_WM_G13_v2.md
```

---

## 7. Version logic for chapters

The main rule:

```text
Chapter number is more important than chapter title.
The highest version number is considered current.
Older versions must be moved to 99_AOV, not deleted immediately.
```

Titles may change after rewriting.  
A chapter can keep the same number but receive a new title after full rewriting.

Therefore, sorting must be based on:

```text
1. Chapter number
2. Language version
3. Highest version number
4. Available file formats
```

Not primarily on the title.

---

## 8. Example of chapter version sorting

Example:

```text
E404GNFB1WM-RU_CH19_v1.md
E404GNFB1WM-RU_CH19_v2.md
E404GNFB1WM-RU_CH19_v3.md
```

Current version:

```text
E404GNFB1WM-RU_CH19_v3.md
```

Archive:

```text
E404GNFB1WM-RU_CH19_v1.md
E404GNFB1WM-RU_CH19_v2.md
```

---

## 9. Working and archive format rules

For the current working version of a chapter, keep all main working formats:

```text
.md
.docx
.txt
```

Example:

```text
E404GNFB1WM-RU_CH13_v2.md
E404GNFB1WM-RU_CH13_v2.docx
E404GNFB1WM-RU_CH13_v2.txt
```

For old archived versions, keep only the clean text source:

```text
.md
```

Example:

```text
99_AOV/E404GNFB1WM-RU_CH13_v1.md
```

Old `.docx` and `.txt` files do not need to be preserved in the archive if the matching `.md` version exists and has been checked.

Recommended rule:

```text
Current chapter version = md + docx + txt
Old archived chapter version = md only
```

---

## 10. Archive rule

The archive is not trash.

`99_AOV` stores old versions so the project history is preserved, but the working folder remains clean.

Do not delete older chapter versions until the matching `.md` archive copy has been checked.

After confirmation, old `.docx` and `.txt` files for archived versions may be deleted or temporarily placed in a review folder.

Possible temporary review folder:

```text
98_TRASH_REVIEW
```

This folder is only for files planned for deletion after manual confirmation.

---

## 11. Recommended cleanup workflow

For each chapter:

```text
1. Rename files using the short naming pattern.
2. Identify the highest version number for each chapter.
3. Keep the highest version in the working folder.
4. Keep md + docx + txt only for the current version.
5. Move older md files to 99_AOV.
6. Delete or review old docx/txt files only after the md archive is confirmed.
```

Example:

Working folder:

```text
E404GNFB1WM-RU_CH19_v3.md
E404GNFB1WM-RU_CH19_v3.docx
E404GNFB1WM-RU_CH19_v3.txt
```

Archive:

```text
99_AOV/E404GNFB1WM-RU_CH19_v1.md
99_AOV/E404GNFB1WM-RU_CH19_v2.md
```

Old removable files after confirmation:

```text
E404GNFB1WM-RU_CH19_v1.docx
E404GNFB1WM-RU_CH19_v1.txt
E404GNFB1WM-RU_CH19_v2.docx
E404GNFB1WM-RU_CH19_v2.txt
```

---

## 12. Final working principle

```text
Keep the current version visible.
Keep old versions safe in md.
Do not trust the title more than the chapter number and version.
Use short technical names for files.
Use full chapter titles inside the documents, not in file names.
```

A chapter may change its title.  
A version number usually tells the truth more reliably.
