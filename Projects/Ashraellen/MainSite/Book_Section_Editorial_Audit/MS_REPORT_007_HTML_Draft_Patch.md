# MS REPORT 007 — BETON HTML Draft / Patch Plan

Date: 2026-07-01  
Project: Ashraellen / MainSite / Book Section Editorial Audit  
Status: short handoff report for MS

---

## 1. Status

`COMMAND_007_HTML_Draft_Patch.md` выполнен.

Создан HTML draft / patch plan для будущей HTML-правки страницы:

```text
ru/books/monolith/beton/index.html
```

Live site не изменялся. HTML-файлы не редактировались.

---

## 2. Files created

Основной HTML draft / patch plan:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_007_HTML_Draft_Patch.md
```

Короткий MS-отчёт:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_007_HTML_Draft_Patch.md
```

---

## 3. Proposed changes

В `DRAFT_007` подготовлен section-by-section HTML draft / pseudo-diff для будущего расширения `БЕТОНА`.

Предлагается:

1. Заменить текущий короткий lead:

```text
Первый том трилогии «МОНОЛИТ».
```

на более холодный hero lead:

```text
БЕТОН — философская антиутопия о мире, где стабильность перестала защищать человека и стала способом удерживать его внутри стены. Это Том I трилогии МОНОЛИТ: стадия затвердевшей формы, калибровки памяти и первой внутренней трещины.
```

2. Сохранить case-file block:
   - обложку;
   - `Дело / Том I`;
   - primary signal;
   - protocol line;
   - verified buttons.

3. Заменить текущий один длинный `Описание` block на архитектуру:
   - `О книге`;
   - `Без спойлеров`;
   - `Художественно-исследовательская рамка`;
   - `Темы / смысловые узлы`;
   - `Для кого эта книга`;
   - `Место в трилогии`;
   - `Где читать / издания`;
   - `Что важно не перепутать`.

4. Использовать 6-node themes grid:
   - Стабильность;
   - Память;
   - Шум;
   - Исправление;
   - Департамент Смыслов;
   - Трещина.

5. Использовать verified links only:

```text
https://play.google.com/store/books/details?id=S__VEQAAQBAJ
https://www.amazon.com/dp/B0H18H1CFR
https://www.ashraellen.com/ru/books/monolith/
```

6. Add only minimal page-local CSS in a future implementation if needed. Do not edit shared CSS.

---

## 4. Applied MS decisions

Applied decisions from current command:

1. Colder hero lead selected.
2. Primary signal preserved:

```text
Бетон начинается не со стены.
Он начинается с привычки называть тюрьму стабильностью.
```

3. Existing case-file atmosphere preserved.
4. Full `О книге` selected as primary.
5. Prose `Без спойлеров` selected.
6. Full research-frame block selected if readable.
7. 6-node themes version selected.
8. Full reader block selected unless too dense.
9. Shorter trilogy-place block selected.
10. Verified links only.
11. Full boundary block compactly.
12. No metadata, JSON-LD, social metadata, sitemap, shared CSS or script changes.

---

## 5. Remaining decisions for MS

Before a future implementation command, MS should review:

1. Whether full `О книге` and full research-frame together are readable on the rendered page.
2. Whether `Где читать / издания` should repeat the same CTA buttons already present in the hero case block.
3. Whether `Что важно не перепутать` should stay compact prose or become compact cards.
4. Whether minimal page-local CSS additions are acceptable in the future implementation command.
5. Whether existing final lines should remain near the bottom or be redistributed:
   - `Бетон боится только тех, кто перестал считать себя его частью.`
   - `Издание выпущено в условиях экстерриториальности для сохранения целостности Сигнала.`
6. Whether the future implementation should leave the existing scripts untouched or explicitly authorize a separate technical cleanup. Current `DRAFT_007` does not include script changes.

---

## 6. Risks

1. The future page may become text-heavy if all full prose blocks are used without visual spacing.
2. The page must not become a grant-like research statement.
3. The page must not inherit the warmer tone of `Сияние` / `Сампо`.
4. The page must not repeat the MONOLITH series page too mechanically.
5. The bottom edition block may duplicate hero CTAs.
6. Script cleanup must not be smuggled into this editorial HTML plan unless a future command explicitly authorizes it.
7. Metadata and JSON-LD modernization should remain out of scope unless separately commanded.

---

## 7. Clear next step

Next step: MS should review:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_007_HTML_Draft_Patch.md
```

After MS review, a separate explicit implementation command is required before editing:

```text
ru/books/monolith/beton/index.html
```

---

## 8. Explicit statement that live site was not edited

Live site не редактировался.

The current target page was read only:

```text
ru/books/monolith/beton/index.html
```

The following files were not edited:

```text
ru/books/monolith/beton/index.html
ru/books/monolith/index.html
ru/books/monolith/sludge/index.html
ru/books/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
assets/books.css
sitemap.xml
```

No metadata, JSON-LD or social metadata was edited.  
No shared CSS was edited.  
No scripts were created or run.  
No live HTML implementation was performed.  
Work completed only by creating the two APM files listed above.
