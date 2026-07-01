# COMMAND 009 — BETON Compression + Selected Fragment

Date: 2026-07-02
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: limited live-site implementation

## Mission

Apply a targeted compression cleanup and add a selected fragment to the Russian BETON page:

```text
ru/books/monolith/beton/index.html
```

This command authorizes editing only that one live-site file.

## Read first

Read:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_006_Beton_Individual_Book_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_007_HTML_Draft_Patch.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_008_HTML_Implementation.md
```

Then read the current live file:

```text
ru/books/monolith/beton/index.html
```

## Authorized edit

Only this live-site file may be edited:

```text
ru/books/monolith/beton/index.html
```

## Files and areas not authorized

Do not edit:

```text
sitemap.xml
assets/books.css
ru/books/index.html
ru/books/monolith/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

Do not change:

```text
metadata
JSON-LD
social metadata
shared CSS
scripts
```

Do not create or run scripts.

## Required changes

### 1. Compress visible text

Compress the visible prose across the BETON page.

Goal: keep only the strongest essence.

Do not remove the page architecture created in COMMAND 008.
Keep the existing sections, but make the prose tighter where it feels explanatory or repetitive.

Important: this is not a rewrite into a different tone. Keep BETON cold, procedural, compressed, concrete-like.

Priority areas for compression:

- `О книге`;
- `Без спойлеров`;
- `Художественно-исследовательская рамка`;
- `Для кого эта книга`;
- `Что важно не перепутать`.

Do not compress the selected fragment.

### 2. Clean `Где читать / издания`

In the section `Где читать / издания`, remove the explanatory paragraphs.

Remove this visible text if present:

```text
Русская версия БЕТОНА доступна в Google Play Books.
Английская версия доступна на Amazon.
Страница серии МОНОЛИТ открывает общий контекст трилогии: БЕТОН, ЖИЖА, ГАЗ.
```

Leave only the CTA buttons with verified links:

```text
https://play.google.com/store/books/details?id=S__VEQAAQBAJ
https://www.amazon.com/dp/B0H18H1CFR
https://www.ashraellen.com/ru/books/monolith/
```

### 3. Add selected fragment

Add a new section after the `Дело` block and before `О книге`.

Section title:

```text
Избранный фрагмент
```

Section note:

```text
Глава 9 / § 9.1
```

Visible intro before the collapsible text:

```text
Глава 9. Протокол «Гордость»
§ 9.1. Лучший клей для общества
```

Then add a short, non-spoiler orientation line:

```text
Фрагмент показывает один из механизмов БЕТОНА: как боль превращают в лозунг, вину — в социальный клей, а человеческую утрату — в управляемый образ стабильности.
```

Button / summary text:

```text
Открыть фрагмент
```

Use native HTML `<details>` / `<summary>` for the collapsible fragment.
Do not use JavaScript.

Important: insert the fragment text fully, exactly as supplied by the user in the current MS conversation.
Do not cut it.
Do not summarize it.
Do not soften it.
Do not paraphrase it.
Do not translate it.
Do not correct style unless strictly necessary for HTML escaping.

The selected fragment is:

```text
Глава 9. Протокол «Гордость»
§ 9.1. Лучший клей для общества
Утро в Департаменте смыслов началось с «белого кода». Это означало, что все текущие задачи отменяются, а лифты блокируются на вход до особого распоряжения. В воздухе висел тяжелый запах озона — климат-контроль работал на пределе, выжигая малейшие следы человеческой тревоги.
Марк стоял у панорамного окна, заложив руки за спину. Его силуэт на фоне утреннего города казался вырезанным из черного картона.
— Нам прилетел «социальный заказ» из самой Верхушки, Антон, — произнес он, не оборачиваясь. — Называется «Протокол Гордость». Проблема в том, что наше население начало... брезговать. Возвращенцы из Зон Контакта вызывают у граждан «эстетическую фрустрацию». Понимаешь? Они портят картинку стабильности.
Антон сел за стол, чувствуя, как вчерашняя двойная доза «баланса» превратила его мозг в идеально чистое зеркало.
— Они калеки, Марк. Калека — это визуальный шум. Это напоминание о том, что бетон может крошиться.
— Именно! — Марк резко развернулся. — Поэтому наша задача — превратить их из «пострадавших» в «объекты поклонения». Но так, чтобы к ним не хотелось подходить слишком близко. Святость на расстоянии. Дистанционное обожание.
На центральном голографическом столе вспыхнули варианты слоганов, которые уже набросали нейросети департамента. Антон листал их, и внутри него шевельнулось забытое чувство — нечто среднее между тошнотой и истерическим смехом.
«Твоя рана — это орден, который нельзя снять».
«Отсутствие конечности — присутствие духа».
«Он отдал часть себя, чтобы ты остался целым».
— Слишком пафосно, — отрезал Марк. — Люди чувствуют подвох. Нам нужно что-то... прикладное. Вот, посмотри на предложение из сектора Б.
На экране появилось изображение: мужчина на инновационных протезах из матового черного полимера. Он стоял на фоне заката, а рядом — слоган:
«МЕХАНИКА ПОДВИГА: НОВАЯ СТАЛЬ В СТАРОЙ КРОВИ».
— Они хотят продавать их как киборгов? — Антон поднял бровь.
— Как эволюцию! — воодушевился Марк. — Мы скажем, что металл надежнее кости.
Антон вспомнил цифры из отчетов, которые видел мельком: большинство этих «улучшенных людей» нанимались в Зоны Контакта просто потому, что их кредитный рейтинг упал ниже плинтуса.
— Марк, — осторожно начал он, — но ведь все знают, что они шли туда за выплатами. У нас даже есть статистика: 89% мотивации — это деньги. Как мы прикрутим к этому «святость»?
Марк посмотрел на него как на ребенка.
— Антон, не путай факт и смысл. Факт — это деньги. Смысл — это жертва. Мы просто меняем полярность. Он не «продал ногу за миллион», он «инвестировал свою плоть в стабильность твоего завтра». И не волнуйся за восприятие. Ведомство твоей супруги уже запустило скрипты «Тихого принятия» во всех домохозяйствах. Лика сегодня утром подтвердила: уровень сопротивляемости в твоем секторе минимален. Мы работаем в паре.
Антон замер. Значит, Лика знала. Пока она гладила его по голове ночью, она уже вшивала в его подсознание готовность принять этот абсурд.
В отделе начался мозговой штурм. Сотрудники, похожие на белых призраков в своих накрахмаленных рубашках, выкрикивали идеи, соревнуясь в уровне цинизма, который они называли «профессиональной отстраненностью».
— Предлагаю визуальный ряд «Ангелы без крыльев»! — крикнула Майя из отдела визуализации. — Сделаем им золотые костыли на плакатах. Чтобы блестели. Костыль как скипетр!
— Глупо, — парировал кто-то. — Костыль — это неудобство. Нужно продвигать идею, что им вообще не нужны ноги. «Герой выше земного притяжения».
Антон смотрел на этот парад абсурда. Он понимал, что под «сталью» и «золотом» скрываются люди, которые видели и делали вещи, несовместимые с этим глянцевым офисом.
— Нам нужно изменить угол зрения, — наконец сказал он. — Сделать так, чтобы обычный человек чувствовал себя виноватым за то, что он цел.
Марк замер. В его глазах вспыхнул фанатичный огонек.
— Вина... Гениально, Антон! Вина — лучший клей для общества. «Твоя целостность оплачена его болью». Записывай это!
```

## Style / layout notes

The selected fragment is long. It must be collapsed by default.

Suggested structure:

```html
<section id="selected-fragment" class="list">
  <div class="list-header"><h2>Избранный фрагмент</h2><p class="note">Глава 9 / § 9.1</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p class="protocol">Глава 9. Протокол «Гордость»<br>§ 9.1. Лучший клей для общества</p>
        <p>Фрагмент показывает...</p>
        <details class="beton-fragment">
          <summary>Открыть фрагмент</summary>
          <div class="beton-fragment-body">
            ... full fragment as paragraphs ...
          </div>
        </details>
      </div>
    </li>
  </ul>
</section>
```

Add only minimal page-local CSS inside the existing inline style block if necessary for:

```text
beton-fragment
beton-fragment-body
```

Do not edit `assets/books.css`.

## Verification

After editing, verify:

1. Only `ru/books/monolith/beton/index.html` changed in the live-site repository.
2. The `Избранный фрагмент` section exists after `Дело` and before `О книге`.
3. The fragment is collapsed by default using native HTML `<details>`.
4. The fragment text is complete and not summarized.
5. `Где читать / издания` contains only CTA buttons, no explanatory paragraphs.
6. Main page prose is visibly compressed.
7. The cover, primary signal, protocol line, verified links and final signal remain present.
8. `sitemap.xml` was not edited.
9. `assets/books.css` was not edited.
10. metadata, JSON-LD, social metadata and scripts were not changed.
11. No scripts were created or run.

## Required MS report

After implementation, create:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_009_Beton_Compression_Selected_Fragment.md
```

The report must include:

1. Status.
2. Live-site commit SHA.
3. Exact files edited.
4. Summary of compression changes.
5. Confirmation that the selected fragment was inserted fully and collapsed by default.
6. Confirmation that `Где читать / издания` now contains only buttons.
7. Confirmation that forbidden files and areas were not edited.
8. Any deviations from this command and why.
9. Clear next step.

## Boundary

This command authorizes only the one live-site edit named above and the APM report.

A separate command is required before editing any other page or any technical / metadata area.
