# Public Thoughts Multilingual Rollout — опорные решения

Дата фиксации: 2026-06-23  
Проект: Ashraellen MainSite / Ashraellen.com  
Репозиторий сайта: `Ashraellen/ashraellen`  
Репозиторий памяти: `Ashraellen/apm`

## Назначение файла

Этот файл является опорной памяткой для новых чатов и будущих проходов по сайту Ashraellen.com.

Его задача — зафиксировать решения, принятые при создании многоязычного слоя `Опорных мыслей` / `Public Thoughts` 0001–0012, чтобы следующему чату не нужно было заново выяснять архитектуру, термины, правила ротации, пути файлов, отношение к старому слою `formulas` и принципы транскреации.

Если новый чат продолжает работу над сайтом, этот файл нужно читать как один из главных источников контекста.

## Завершённый результат

Многоязычный слой опорных мыслей 0001–0012 создан и принят пользователем.

Пользователь выборочно проверил сайт и подтвердил:

```text
Всё хорошо.
```

Готовы все языки проекта, представленные в навигации сайта:

```text
RU, EN, PL, UK, BE, PT, ES, FR, DE
```

## Основная архитектура слоя

Для каждого языка действует одна и та же структура:

```text
/[lang]/public/
→ живая витрина текущей шестёрки опорных мыслей

/[lang]/public/thoughts/
→ самая свежая завершённая дуга, ушедшая с витрины

/[lang]/public/thoughts/arcs/
→ отдельные страницы опорных мыслей
```

На момент фиксации:

```text
/[lang]/public/
→ 0007–0012

/[lang]/public/thoughts/
→ дуга 0001–0006

/[lang]/public/thoughts/arcs/
→ отдельные страницы 0001–0012
```

## Правило ротации будущих дуг

Когда появится новая шестёрка 0013–0018:

```text
/[lang]/public/
→ 0013–0018

/[lang]/public/thoughts/
→ 0007–0012

/[lang]/public/thoughts/index-0001.html
→ 0001–0006
```

При следующей ротации:

```text
/[lang]/public/
→ 0019–0024

/[lang]/public/thoughts/
→ 0013–0018

/[lang]/public/thoughts/index-0002.html
→ 0007–0012

/[lang]/public/thoughts/index-0001.html
→ 0001–0006
```

Правило:

1. `index.html` внутри `/[lang]/public/thoughts/` всегда самая свежая завершённая дуга.
2. Старые завершённые дуги уходят в номерные архивы `index-0001.html`, `index-0002.html` и далее.
3. Номерные архивы не перезаписывать.
4. `/[lang]/public/` всегда показывает текущую живую шестёрку.

## Старый слой formulas

Старый слой формул не удалять и не ломать:

```text
/[lang]/public/formulas/...
```

Он считается историческим слоем и может продолжать существовать для старых ссылок, поисковиков и прежней структуры сайта.

Новая правильная архитектура идёт через:

```text
/[lang]/public/thoughts/
/[lang]/public/thoughts/arcs/
```

Не переносить старые изображения и страницы грубо. Старый слой должен оставаться работоспособным, если нет отдельного решения пользователя.

## Ассеты изображений

Старые изображения формул остаются здесь:

```text
assets/public-formulas/
```

Новый слой опорных мыслей использует:

```text
assets/thoughts/
```

Файлы изображений 0001–0012:

```text
assets/thoughts/0001-cheerfulness.jpg
assets/thoughts/0002-still-the-same.jpg
assets/thoughts/0003-let-go.jpg
assets/thoughts/0004-mortality-awakens.jpg
assets/thoughts/0005-on-your-own.jpg
assets/thoughts/0006-insight.jpg
assets/thoughts/0007-empty-chair.jpg
assets/thoughts/0008-generalization.jpg
assets/thoughts/0009-where-life-stopped.jpg
assets/thoughts/0010-dirty-cup.jpg
assets/thoughts/0011-do-not-regret.jpg
assets/thoughts/0012-close-the-book.jpg
```

Новые страницы `thoughts` должны ссылаться именно на `assets/thoughts/`.

Старые страницы `formulas` должны продолжать ссылаться на `assets/public-formulas/`, если не принято другое решение.

## Нумерация

Формат нумерации:

```text
0001
0002
...
0012
...
0100
```

Отдельные страницы мыслей:

```text
/[lang]/public/thoughts/arcs/0001-cheerfulness.html
/[lang]/public/thoughts/arcs/0002-still-the-same.html
...
/[lang]/public/thoughts/arcs/0012-close-the-book.html
```

Не использовать паттерн `arc-0001.html` для отдельной мысли. Это звучит как страница дуги, а не как страница отдельной опорной мысли.

## Текущие страницы 0001–0012

В каждом языке созданы отдельные страницы:

```text
0001-cheerfulness.html
0002-still-the-same.html
0003-let-go.html
0004-mortality-awakens.html
0005-on-your-own.html
0006-insight.html
0007-empty-chair.html
0008-generalization.html
0009-where-life-stopped.html
0010-dirty-cup.html
0011-do-not-regret.html
0012-close-the-book.html
```

Текущие темы:

```text
0001 — Весёлость / Cheerfulness
0002 — Всё те же силы / Still the same forces
0003 — Отпустить / Let go
0004 — Конечность пробуждает / Mortality awakens
0005 — Самостоятельность перед страхом / On your own
0006 — Прозрение / Insight
0007 — Пустой стул / Empty chair
0008 — Обобщение вместо наблюдения / Generalization instead of observation
0009 — Где ты перестал быть живым / Where life stopped
0010 — Грязная чашка / Dirty cup
0011 — Не сожалей / Do not regret
0012 — Когда закрыть книгу / Close the book
```

## Терминология по языкам

Русский:

```text
Опорные мысли
Опорная мысль 0001
Дуга опорных мыслей
```

English:

```text
Support Thoughts
Support Thought 0001
Support-thought arc
```

Polish:

```text
Myśli oparcia
Myśl oparcia 0001
Łuk myśli oparcia
```

Ukrainian:

```text
Опорні думки
Опорна думка 0001
Дуга опорних думок
```

Belarusian:

```text
Апорныя думкі
Апорная думка 0001
Дуга апорных думак
```

Portuguese:

```text
Pensamentos de apoio
Pensamento de apoio 0001
Arco de pensamentos de apoio
```

Spanish:

```text
Pensamientos de apoyo
Pensamiento de apoyo 0001
Arco de pensamientos de apoyo
```

French:

```text
Pensées d’appui
Pensée d’appui 0001
Arc de pensées d’appui
```

German:

```text
Stützgedanken
Stützgedanke 0001
Bogen der Stützgedanken
```

## Важное правило текста

Русский мастер-текст опорной мысли неприкосновенен.

Нельзя без прямого запроса пользователя:

1. сокращать полный текст;
2. сглаживать авторский ритм;
3. убирать повторы;
4. переписывать финалы;
5. делать текст более коммерческим, мотивационным или коучинговым;
6. менять философскую плотность;
7. исправлять авторскую интонацию ради литературной гладкости.

Если пользователь даёт новую опорную мысль как `Полный текст`, этот текст сохраняется как авторский оригинал.

К нему можно добавлять:

```text
Смысл
Почему выбрано
Исследовательская заметка
```

но сам `Полный текст` не менять.

## Принцип транскреации

Для языков проекта используется не механический перевод, а литературная транскреация.

Цель:

1. сохранить смысл;
2. сохранить дыхание;
3. сохранить ритм;
4. сохранить образ;
5. сохранить удар финальной фразы;
6. не превращать текст в мотивационный контент;
7. не упрощать философскую плотность;
8. не делать текст гладким ценой авторского давления;
9. не добавлять чужие смыслы;
10. не сжимать и не урезать.

Русский слой остаётся мастер-слоем смысла.

Английский может использоваться как дополнительный рабочий мост для остальных языков, но при сомнении возвращаться к русскому оригиналу.

## Правило для 0010 — `Грязная чашка`

Пользователь уточнил:

```text
0010 `Грязная чашка` — это вольная авторская интерпретация знаменитой сказки `Алиса в стране чудес`.
Оригинальный эпизод изменён и дополнен для закрепления мысли.
```

Это пояснение должно быть отражено в исследовательской заметке на каждом языке.

Не подавать 0010 как пересказ оригинала. Это авторская интерпретация мотива чаепития.

## Острые места и безопасная формулировка

В 0011 есть образ, который в разных языках был передан мягче, чтобы избежать лишней графичности и платформенных фильтров, не теряя смысла.

Использованные безопасные варианты:

```text
EN: harm themselves
PL: skrzywdzić siebie
UK: нашкодити собі
BE: нашкодзіць сабе
PT: se ferir
ES: hacerse daño
FR: se blesser
DE: sich selbst verletzen
```

Смысл сохраняется: человек часто мечтает из раны, страха, зависти, одиночества или желания доказать свою ценность и мог бы этой мечтой себе навредить.

## Текущий статус по языкам

Все языки проекта получили слой опорных мыслей 0001–0012:

```text
RU — готово и принято
EN — готово
PL — готово
UK — готово
BE — готово
PT — готово
ES — готово
FR — готово
DE — готово
```

Пользователь выборочно проверил сайт и подтвердил, что всё хорошо.

## Session logs по языкам

В памяти проекта созданы session logs:

```text
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_RU_Public_Thoughts_0007_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_EN_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_PL_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_UK_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_BE_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_PT_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_ES_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_FR_Public_Thoughts_0001_0012_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_DE_Public_Thoughts_0001_0012_2026-06-23.md
```

Также важны:

```text
Projects/Ashraellen/MainSite/Working_Notes/RU_Public_Thoughts_Rotating_Architecture_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_RU_Public_Thoughts_Build_2026-06-23.md
Projects/Ashraellen/MainSite/Session_Logs/MS_SL_RU_Public_Thoughts_Assets_2026-06-23.md
```

## Что не трогать без отдельного решения

Не удалять и не ломать:

```text
/[lang]/public/formulas/...
/[lang]/public/thoughts/01-...
/[lang]/public/thoughts/02-...
/[lang]/public/thoughts/arcs/arc-0001.html
assets/public-formulas/
```

Некоторые старые или временные страницы могут существовать исторически. Их не развивать как основной паттерн, но и не удалять без отдельного решения пользователя.

## Будущая работа

Наиболее логичный следующий этап:

```text
1. Общий аудит ссылок и отображения по всем языкам.
2. Проверка мобильного вида.
3. Проверка картинок и alt-текстов.
4. Проверка hreflang/canonical.
5. Проверка, что старые formulas не сломаны.
6. Подготовка новой шестёрки 0013–0018.
7. Ротация текущей витрины по установленному правилу.
```

Если новый чат получает задачу `сделать 0013–0018`, он должен:

1. взять русский мастер-текст от пользователя;
2. не менять `Полный текст`;
3. создать русские страницы 0013–0018;
4. обновить `/ru/public/`;
5. перенести 0007–0012 в `/ru/public/thoughts/index.html`;
6. перенести старую 0001–0006 в `/ru/public/thoughts/index-0001.html`;
7. затем делать языковые проходы по EN, PL, UK, BE, PT, ES, FR, DE;
8. фиксировать каждый языковой проход в session log;
9. обновлять `Projects/Ashraellen/MainSite/INDEX.md`.

## Название завершённого чата

Рекомендуемое название чата, где была сделана эта работа:

```text
MainSite — Public Thoughts Multilingual Rollout 0001–0012
```

Русский вариант:

```text
Ashraellen.com — многоязычный слой опорных мыслей 0001–0012
```

## Краткая памятка для нового чата

Если нужно начать новый чат, можно дать ему такой стартовый текст:

```text
Работаем над сайтом Ashraellen.com.

Прочитай в APM файл:
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md

Важно:
- слой опорных мыслей 0001–0012 уже создан на RU, EN, PL, UK, BE, PT, ES, FR, DE;
- архитектура: /[lang]/public/, /[lang]/public/thoughts/, /[lang]/public/thoughts/arcs/;
- старый слой /[lang]/public/formulas/ не трогать;
- русские Полные тексты не менять и не сокращать;
- новые языки делать транскреацией, не механическим переводом;
- 0010 `Грязная чашка` — вольная авторская интерпретация мотива чаепития из `Алисы в стране чудес`;
- следующая задача: аудит, ротация или новая шестёрка 0013–0018.
```
