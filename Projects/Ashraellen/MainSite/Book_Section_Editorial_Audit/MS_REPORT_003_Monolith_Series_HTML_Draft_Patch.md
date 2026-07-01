# MS REPORT 003 — MONOLITH Series HTML Draft / Patch Plan

Date: 2026-07-01  
Project: Ashraellen / MainSite / Book Section Editorial Audit  
Status: short handoff report for MS

---

## 1. Status

`COMMAND_003_Monolith_Series_HTML_Draft_Patch.md` выполнен.

Создан HTML-draft / patch plan для будущего расширения страницы:

```text
ru/books/monolith/index.html
```

Live site не изменялся. HTML-файлы не редактировались.

---

## 2. Files created

Основной HTML-draft / patch plan:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_003_Monolith_Series_HTML_Draft_Patch.md
```

Короткий отчёт для MS:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_003_Monolith_Series_HTML_Draft_Patch.md
```

---

## 3. Summary of proposed HTML changes

В `DRAFT_003` подготовлен точный план будущего HTML-внедрения для `MONOLITH` series page.

Предложено:

1. Расширить hero:
   - добавить kicker `Протокол распада социальной материи / БЕТОН — ЖИЖА — ГАЗ`;
   - заменить lead на литературно-философскую антиутопическую формулу;
   - вынести главный сигнал серии выше: `Система боится не бунта. Она боится первой трещины.`;
   - добавить CTA: `Тома трилогии`, `Карта распада`, `Что важно не перепутать`.

2. Заменить текущий блок `Серия` на `Что такое МОНОЛИТ`.

3. Сохранить блок `Тома`, добавив `id="volumes"` и отметив возможную будущую статическую замену `href="#"` на прямые ссылки.

4. Добавить новые блоки:
   - `Художественно-исследовательская рамка`;
   - `Карта распада`;
   - `Для кого этот проект`;
   - `Что важно не перепутать`.

5. Предложить минимальные local CSS additions внутри существующего inline `<style>`, не трогая общий `assets/books.css`.

6. Сохранить главный голос страницы: холод, протокол, контроль, стена, трещина, распад, разгерметизация.

---

## 4. Decisions requiring MS review

MS should review and decide:

1. Использовать полную или medium-версию блока `Что такое МОНОЛИТ`.
2. Использовать 9-node или 6-node версию `Карты распада`.
3. Оставить полный блок `Что важно не перепутать` или взять короткий fallback.
4. Что делать с финальным блоком `Фраза серии` после переноса главного сигнала в hero:
   - оставить как есть;
   - удалить;
   - заменить на вариант: `Распад начинается не тогда, когда рушится стена...`.
5. Подтвердить, можно ли в будущей HTML-фазе заменить `href="#"` в кнопках `БЕТОН` и `ЖИЖА` на статические URL.
6. Подтвердить, что metadata / JSON-LD остаются нетронутыми на ближайшем implementation-step.

---

## 5. Risks

1. Страница может стать длинной и тяжёлой на мобильных устройствах.
2. Полная версия `Что важно не перепутать` может звучать слишком объяснительно, если будет стоять без визуального воздуха.
3. Дублирование сигнала `Система боится не бунта...` в hero и финале может быть сильным ритуальным повтором, а может стать избыточным.
4. Партнёрский блок нужно держать коротким, чтобы не уйти в grant/institutional tone.
5. Нельзя переносить тон `Сияния` в `МОНОЛИТ`: архитектура да, температура нет.
6. Нельзя превращать patch plan в несанкционированную live-site правку.

---

## 6. Clear next step

Следующий шаг: MS review основного draft:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_003_Monolith_Series_HTML_Draft_Patch.md
```

После review нужен отдельный explicit command на фактическую HTML-правку:

```text
ru/books/monolith/index.html
```

До такого command live-site файл не менять.

---

## 7. Explicit statement that live site was not edited

Live site не редактировался.

Не изменялись:

```text
ru/books/monolith/index.html
ru/books/monolith/beton/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
ru/books/index.html
assets/books.css
sitemap.xml
```

Не создавались SEO-скрипты.  
Не запускались metadata repair scripts.  
Не добавлялся client-side JS для content / SEO / metadata / social metadata.  
Работа завершена только APM-файлами, указанными выше.
