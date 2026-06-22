# Prompt — request site memory from older chats

Status: reusable prompt  
Created: 2026-06-22  
Purpose: paste into any older chat where website work may have happened

## Copy-paste prompt

```text
Прошу тебя собрать всю информацию из этого чата, связанную с сайтом Ashraellen / ashraellen.com.

Мне нужен не пересказ всего чата, а аккуратный файл-памятка именно по сайту.

Собери, пожалуйста:

1. Какие решения по сайту были приняты в этом чате.
2. Какие страницы, разделы, языковые версии, лендинги, тексты или структуры мы обсуждали или создавали.
3. Какие файлы, пути, репозитории, URL, GitHub Pages, технические решения, редиректы, sitemap, JSON-LD, SEO, llms.txt, PWA, автоопределение языка или кнопки выбора языка упоминались.
4. Какие тексты были написаны или утверждены для сайта.
5. Какие решения касались позиционирования Ashraellen: artistic research, literary-philosophical research, practice-based cultural research, multilingual public archive, grant-facing presentation и т. п.
6. Какие решения касались языков: русский, английский, польский, финский и другие версии.
7. Что уже было сделано/создано/обновлено, а что осталось только идеей.
8. Что было отвергнуто, признано устаревшим или заменено другим решением.
9. Какие открытые задачи остались после этого чата.
10. Какие файлы лучше потом перенести в общий архив сайта.

Важно:
- Не начинай общую стратегию заново.
- Не придумывай новые решения.
- Не улучшай задним числом.
- Разделяй: "принято", "обсуждалось", "сделано", "отложено", "устарело", "нужно проверить".
- Если есть точные пути файлов, названия страниц, URL или названия репозиториев — обязательно укажи.
- Если есть готовые фрагменты текста для сайта — приведи их или кратко укажи, где они находятся.

Сделай результат в формате Markdown-файла.

Название файла предложи по шаблону:
MainSite_ChatMemory_YYYY-MM-DD_short-topic.md

Структура файла:

# MainSite Chat Memory — [краткая тема]

Source chat: [название/тема чата, если понятно]
Date of extraction: [сегодняшняя дата]
Status: raw import / needs sorting

## 1. Краткое резюме

## 2. Принятые решения

## 3. Уже сделано / создано / обновлено

## 4. Страницы, разделы и структура

## 5. Языки и переводы

## 6. Технические решения

## 7. SEO / metadata / AI-readable context

## 8. Grant / institutional positioning

## 9. Готовые тексты или важные формулировки

## 10. Открытые задачи

## 11. Устаревшее / отвергнутое / сомнительное

## 12. Что перенести в MASTER_MainSite.md

## 13. Что требует проверки

После этого дай мне готовый файл .md для скачивания или текст, который можно сохранить как .md.
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
