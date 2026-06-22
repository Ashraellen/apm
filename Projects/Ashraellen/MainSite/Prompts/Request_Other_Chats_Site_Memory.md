# Prompt — request site memory from older chats

Status: reusable prompt  
Created: 2026-06-22  
Updated: 2026-06-22  
Purpose: paste into any older chat where website work may have happened

## File naming rule

Use short numbered filenames:

`MS_01.md`, `MS_02.md`, `MS_03.md`, etc.

Because different chats cannot see one another, the user should provide the number before pasting the prompt.

Example:

`Номер файла: 01`

If no number is provided, the chat should use `MS_XX.md` and clearly tell the user to replace `XX` with the correct number before saving.

## Copy-paste prompt

```text
Номер файла: 01

Прошу тебя собрать из этого чата всю информацию, связанную с сайтом Ashraellen / ashraellen.com.

Нужна не история всего чата, а короткая рабочая памятка для общего архива сайта.

Создай Markdown-файл с коротким именем:
MS_01.md

Если в строке "Номер файла" указан другой номер, используй его: MS_02.md, MS_03.md и так далее.
Если номер не указан, используй временное имя MS_XX.md и отдельно напомни мне заменить XX на правильный номер.

Собери только то, что относится к сайту:

1. Принятые решения.
2. Что было создано, обновлено или подготовлено.
3. Страницы, разделы, структура сайта.
4. Языки и переводы.
5. Технические решения: GitHub Pages, пути, URL, редиректы, sitemap, JSON-LD, SEO, llms.txt, PWA, автоопределение языка, ручной выбор языка.
6. Позиционирование Ashraellen для сайта: artistic research, literary-philosophical research, practice-based cultural research, multilingual public archive, grant-facing presentation.
7. Готовые тексты или важные формулировки.
8. Открытые задачи.
9. Устаревшее, отвергнутое или сомнительное.
10. Что потом нужно перенести в общий MASTER_MainSite.md.

Важно:
- Не начинай стратегию заново.
- Не придумывай новые решения.
- Не улучшай задним числом.
- Разделяй: "принято", "сделано", "обсуждалось", "отложено", "устарело", "нужно проверить".
- Если есть точные пути файлов, названия страниц, URL или репозитории — укажи.
- Если в чате есть готовые тексты для сайта — приведи их или укажи, где они находятся.

Структура файла:

# MS_01 — MainSite chat memory

Source chat: [тема/название чата, если понятно]
Date of extraction: [сегодняшняя дата]
Status: raw import / needs sorting

## 1. Summary

## 2. Accepted decisions

## 3. Done / created / updated

## 4. Pages and structure

## 5. Languages

## 6. Technical notes

## 7. Positioning / grants

## 8. Ready text fragments

## 9. Open tasks

## 10. Outdated / rejected / uncertain

## 11. Move to MASTER_MainSite.md

После этого дай мне готовый .md файл для скачивания или полный текст файла, который можно сохранить как .md.
```

## Where to place resulting files

All resulting files from older chats should be stored in:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/`

After sorting, confirmed material can be moved into:

- `MASTER_MainSite.md`;
- `Decisions/`;
- `Content/`;
- `Languages/`;
- `Technical/`;
- `Grant_Positioning/`;
- `Tasks/`.
