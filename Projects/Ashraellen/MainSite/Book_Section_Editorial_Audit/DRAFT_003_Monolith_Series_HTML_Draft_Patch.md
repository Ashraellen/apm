# DRAFT 003 — MONOLITH Series HTML Draft / Patch Plan

Date: 2026-07-01  
Project: Ashraellen / MainSite / Book Section Editorial Audit  
Status: HTML draft / patch plan only  
Command source: `COMMAND_003_Monolith_Series_HTML_Draft_Patch.md`  
Update: MS decision applied — `Карта распада` uses a 3×3 structure.

---

## 1. Status and scope

Этот документ подготавливает HTML-draft / patch plan для будущего расширения страницы:

```text
ru/books/monolith/index.html
```

Это не live-site правка. Файл `ru/books/monolith/index.html` не изменялся.

Цель: перевести редакционный черновик `DRAFT_002` и последующее решение MS по `Карте распада` в точный план HTML-внедрения, который MS сможет проверить до отдельного implementation-command.

Работа ограничена страницей серии `МОНОЛИТ`. Страницы `БЕТОН`, `ЖИЖА`, `Сияние`, `Сампо` и общий каталог книг в рамках этого command не трогаются.

---

## 2. Source files read / decision sources

Использованы:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/REPORT_001_Book_Section_Audit_Plan.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_002_Monolith_Series_Editorial_Expansion.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_002_Monolith_Series_Editorial_Expansion.md
ru/books/monolith/index.html
assets/books.css
```

Также применено решение MS по `Карте распада`:

```text
Не использовать плоскую карту на 9 равноправных узлов.
Не сокращать карту до трёх слишком бедных карточек.
Использовать структуру 3×3:
- три главных узла: БЕТОН, ЖИЖА, ГАЗ;
- внутри каждого узла — по три смысловых признака.
```

Из `REPORT_001` взято решение: `МОНОЛИТ` нужно усиливать, но не переписывать с нуля. Главная задача — добавить архитектуру, не потеряв холодный протокольный нерв.

Из `DRAFT_002` взяты утверждённые public-facing тексты и структура: hero, `Что такое МОНОЛИТ`, художественно-исследовательская рамка, карта распада, `Для кого`, `Что важно не перепутать`, существующие фразы к сохранению.

Из `MS_REPORT_002` взят practical direction: использовать холодный MONOLITH-specific voice, не смягчать до тона `Сияния`, сохранить сильные фразы и подготовить следующий HTML-draft только как APM-документ.

Из текущего `ru/books/monolith/index.html` установлено, что основной редактируемый участок находится внутри:

```html
<main class="main"><div class="container">
  ...
</div></main>
```

Текущая страница уже содержит:

- `h1` и `lead`;
- блок `Серия`;
- блок `Тома`;
- блок `Фраза серии`;
- inline style для монолитной страницы;
- общий CSS из `assets/books.css`.

---

## 3. Implementation principle

Будущая HTML-фаза должна идти по принципу минимального вторжения:

1. Не менять live site без отдельного command.
2. Не менять `sitemap.xml`.
3. Не создавать SEO scripts.
4. Не запускать metadata repair scripts.
5. Не использовать client-side JS для content, SEO, metadata или social metadata repair.
6. Основной публичный текст должен быть статическим HTML.
7. Не трогать общий `assets/books.css`, если можно обойтись минимальными page-local style additions внутри существующего `<style>` страницы.
8. Не менять JSON-LD и metadata в рамках этого draft, кроме отдельного раздела optional future work.
9. Сохранить текущий фон, обложки, карточки томов и главный сигнал серии.
10. Использовать архитектуру `Сияния` только как каркас, не как тон.
11. `Карта распада` должна быть иерархической: три состояния социальной материи, внутри каждого — три признака.

Коротко: не строим новый Департамент, просто даём старому бетону нормальную несущую конструкцию.

---

## 4. Proposed final page architecture for `ru/books/monolith/index.html`

Рекомендуемая структура внутри `<main class="main"><div class="container">`:

1. Hero / entry:
   - kicker;
   - `h1`;
   - updated lead;
   - hero-note / signal;
   - CTA row.

2. `Что такое МОНОЛИТ`:
   - заменить текущий блок `Серия`;
   - сохранить opening sentence `Перед вами хроника контролируемого распада...`.

3. `Тома`:
   - сохранить карточки томов;
   - добавить `id="volumes"`;
   - в future HTML implementation можно заменить `href="#"` на static links, если MS одобрит.

4. `Художественно-исследовательская рамка`:
   - новый блок после `Тома`.

5. `Карта распада`:
   - новый блок после research frame;
   - использовать модель 3×3:
     - `БЕТОН` → три признака;
     - `ЖИЖА` → три признака;
     - `ГАЗ` → три признака.

6. `Для кого этот проект`:
   - две компактные колонки.

7. `Что важно не перепутать`:
   - full version, но в компактной структуре.

8. `Фраза серии`:
   - сохранить как финальный сигнал или заменить на альтернативный финальный сигнал, если MS захочет избежать повтора hero.

9. Seal:
   - оставить как есть.

---

## 5. Exact section-by-section HTML draft / pseudo-diff

### 5.1. Minimal local style additions

Current file already contains an inline `<style>` block with `series-grid`, `series-card`, `quote-line`, `series-desc`, etc.

For the future HTML implementation, add the following page-local CSS inside the existing `<style>` block, after the current `.series-card .btn` rule and before the mobile media query.

Do not add this to `assets/books.css` unless a separate design cleanup command requests it.

```html
<style>
  /* existing MONOLITH page styles remain */

  .monolith-kicker{
    margin:0 0 8px;
    font-family:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
    font-size:12px;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--muted);
  }

  .monolith-signal{
    margin:0 0 14px;
    max-width:76ch;
    font-family:Georgia,'Times New Roman',serif;
    font-size:18px;
    line-height:1.45;
    color:rgba(242,242,244,.94);
  }

  .monolith-copy{
    font-size:13px;
    line-height:1.78;
    color:var(--muted);
    max-width:82ch;
  }

  .monolith-copy p{
    margin:0 0 12px;
  }

  .monolith-copy p:last-child{
    margin-bottom:0;
  }

  .monolith-state-grid{
    display:grid;
    grid-template-columns:repeat(3,minmax(0,1fr));
    gap:14px;
  }

  .monolith-state-card,
  .monolith-box{
    border:1px solid rgba(242,242,244,.12);
    border-radius:14px;
    padding:14px;
    background:rgba(0,0,0,.20);
  }

  .monolith-state-card h3,
  .monolith-box h3{
    margin:0 0 7px;
    color:var(--fg);
    font-size:15px;
    line-height:1.25;
  }

  .monolith-state-card .state-note{
    margin:0 0 10px;
    color:var(--muted);
    font-size:12px;
    line-height:1.35;
    font-family:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
    letter-spacing:.03em;
  }

  .monolith-state-card ul{
    margin:0;
    padding:0;
    list-style:none;
    display:grid;
    gap:7px;
  }

  .monolith-state-card li{
    color:var(--muted);
    font-size:13px;
    line-height:1.45;
  }

  .monolith-state-card li::before{
    content:'— ';
    opacity:.75;
  }

  .monolith-box p{
    margin:0;
    color:var(--muted);
    font-size:13px;
    line-height:1.55;
  }

  .monolith-two-col{
    display:grid;
    grid-template-columns:repeat(2,minmax(0,1fr));
    gap:14px;
  }

  @media(max-width:900px){
    .monolith-state-grid,
    .monolith-two-col{
      grid-template-columns:1fr;
    }
  }
</style>
```

Reason: existing `assets/books.css` has good base blocks but no dedicated 3×3 semantic card layout for the map or two compact columns. Local additions keep the change isolated to `MONOLITH`.

### 5.2. Replace current `h1 + lead` with expanded hero

Current block:

```html
<h1 class="h1">МОНОЛИТ</h1>
<p class="lead">МОНОЛИТ — трилогия социальной фантастики, антиутопии и философского киберпанка о контроле, памяти и распаде систем.</p>
```

Future draft replacement:

```html
<p class="monolith-kicker">Протокол распада социальной материи / БЕТОН — ЖИЖА — ГАЗ</p>
<h1 class="h1">МОНОЛИТ</h1>
<p class="lead">МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Три тома фиксируют переход социальной материи через три состояния: БЕТОН, ЖИЖА, ГАЗ — от затвердевшей стабильности к вязкой деформации и полной разгерметизации формы.</p>
<p class="monolith-signal">Система боится не бунта.<br>Она боится первой трещины.</p>
<div class="cta-row">
  <a class="btn" href="#volumes">Тома трилогии</a>
  <a class="btn secondary" href="#collapse-map">Карта распада</a>
  <a class="btn secondary" href="#boundaries">Что важно не перепутать</a>
</div>
```

Notes:

- Keeps the colder MONOLITH-specific voice.
- Uses command-approved kicker and lead.
- Moves the main signal upward into hero without deleting the final `Фраза серии` block yet. MS should decide whether to keep the signal both in hero and near the end. Recommendation: keep in hero and transform the final block into an alternative signal if repetition feels heavy.

### 5.3. Replace current `Серия` block with `Что такое МОНОЛИТ`

Current block starts:

```html
<section class="list"><div class="list-header"><h2>Серия</h2><p class="note">БЕТОН / ЖИЖА / ГАЗ</p></div>...
```

Future draft replacement:

```html
<section id="about-monolith" class="list">
  <div class="list-header">
    <h2>Что такое МОНОЛИТ</h2>
    <p class="note">БЕТОН / ЖИЖА / ГАЗ</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body">
        <p class="quote-line" style="margin:0 0 12px;">Перед вами хроника контролируемого распада: последовательная фиксация фазового перехода социальной материи, запечатлённая в трёх агрегатных состояниях: БЕТОН, ЖИЖА, ГАЗ.</p>
        <div class="monolith-copy">
          <p>МОНОЛИТ — литературно-философская антиутопическая трилогия о мире, где стабильность становится не защитой, а формой затвердевания. В этом мире порядок больше не служит человеку. Он сохраняет собственную форму, редактирует память, сглаживает шум, устраняет внутренний резонанс и называет давление заботой о будущем.</p>
          <p>БЕТОН показывает общество, которое слишком долго называло неподвижность безопасностью. Здесь живая мысль становится дефектом, личная память — угрозой, а первая трещина возникает не на стене, а внутри человека, который вдруг слышит гул там, где должна быть тишина.</p>
          <p>ЖИЖА начинается после трещины. Форма уже не держит прежней жёсткости, но свобода ещё не наступила. Человек оказывается в вязкой среде, где сопротивление устаёт, границы растворяются, деформация становится привычкой, а участие в недопустимом постепенно начинает казаться нормой.</p>
          <p>ГАЗ — финальная стадия разгерметизации. Смысл выходит из прежних контейнеров. Контроль теряет стену, но не исчезает сразу: он пытается распространиться, смешаться с воздухом, стать невидимым и потому ещё более привычным. МОНОЛИТ исследует не будущее как прогноз, а настоящее как материал, который уже меняет состояние.</p>
        </div>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Preserves the mandatory opening phrase.
- Redistributes current ideas about stability, living thought as defect, editing memory and phase transition.
- This is the full version from `DRAFT_002`; if MS considers it heavy, use the medium version below.

Medium alternative for this block:

```html
<section id="about-monolith" class="list">
  <div class="list-header">
    <h2>Что такое МОНОЛИТ</h2>
    <p class="note">БЕТОН / ЖИЖА / ГАЗ</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body">
        <p class="quote-line" style="margin:0 0 12px;">Перед вами хроника контролируемого распада: последовательная фиксация фазового перехода социальной материи, запечатлённая в трёх агрегатных состояниях: БЕТОН, ЖИЖА, ГАЗ.</p>
        <div class="monolith-copy">
          <p>МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Её три тома устроены как три агрегатных состояния социальной материи: БЕТОН, ЖИЖА, ГАЗ.</p>
          <p>БЕТОН — стадия затвердевшей стабильности, где порядок становится тюрьмой. ЖИЖА — стадия вязкой деформации, где человек постепенно теряет форму и начинает соглашаться со средой. ГАЗ — стадия разгерметизации, где прежние структуры больше не удерживают смысл.</p>
          <p>Это не фантастика о далёком будущем. Это жёсткая художественная фиксация того, как система входит в память, язык, тело, страх, привычку и нормальность.</p>
        </div>
      </div>
    </li>
  </ul>
</section>
```

Recommendation: start with full version in the draft review, but be ready to use medium version if the page becomes too dense on mobile.

### 5.4. Preserve `Тома` block with minor future static-link cleanup

Current `Тома` block should remain mostly unchanged.

Recommended future draft adjustment:

```html
<section id="volumes" class="list">
  <div class="list-header"><h2>Тома</h2><p class="note">открыть страницу книги</p></div>
  <div class="series-grid">
    <article class="series-card">
      <div class="series-cover"><img src="../../../assets/covers/beton-ru.webp" alt="БЕТОН — обложка" loading="lazy"></div>
      <h3>Том I — БЕТОН</h3>
      <p>Стабильность становится тюрьмой. Память редактируется. Первая трещина появляется внутри самой Системы.</p>
      <div class="cta-row"><a id="goBeton" class="btn" href="https://www.ashraellen.com/ru/books/monolith/beton/">Открыть том</a></div>
    </article>
    <article class="series-card">
      <div class="series-cover"><img src="../../../assets/covers/sludge-ru.webp" alt="ЖИЖА — обложка" loading="lazy"></div>
      <h3>Том II — ЖИЖА</h3>
      <p>После первой трещины форма начинает распадаться. Человек постепенно становится веществом среды.</p>
      <div class="cta-row"><a id="goSludge" class="btn" href="https://www.ashraellen.com/ru/books/monolith/sludge/">Открыть том</a></div>
    </article>
    <article class="series-card">
      <div class="series-cover placeholder">ГАЗ</div>
      <h3>Том III — ГАЗ</h3>
      <p>Финальная разгерметизация. Смысл начинает распространяться там, где прежняя форма уже не удерживает давление.</p>
      <div class="cta-row"><span class="btn secondary">В подготовке</span></div>
    </article>
  </div>
</section>
```

Notes:

- Adds `id="volumes"` for CTA navigation.
- Keeps current cards and images.
- Suggested static href cleanup is included as draft plan only. MS should confirm whether to keep or remove the existing inline JS link reassignment in the later implementation.

### 5.5. Add `Художественно-исследовательская рамка` block after `Тома`

```html
<section id="research-frame" class="list">
  <div class="list-header">
    <h2>Художественно-исследовательская рамка</h2>
    <p class="note">контроль, память, форма</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body monolith-copy">
        <p>МОНОЛИТ исследует систему не как внешнего злодея, а как способ организации восприятия. Контроль здесь действует не только через приказ, запрет или наказание. Он входит в язык, в бытовую норму, в память, в страх ошибки, в привычку соглашаться с тем, что уже названо правильным.</p>
        <p>Художественная форма позволяет показать то, что плохо видно в прямом объяснении: момент, когда человек ещё уверен, что думает сам, но его внутренние реакции уже откалиброваны. Он помнит не всё, что было. Боится не всего, что опасно. Соглашается не потому, что убеждён, а потому что среда давно обучила его выбирать удобную версию реальности.</p>
        <p>Трилогия работает с образом социальной материи. В БЕТОНЕ общество затвердевает: форма кажется вечной, а трещина — преступлением. В ЖИЖЕ эта форма размягчается: давление больше не выглядит как стена, оно становится средой. В ГАЗЕ удерживающие структуры разгерметизируются: контроль пытается перестать быть видимым и раствориться в самом воздухе нормальности.</p>
        <p>МОНОЛИТ не объясняет систему лекцией. Он фиксирует её через сцену, протокол, запах, память, процедуру, усталость, сбой и внутренний шум. Здесь исследование происходит не над текстом, а внутри текста: там, где человек впервые замечает, что его реальность уже редактировали до того, как он начал её защищать.</p>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Uses the main version from `DRAFT_002`.
- Uses the word `исследует`, but keeps the block rooted in system image and artistic mechanism.
- Does not sound like a grant application.

### 5.6. Add `Карта распада` block after research frame — MS-approved 3×3 model

Do not use the previous flat 9-node list.  
Do not use the too-poor 3-card-only version.  
Use three main states, each with three signs.

Recommended HTML draft:

```html
<section id="collapse-map" class="list">
  <div class="list-header">
    <h2>Карта распада</h2>
    <p class="note">три состояния / девять признаков</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body">
        <div class="monolith-state-grid">
          <article class="monolith-state-card">
            <h3>БЕТОН</h3>
            <p class="state-note">затвердевшая стабильность</p>
            <ul>
              <li>стабильность как тюрьма</li>
              <li>память как опасность</li>
              <li>первая трещина</li>
            </ul>
          </article>

          <article class="monolith-state-card">
            <h3>ЖИЖА</h3>
            <p class="state-note">вязкая деформация</p>
            <ul>
              <li>усталость сопротивления</li>
              <li>растворение границ</li>
              <li>соучастие как привычка</li>
            </ul>
          </article>

          <article class="monolith-state-card">
            <h3>ГАЗ</h3>
            <p class="state-note">разгерметизация формы</p>
            <ul>
              <li>контроль становится воздухом</li>
              <li>смысл выходит из контейнеров</li>
              <li>прежняя система теряет стену, но не исчезает</li>
            </ul>
          </article>
        </div>
      </div>
    </li>
  </ul>
</section>
```

Expanded text alternative if MS wants each state to have one explanatory line before the three signs:

```html
<section id="collapse-map" class="list">
  <div class="list-header">
    <h2>Карта распада</h2>
    <p class="note">три состояния / девять признаков</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body">
        <div class="monolith-state-grid">
          <article class="monolith-state-card">
            <h3>БЕТОН</h3>
            <p class="state-note">затвердевшая стабильность</p>
            <p class="state-desc">Форма кажется вечной, потому что всё живое внутри неё уже объявлено дефектом.</p>
            <ul>
              <li>стабильность как тюрьма</li>
              <li>память как опасность</li>
              <li>первая трещина</li>
            </ul>
          </article>
          <article class="monolith-state-card">
            <h3>ЖИЖА</h3>
            <p class="state-note">вязкая деформация</p>
            <p class="state-desc">Форма больше не защищает человека, но ещё удерживает его внутри среды.</p>
            <ul>
              <li>усталость сопротивления</li>
              <li>растворение границ</li>
              <li>соучастие как привычка</li>
            </ul>
          </article>
          <article class="monolith-state-card">
            <h3>ГАЗ</h3>
            <p class="state-note">разгерметизация формы</p>
            <p class="state-desc">Прежние контейнеры распадаются, а контроль пытается стать невидимым и привычным.</p>
            <ul>
              <li>контроль становится воздухом</li>
              <li>смысл выходит из контейнеров</li>
              <li>прежняя система теряет стену, но не исчезает</li>
            </ul>
          </article>
        </div>
      </div>
    </li>
  </ul>
</section>
```

If the expanded version is used, add this CSS inside `.monolith-state-card` styles:

```css
.monolith-state-card .state-desc{
  margin:0 0 10px;
  color:var(--muted);
  font-size:13px;
  line-height:1.45;
}
```

Recommendation: use the compact 3×3 version first. It is stronger, cleaner and less explanatory. Use expanded version only if MS decides that the cards need one line of orientation.

### 5.7. Add `Для кого этот проект` block after map

```html
<section class="list">
  <div class="list-header">
    <h2>Для кого этот проект</h2>
    <p class="note">читатели и профессиональный вход</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body monolith-two-col">
        <div class="monolith-box">
          <h3>Читателям</h3>
          <p>МОНОЛИТ может быть близок читателям, которым важна антиутопия без декоративного неона и удобной героики: жёсткая философская проза о контроле, памяти, страхе, системном давлении и человеке, который начинает слышать сбой внутри слишком правильного мира.</p>
        </div>
        <div class="monolith-box">
          <h3>Издателям / партнёрам / переводчикам</h3>
          <p>Серия открыта для издательского, переводческого и редакторского сотрудничества. Её профессиональный интерес — в соединении антиутопической формы, философской прозы и художественного исследования контроля, памяти и распада систем.</p>
        </div>
      </div>
    </li>
  </ul>
</section>
```

Notes:

- Uses shorter partner version from `DRAFT_002`, as requested by `COMMAND_003`.
- Keeps the professional doorway without sounding like a grant pitch.

### 5.8. Add `Что важно не перепутать` block after `Для кого`

```html
<section id="boundaries" class="list">
  <div class="list-header">
    <h2>Что важно не перепутать</h2>
    <p class="note">границы серии</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body monolith-copy">
        <p>МОНОЛИТ — не прогноз будущего. Он не утверждает, что мир обязательно станет таким. Он показывает, какие процессы уже становятся возможными, когда контроль входит в память, язык, тело, страх и привычку.</p>
        <p>МОНОЛИТ — не инструкция к бунту. Серия не романтизирует сопротивление и не продаёт героическую позу. Её интересует более тихий и более опасный момент: первая внутренняя трещина.</p>
        <p>МОНОЛИТ — не политический памфлет. Власть здесь важна не как вывеска, партия или режим, а как логика, которая умеет повторяться в разных системах, организациях, семьях, языках и способах мышления.</p>
        <p>МОНОЛИТ — не декоративный киберпанк о гаджетах. Технологии здесь вторичны. Главный механизм — редактирование реальности, памяти и нормы.</p>
        <p>МОНОЛИТ — не технологическая фантазия. Его холод не в машинах, а в процедурах, привычках, отчётах, исправлениях, мягких формулировках и согласии человека на собственное сжатие.</p>
        <p>МОНОЛИТ — художественное исследование того, как системная логика входит в человека настолько глубоко, что он начинает принимать давление за порядок, страх — за разумность, а отсутствие трещин — за жизнь.</p>
      </div>
    </li>
  </ul>
</section>
```

Short fallback if page becomes too heavy:

```html
<section id="boundaries" class="list">
  <div class="list-header">
    <h2>Что важно не перепутать</h2>
    <p class="note">границы серии</p>
  </div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body monolith-copy">
        <p>МОНОЛИТ — не прогноз будущего, не инструкция к бунту, не политический памфлет и не декоративный киберпанк о гаджетах. Это художественное исследование того, как системная логика входит в память, язык, тело, привычку, страх и нормальность.</p>
      </div>
    </li>
  </ul>
</section>
```

Recommendation: use full version for review; fallback only if mobile readability suffers.

### 5.9. Preserve or adjust final `Фраза серии`

Current block:

```html
<section class="list"><div class="list-header"><h2>Фраза серии</h2><p class="note">сигнал</p></div><ul class="items"><li class="item" style="grid-template-columns:1fr;"><div class="body"><p class="quote-line" style="margin:0;">Система боится не бунта.<br>Она боится первой трещины.</p></div></li></ul></section>
```

Decision needed from MS:

Option A — keep final block unchanged.  
Pros: strong closing signal.  
Cons: repeats hero signal.

Option B — remove final block after moving signal to hero.  
Pros: less repetition.  
Cons: loses strong ending.

Option C — transform final block into variant signal:

```html
<section class="list">
  <div class="list-header"><h2>Фраза серии</h2><p class="note">сигнал</p></div>
  <ul class="items">
    <li class="item" style="grid-template-columns:1fr;">
      <div class="body">
        <p class="quote-line" style="margin:0;">Распад начинается не тогда, когда рушится стена.<br>Он начинается, когда человек впервые слышит внутри неё гул.</p>
      </div>
    </li>
  </ul>
</section>
```

Recommendation: Option C. It keeps the final ritual удар, but avoids exact repetition. Если MS хочет максимальную узнаваемость — Option A.

---

## 6. Notes on existing blocks: replace, preserve, move

### Replace

Replace:

```html
<h1 class="h1">МОНОЛИТ</h1>
<p class="lead">...</p>
```

with the expanded hero from section 5.2.

Replace current `Серия` block with `Что такое МОНОЛИТ` from section 5.3.

### Preserve

Preserve:

```text
Система боится не бунта.
Она боится первой трещины.
```

Preserve:

```text
Перед вами хроника контролируемого распада...
```

Preserve the three volume cards and cover paths:

```text
../../../assets/covers/beton-ru.webp
../../../assets/covers/sludge-ru.webp
```

Preserve background:

```text
../../../assets/backgrounds/monolith-bg.webp
```

Preserve seal:

```html
<div class="seal"><img id="sealImg" src="https://www.ashraellen.com/assets/symbol.png" alt="Ashraellen symbol"><span>— mark of presence</span></div>
```

### Move / redistribute

The existing `Серия` paragraphs should not be discarded. Their core material is redistributed into `Что такое МОНОЛИТ`, the research frame and the 3×3 map:

- `Мы привыкли считать стабильность безопасностью` → `Что такое МОНОЛИТ` and `БЕТОН` state.
- `абсолютная стабильность — состояние предельного затвердевания` → `Что такое МОНОЛИТ` and `БЕТОН` state.
- `любая живая мысль становится дефектом` → `Что такое МОНОЛИТ`.
- `исправление / удаление шума / редактирование реальности` → research frame and boundaries.
- `путь от Бетона через Жижу к разгерметизации` → hero, `Что такое`, 3×3 map.

---

## 7. Recommended metadata / JSON-LD changes for future separate stage

No metadata or JSON-LD changes are included in this command.

Optional future metadata improvement, only under a separate command:

Current description:

```text
МОНОЛИТ — трилогия социальной фантастики, антиутопии и философского киберпанка о контроле, памяти и распаде систем.
```

Possible future description:

```text
МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти, социальной материи, редактировании реальности и распаде систем: БЕТОН, ЖИЖА, ГАЗ.
```

Possible future JSON-LD `BookSeries.description` update should mirror the approved public description, but this must be a separate metadata / schema command or explicitly included in an implementation command.

Do not run broad metadata repair scripts.

---

## 8. Mobile / readability notes

1. The page will become significantly longer. This is acceptable if sections remain scannable.
2. The `Карта распада` should be a 3-column state grid on desktop and 1-column on mobile.
3. The 3×3 model is better than a flat 9-node list because it preserves the internal logic of the trilogy: three states, each with three signs.
4. `Что важно не перепутать` full version is the heaviest block. MS should test whether it feels like necessary boundary-setting or too much explanation.
5. Two-column `Для кого` should collapse to one column under 900px.
6. Existing `.main` uses vertical centering on desktop. With longer page content this may still work, but if the page feels vertically awkward, a future implementation may need to consider `align-items:flex-start` for this page only. Do not change this in the draft unless visual testing confirms the need.
7. Keep text blocks narrow: `max-width:82ch` is recommended for readability.
8. Avoid adding images, new backgrounds or design effects. The page needs pressure, not carnival.

---

## 9. Explicit list of files not touched

The following live-site files were not edited:

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

No SEO scripts were created.  
No metadata repair scripts were run.  
No client-side JavaScript was added for content, SEO, metadata or social metadata.

---

## 10. Explicit statement that no live-site edits were made

No live-site edits were made during this `DRAFT_003` update.

This update changed only the APM draft plan:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/DRAFT_003_Monolith_Series_HTML_Draft_Patch.md
```

A separate explicit command is required before editing:

```text
ru/books/monolith/index.html
```

or any other live-site file.
