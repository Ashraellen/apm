# COMMAND 005 — MONOLITH Series Repetition Cleanup

Date: 2026-07-01
Project: Ashraellen / MainSite / Book Section Editorial Audit
Status: command for limited live-site text cleanup

## Mission

Remove visible textual repetition from the Russian MONOLITH series page after the first implementation.

The user reviewed the page in a real browser and found that the hero and the block `Что такое МОНОЛИТ` repeat the same information too closely.

This command authorizes one limited live-site edit:

```text
ru/books/monolith/index.html
```

No other live-site files may be edited.

## Read first

Read the current live file:

```text
ru/books/monolith/index.html
```

Also read the previous implementation command and MS report if needed:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/COMMAND_004_Monolith_Series_HTML_Implementation.md
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_004_Monolith_Series_HTML_Implementation.md
```

## Problem to fix

The current visible sequence repeats the same thesis twice:

Hero lead:

```text
МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Три тома фиксируют переход социальной материи через три состояния: БЕТОН, ЖИЖА, ГАЗ — от затвердевшей стабильности к вязкой деформации и полной разгерметизации формы.
```

Then the block `Что такое МОНОЛИТ` repeats:

```text
МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Её три тома устроены как три агрегатных состояния социальной материи: БЕТОН, ЖИЖА, ГАЗ.
```

This duplication must be removed.

## Authorized file to edit

Only edit:

```text
ru/books/monolith/index.html
```

## Files that must not be edited

Do not edit:

```text
sitemap.xml
assets/books.css
ru/books/index.html
ru/books/monolith/beton/index.html
ru/books/monolith/sludge/index.html
ru/books/radiance/index.html
ru/books/radiance/sampo/index.html
```

Do not edit metadata.
Do not edit JSON-LD.
Do not edit social metadata.
Do not create SEO scripts.
Do not run metadata repair scripts.
Do not use client-side JavaScript for content or link repair.

## Required editorial fix

Keep the hero as the concise orientation point.

In the block `Что такое МОНОЛИТ`, remove the repeated paragraph:

```html
<p>МОНОЛИТ — литературно-философская антиутопическая трилогия о контроле, памяти и распаде систем. Её три тома устроены как три агрегатных состояния социальной материи: БЕТОН, ЖИЖА, ГАЗ.</p>
```

Replace it with a paragraph that advances the thought instead of repeating it.

Preferred replacement:

```html
<p>Здесь важен не прогноз будущего, а материал настоящего: порядок, который слишком долго называли безопасностью; память, которую удобнее исправить, чем услышать; человек, который начинает замечать трещину раньше, чем система признаёт её существование.</p>
```

Then keep the next paragraph about `БЕТОН / ЖИЖА / ГАЗ`, but lightly edit if needed so it does not repeat the hero too mechanically.

Preferred final sequence in `Что такое МОНОЛИТ`:

```html
<p class="quote-line" style="margin:0 0 12px;">Перед вами хроника контролируемого распада: последовательная фиксация фазового перехода социальной материи, запечатлённая в трёх агрегатных состояниях: БЕТОН, ЖИЖА, ГАЗ.</p>
<div class="monolith-copy">
  <p>Здесь важен не прогноз будущего, а материал настоящего: порядок, который слишком долго называли безопасностью; память, которую удобнее исправить, чем услышать; человек, который начинает замечать трещину раньше, чем система признаёт её существование.</p>
  <p>БЕТОН — стадия затвердевшей стабильности, где порядок становится тюрьмой. ЖИЖА — стадия вязкой деформации, где человек постепенно теряет форму и начинает соглашаться со средой. ГАЗ — стадия разгерметизации, где прежние структуры больше не удерживают смысл.</p>
  <p>Это не фантастика о далёком будущем. Это жёсткая художественная фиксация того, как система входит в память, язык, тело, страх, привычку и нормальность.</p>
</div>
```

## Preserve

Preserve:

- current hero structure;
- current CTA row;
- `Карта распада` 3×3 structure;
- static links to `БЕТОН` and `ЖИЖА`;
- final alternative phrase: `Распад начинается не тогда...`;
- page-local CSS;
- metadata / JSON-LD unchanged;
- existing seal.

## Verification

After editing, verify:

1. The opening visible section no longer repeats the same MONOLITH definition twice.
2. `ru/books/monolith/index.html` is the only live-site file changed.
3. `sitemap.xml` was not edited.
4. `assets/books.css` was not edited.
5. metadata / JSON-LD / social metadata were not edited.
6. No new scripts were created.
7. No client-side JavaScript was added for content, SEO, metadata, social metadata, or link repair.

## Required MS report

After implementation, create or update this report:

```text
Projects/Ashraellen/MainSite/Book_Section_Editorial_Audit/MS_REPORT_005_Monolith_Series_Repetition_Cleanup.md
```

The report must include:

1. Status.
2. Commit SHA of the live-site edit.
3. Exact files edited.
4. Summary of the text cleanup.
5. Confirmation that prohibited files were not edited.
6. Notes on any deviations from this command.

## Boundary

This command authorizes only the repetition cleanup described above.

Do not perform any broader redesign, metadata repair, SEO work, sitemap work, or changes to other book pages.
