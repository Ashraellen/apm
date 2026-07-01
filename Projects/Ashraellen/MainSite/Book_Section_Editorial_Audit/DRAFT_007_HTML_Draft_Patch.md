# DRAFT 007 — BETON HTML Draft / Patch Plan

Date: 2026-07-01  
Project: Ashraellen / MainSite / Book Section Editorial Audit  
Status: HTML draft / patch plan only  
Command source: `COMMAND_007_HTML_Draft_Patch.md`

---

## 1. Status and scope

Этот документ подготавливает HTML draft / patch plan для будущего расширения индивидуальной страницы книги:

```text
ru/books/monolith/beton/index.html
```

Это не implementation task. Live site не редактировался. HTML-файлы не изменялись.

Задача документа: перевести `DRAFT_006_Beton_Individual_Book_Editorial_Expansion.md` и решения MS из текущего command в точный план будущей HTML-правки.

Этот draft покрывает только страницу `БЕТОН`. Он не касается `ЖИЖА`, страницы серии `МОНОЛИТ`, общего каталога книг, `Сияния`, `Сампо`, metadata, JSON-LD, social metadata, sitemap, shared CSS или scripts.

---

## 2. Source files read

Прочитаны и использованы:

```text
REPORT_001_Book_Section_Audit_Plan.md
DRAFT_006_Beton_Individual_Book_Editorial_Expansion.md
MS_REPORT_006_Beton_Individual_Book_Editorial_Expansion.md
ru/books/monolith/beton/index.html
```

Из `REPORT_001` взят диагноз: текущая страница `БЕТОН` имеет сильный hero, дело, обложку, verified CTA и атмосферное описание, но ей не хватает структуры индивидуальной книжной страницы: `Без спойлеров`, карта тем, художественно-исследовательская рамка, `Для кого`, `Что важно не перепутать`, `Место в трилогии`, `Покупка / editions`.

Из `DRAFT_006` взяты public-facing тексты для `О книге`, `Без спойлеров`, research frame, 6-node themes, reader block, shorter trilogy-place block, verified links and boundaries.

Из текущего live source подтверждены existing elements to preserve:

- `h1`: `БЕТОН`;
- current lead: `Первый том трилогии «МОНОЛИТ».`;
- current case block `Дело / Том I`;
- cover path: `../../../../assets/covers/beton-ru.webp`;
- primary signal: `Бетон начинается не со стены. Он начинается с привычки называть тюрьму стабильностью.`;
- protocol line: `ДЕЛО № 2026-001B. Индекс: 6666548A. СТАТУС: Совершенно секретно.`;
- verified links:
  - `https://play.google.com/store/books/details?id=S__VEQAAQBAJ`;
  - `https://www.amazon.com/dp/B0H18H1CFR`;
  - `https://www.ashraellen.com/ru/books/monolith/`.

---

## 3. MS decisions applied in this draft

The current command fixes the following decisions:

1. Use the colder hero lead from `DRAFT_006`.
2. Keep the primary signal identified in the editorial draft.
3. Keep the existing case-file atmosphere.
4. Use full `О книге` as primary.
5. Use prose `Без спойлеров`.
6. Use full research-frame block if readable.
7. Use the 6-node themes version.
8. Use full reader block unless too dense.
9. Use the shorter trilogy-place block.
10. Use verified links only.
11. Use full boundary block compactly.
12. Do not change metadata, JSON-LD, social metadata, sitemap, shared CSS, or scripts.

Practical interpretation: the future implementation should be a visible-content expansion only. It should not become a technical cleanup or SEO repair task.

---

## 4. Target page diagnosis after reading current HTML

Current `ru/books/monolith/beton/index.html` is compact and atmospheric. The page already has:

- cover-led case block;
- strong quote;
- protocol line;
- direct purchase / reading CTAs;
- long descriptive block;
- seal;
- current metadata and JSON-LD.

The future patch should preserve the case-file pressure, but split the current long `Описание` into a mature page architecture. The main problem is not weak text, but insufficient sectioning.

Do not remove the concrete weight of the page. The goal is not to make `БЕТОН` friendly. The goal is to make it readable, structured and professionally presentable without softening its temperature.

---

## 5. Proposed future page architecture

Inside:

```html
<main class="main"><div class="container">
  ...
</div></main>
```

Recommended future order:

1. Hero / top orientation:
   - `h1`;
   - colder lead.

2. Case block:
   - keep `Дело / Том I`;
   - keep cover;
   - keep primary signal;
   - keep protocol line;
   - keep verified CTA buttons.

3. `О книге`:
   - full version from `DRAFT_006`.

4. `Без спойлеров`:
   - prose version.

5. `Художественно-исследовательская рамка`:
   - full version if readable.

6. `Темы / смысловые узлы`:
   - 6-node version.

7. `Для кого эта книга`:
   - full reader block unless too dense.

8. `Место в трилогии`:
   - shorter version.

9. `Где читать / издания`:
   - verified links only.

10. `Что важно не перепутать`:
   - full boundary block, compactly presented.

11. Existing final signal / edition note / seal:
   - preserve or redistribute existing strong lines;
   - preserve seal.

---

## 6. Section-by-section HTML draft / pseudo-diff

### 6.1. Page-local CSS additions for a later implementation

Current page already has an inline `<style>` block. For a future implementation, add only page-local CSS inside that existing inline style block. Do not edit `assets/books.css`.

Suggested additions:

```html
<style>
  /* existing BETON page styles remain */

  .beton-copy{
    font-size:13px;
    line-height:1.78;
    color:var(--muted);
    max-width:82ch;
  }

  .beton-copy p{
    margin:0 0 12px;
  }

  .beton-copy p:last-child{
    margin-bottom:0;
  }

  .beton-grid{
    display:grid;
    grid-template-columns:repeat(3,minmax(0,1fr));
    gap:14px;
  }

  .beton-card{
    border:1px solid rgba(242,242,244,.12);
    border-radius:14px;
    padding:14px;
    background:rgba(0,0,0,.20);
  }

  .beton-card h3{
    margin:0 0 7px;
    color:var(--fg);
    font-size:15px;
    line-height:1.25;
  }

  .beton-card p{
    margin:0;
    color:var(--muted);
    font-size:13px;
    line-height:1.55;
  }

  .beton-two-col{
    display:grid;
    grid-template-columns:repeat(2,minmax(0,1fr));
    gap:14px;
  }

  .beton-link-box{
    border:1px solid rgba(242,242,244,.12);
    border-radius:14px;
    padding:14px;
    background:rgba(0,0,0,.20);
  }

  .beton-link-box p{
    margin:0 0 12px;
    color:var(--muted);
    font-size:13px;
    line-height:1.55;
  }

  @media(max-width:900px){
    .beton-grid,
    .beton-two-col{
      grid-template-columns:1fr;
    }
  }
</style>
```

Notes:

- This does not touch shared CSS.
- These classes are only for future HTML implementation.
- If an implementation command forbids style changes entirely, use existing `.desc`, `.items`, `.item`, `.body`, `.cta-row` instead.

### 6.2. Replace current lead with colder hero lead

Current:

```html
<h1 class="h1">БЕТОН</h1>
<p class="lead">Первый том трилогии «МОНОЛИТ».</p>
```

Future draft replacement:

```html
<h1 class="h1">БЕТОН</h1>
<p class="lead">БЕТОН — философская антиутопия о мире, где стабильность перестала защищать человека и стала способом удерживать его внутри стены. Это Том I трилогии МОНОЛИТ: стадия затвердевшей формы, калибровки памяти и первой внутренней трещины.</p>
```

Reason:

- Applies MS decision to use colder hero lead.
- Keeps `БЕТОН` as title and `Том I` identity.
- Does not change metadata.

### 6.3. Preserve current case block

Current case block should remain structurally recognizable.

Preserve:

```html
<section class="list">
  <div class="list-header"><h2>Дело</h2><p class="note">Том I</p></div>
  ...
</section>
```

Preserve cover:

```html
<img src="../../../../assets/covers/beton-ru.webp" alt="БЕТОН — обложка" loading="lazy">
```

Preserve primary signal:

```html
<p class="quote-line" style="margin:0 0 12px;">Бетон начинается не со стены. Он начинается с привычки называть тюрьму стабильностью.</p>
```

Preserve protocol:

```html
<p class="protocol">ДЕЛО № 2026-001B. Индекс: 6666548A. СТАТУС: Совершенно секретно.</p>
```

Preserve verified buttons:

```html
<div class="cta-row">
  <a class="btn" href="https://play.google.com/store/books/details?id=S__VEQAAQBAJ" target="_blank" rel="noopener noreferrer">Читать на русском в Google Play Books</a>
  <a class="btn secondary" href="https://www.amazon.com/dp/B0H18H1CFR" target="_blank" rel="noopener noreferrer">English edition on Amazon</a>
  <a id="backSeries" class="btn secondary" href="https://www.ashraellen.com/ru/books/monolith/">Назад к серии</a>
</div>
```

Notes:

- Do not add any new sales links.
- Do not link `ГАЗ`, because no verified page is established here.
- Do not change current scripts in this draft plan; script cleanup is outside this command.

### 6.4. Replace current long `Описание` block with structured `О книге`

Current block starts:

```html
<section class="list"><div class="list-header"><h2>Описание</h2><p class="note">о книге</p></div>...
```

Future draft replacement should start with `О книге` and use full version:

```html
<section id="about-beton" class="list">
  <div class="list-header"><h2>О книге</h2><p class="note">первая стадия МОНОЛИТА</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>БЕТОН открывает трилогию МОНОЛИТ с самого плотного состояния социальной материи. Здесь система ещё кажется прочной, порядок — разумным, а стабильность — единственной формой безопасности. Но именно эта прочность становится первой тюрьмой.</p>
        <p>Это философская антиутопия о мире, где человек больше не сталкивается с открытым насилием как с исключением. Давление становится процедурой. Исправление называется заботой. Удаление шума — защитой будущего. Память превращается в опасный материал, если она хранит то, что не совпадает с гладкой версией реальности.</p>
        <p>В центре книги — Антон, человек, встроенный в механизм калибровки смыслов. Он не просто наблюдает систему со стороны. Он работает внутри неё, говорит её языком, знает её протоколы и слишком долго принимает её холод за норму.</p>
        <p>БЕТОН важен не потому, что показывает уже разрушенный мир. Он фиксирует более ранний и более страшный момент: когда стена ещё стоит, отчёты ещё сходятся, процедуры ещё работают, но внутри человека появляется первая трещина.</p>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Use full `О книге` as required by `COMMAND_007`.
- Do not keep the old `Описание` as a second redundant block. Its strong material is redistributed into the new sections.

### 6.5. Add prose `Без спойлеров`

```html
<section id="spoiler-free" class="list">
  <div class="list-header"><h2>Без спойлеров</h2><p class="note">что читатель встретит внутри</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>Мир БЕТОНА не выглядит разрушенным. Он выглядит слишком правильным. В нём есть порядок, отчёты, процедуры, спокойные формулировки и уверенность, что всё живое можно привести к допустимой форме.</p>
        <p>Антон работает там, где человеческие смыслы проходят проверку. Его задача — выявлять шум: воспоминания, чувства, запахи, вопросы и внутренние реакции, которые не совпадают с утверждённой гладкостью мира.</p>
        <p>Департамент Смыслов не обязательно кричит и угрожает. Он корректирует. Калибрует. Убирает лишнее. Делает реальность удобной для управления и называет это заботой, точностью, безопасностью.</p>
        <p>Но память не всегда стирается до конца. Иногда она возвращается не как доказательство, а как запах, сбой, внутренний гул, странная невозможность снова поверить в правильность стены.</p>
        <p>БЕТОН — это история о первой трещине. Не о громком бунте, не о победной позе, а о моменте, когда человек впервые перестаёт быть полностью частью конструкции.</p>
      </div>
    </li>
  </ul>
</section>
```

Reason:

- Applies MS decision: prose `Без спойлеров`, not card-like breakdown.
- Avoids plot turns while keeping premise and atmosphere.

### 6.6. Add full `Художественно-исследовательская рамка`

```html
<section id="research-frame" class="list">
  <div class="list-header"><h2>Художественно-исследовательская рамка</h2><p class="note">стабильность, память, давление</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>БЕТОН исследует стабильность не как благо и не как политический лозунг, а как состояние материи. Что происходит с человеком, если порядок становится настолько плотным, что в нём больше нет места для внутреннего движения?</p>
        <p>Книга показывает контроль не только как власть сверху. В БЕТОНЕ контроль работает через привычку, норму, служебный язык, страх ошибки, процедуру исправления и готовность человека заранее удалить в себе то, что может быть признано шумом.</p>
        <p>Память здесь становится опасной не потому, что она хранит факты, а потому что она возвращает человеку несовпадение. Официальная реальность требует гладкой поверхности. Личная память оставляет на ней след, запах, вопрос, трещину.</p>
        <p>Художественная форма позволяет показать этот процесс не как тезис, а как внутреннюю среду: через сцену, документ, протокол, усталость, холод, служебную точность и постепенное распознавание того, что насилие давно перестало выглядеть как насилие.</p>
        <p>Начало распада в БЕТОНЕ — не внешний взрыв. Это внутреннее событие: человек впервые замечает, что система не просто окружает его, а уже говорит его голосом.</p>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Use full version if readable, per MS decision.
- If future browser review finds it too dense, shorten only under a separate explicit implementation instruction.

### 6.7. Add `Темы / смысловые узлы` using 6-node version

```html
<section id="themes" class="list">
  <div class="list-header"><h2>Темы / смысловые узлы</h2><p class="note">карта книги</p></div>
  <div class="beton-grid">
    <article class="beton-card"><h3>Стабильность</h3><p>Неподвижность, названная безопасностью.</p></article>
    <article class="beton-card"><h3>Память</h3><p>То, что нарушает гладкую версию реальности.</p></article>
    <article class="beton-card"><h3>Шум</h3><p>Живой остаток, который не удалось откалибровать.</p></article>
    <article class="beton-card"><h3>Исправление</h3><p>Насилие, замаскированное под заботу.</p></article>
    <article class="beton-card"><h3>Департамент Смыслов</h3><p>Место, где человеческое переживание превращается в служебный материал.</p></article>
    <article class="beton-card"><h3>Трещина</h3><p>Первый внутренний отказ считать стену вечной.</p></article>
  </div>
</section>
```

Reason:

- Applies MS decision: 6-node themes version.
- Keeps the section scannable after prose-heavy blocks.

### 6.8. Add full `Для кого эта книга`

```html
<section id="for-whom" class="list">
  <div class="list-header"><h2>Для кого эта книга</h2><p class="note">читательский вход</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>БЕТОН может быть близок читателям, которым важна антиутопия без декоративного неона, без удобной героики и без простого деления мира на злодеев и жертв.</p>
        <p>Это книга для тех, кому интересна не только борьба с системой, но и более неприятный вопрос: как система входит в память, язык, привычку, страх и способность человека заранее исправлять самого себя.</p>
        <p>Она может быть особенно точной для читателей философской антиутопии, психологического триллера и социальной фантастики, где главный конфликт начинается не с внешнего восстания, а с трещины в восприятии.</p>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Use full reader block unless future browser review says it is too dense.
- Keep it reader-facing, not partner-facing.

### 6.9. Add shorter `Место в трилогии`

```html
<section id="place-in-trilogy" class="list">
  <div class="list-header"><h2>Место в трилогии</h2><p class="note">МОНОЛИТ / Том I</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>БЕТОН — Том I трилогии МОНОЛИТ и стадия затвердевшей стабильности. Он устанавливает стену, норму, механизм исправления, страх шума и первую внутреннюю трещину.</p>
        <p>После него следует ЖИЖА — вязкая деформация формы, затем ГАЗ — разгерметизация прежней системы. БЕТОН важен как начало: здесь распад ещё почти невидим, но его первый звук уже слышен внутри человека.</p>
      </div>
    </li>
  </ul>
</section>
```

Reason:

- Applies MS decision: shorter trilogy-place block.
- Avoids over-summarizing the whole trilogy.

### 6.10. Add `Где читать / издания` using verified links only

```html
<section id="editions" class="list">
  <div class="list-header"><h2>Где читать / издания</h2><p class="note">текущие доступные ссылки</p></div>
  <div class="beton-link-box">
    <p>Русская версия БЕТОНА доступна в Google Play Books.</p>
    <p>Английская версия доступна на Amazon.</p>
    <p>Страница серии МОНОЛИТ открывает общий контекст трилогии: БЕТОН, ЖИЖА, ГАЗ.</p>
    <div class="cta-row">
      <a class="btn" href="https://play.google.com/store/books/details?id=S__VEQAAQBAJ" target="_blank" rel="noopener noreferrer">Читать на русском в Google Play Books</a>
      <a class="btn secondary" href="https://www.amazon.com/dp/B0H18H1CFR" target="_blank" rel="noopener noreferrer">English edition on Amazon</a>
      <a class="btn secondary" href="https://www.ashraellen.com/ru/books/monolith/">Назад к серии МОНОЛИТ</a>
    </div>
  </div>
</section>
```

Notes:

- Verified links only.
- This duplicates the hero CTA links intentionally as a bottom conversion / navigation point. MS may decide during implementation review whether this second CTA row is useful or visually excessive.
- Do not invent availability.

### 6.11. Add full `Что важно не перепутать` compactly

Preferred compact prose:

```html
<section id="boundaries" class="list">
  <div class="list-header"><h2>Что важно не перепутать</h2><p class="note">границы книги</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body beton-copy">
        <p>БЕТОН — не самостоятельный политический памфлет. Власть здесь важна не как вывеска или режим, а как логика, которая умеет входить в память, язык, страх и привычку.</p>
        <p>БЕТОН — не декоративный киберпанк о гаджетах. Технологии вторичны. Главный механизм книги — редактирование реальности и калибровка человеческих смыслов.</p>
        <p>БЕТОН — не только социальный триллер. Его напряжение работает глубже: через вопрос о том, как человек начинает принимать давление за порядок.</p>
        <p>БЕТОН — не инструкция к бунту. Книга не продаёт героическую позу. Её интересует момент до бунта: первая внутренняя трещина.</p>
        <p>БЕТОН — первый том художественного и литературно-философского исследования того, как стабильность становится системой давления, а человек внутри стены начинает слышать её гул.</p>
      </div>
    </li>
  </ul>
</section>
```

Alternative compact card version, if implementation needs visual scannability:

```html
<section id="boundaries" class="list">
  <div class="list-header"><h2>Что важно не перепутать</h2><p class="note">границы книги</p></div>
  <div class="beton-grid">
    <article class="beton-card"><h3>Не памфлет</h3><p>Власть здесь важна как логика, а не как вывеска или режим.</p></article>
    <article class="beton-card"><h3>Не киберпанк о гаджетах</h3><p>Технологии вторичны; главный механизм — редактирование реальности.</p></article>
    <article class="beton-card"><h3>Не только триллер</h3><p>Напряжение строится вокруг того, как давление начинает казаться порядком.</p></article>
    <article class="beton-card"><h3>Не инструкция к бунту</h3><p>Книга не продаёт героическую позу; её интересует первая внутренняя трещина.</p></article>
    <article class="beton-card"><h3>Первый том исследования</h3><p>БЕТОН показывает, как стабильность становится системой давления.</p></article>
  </div>
</section>
```

Recommendation: start with compact prose to preserve severity. Use cards only if future browser review shows that the section is too heavy.

### 6.12. Preserve final signal / edition note / seal

Preserve existing line as a possible final signal after boundaries or before seal:

```html
<p class="quote-line">«Бетон боится только тех, кто перестал считать себя его частью.»</p>
```

Preserve edition note, but place it near `Где читать / издания` or before seal:

```html
<p>Издание выпущено в условиях экстерриториальности для сохранения целостности Сигнала.</p>
```

Preserve seal:

```html
<div class="seal"><img id="sealImg" src="https://www.ashraellen.com/assets/symbol.png" alt="Ashraellen symbol"><span>— mark of presence</span></div>
```

Notes:

- Do not change scripts under this plan.
- Do not add a new seal.
- Do not move seal above content.

---

## 7. What to replace / preserve / add

### Replace

Replace current short lead:

```html
<p class="lead">Первый том трилогии «МОНОЛИТ».</p>
```

with colder lead from section 6.2.

Replace the single long `Описание` block with structured sections:

```text
О книге
Без спойлеров
Художественно-исследовательская рамка
Темы / смысловые узлы
Для кого эта книга
Место в трилогии
Где читать / издания
Что важно не перепутать
```

### Preserve

Preserve:

```text
Бетон начинается не со стены. Он начинается с привычки называть тюрьму стабильностью.
```

Preserve:

```text
ДЕЛО № 2026-001B. Индекс: 6666548A. СТАТУС: Совершенно секретно.
```

Preserve:

```text
../../../../assets/covers/beton-ru.webp
../../../../assets/backgrounds/monolith-bg.webp
```

Preserve verified links:

```text
https://play.google.com/store/books/details?id=S__VEQAAQBAJ
https://www.amazon.com/dp/B0H18H1CFR
https://www.ashraellen.com/ru/books/monolith/
```

Preserve metadata, JSON-LD, social metadata and scripts exactly unless a separate command says otherwise.

### Add

Add page-local CSS only if necessary for layout.

Add section anchors only for visible-content navigation if future implementation wants internal CTAs:

```text
#about-beton
#spoiler-free
#research-frame
#themes
#for-whom
#place-in-trilogy
#editions
#boundaries
```

No new scripts.

---

## 8. Readability notes

1. The page will become longer. This is expected; individual book pages should carry more context than a single description block.
2. The strongest risk is over-explanation. Use section breaks and a 6-node themes grid to keep pressure without letting the page turn into an essay.
3. Full `О книге` and full research-frame are acceptable if the future implementation keeps text width controlled.
4. The 6-node themes grid gives readers relief between prose-heavy sections.
5. The bottom `Где читать / издания` section may duplicate hero CTAs. This is acceptable if it helps navigation after a long page; MS may remove it in implementation if it feels redundant.
6. Keep all text cold. Avoid warm partner language and avoid `Сияние` / `Сампо` mythopoetic softness.
7. The page should feel like a classified file that became readable, not like a brochure.

---

## 9. Implementation boundary for future work

This document is not authorization to edit the live site.

A separate explicit implementation command is required before editing:

```text
ru/books/monolith/beton/index.html
```

Future implementation should not edit:

```text
sitemap.xml
assets/books.css
ru/books/index.html
ru/books/monolith/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

Future implementation should not change:

```text
metadata
JSON-LD
social metadata
shared CSS
scripts
```

unless a separate command explicitly authorizes those changes.

---

## 10. Explicit statement that no live-site files were edited

No live-site files were edited during `COMMAND_007_HTML_Draft_Patch.md`.

The following file was read only:

```text
ru/books/monolith/beton/index.html
```

The following were not edited:

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

This command created only APM draft/report files:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_007_HTML_Draft_Patch.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_007_HTML_Draft_Patch.md
```
