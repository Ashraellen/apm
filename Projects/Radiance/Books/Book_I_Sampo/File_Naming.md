# File_Naming — Book I: Сампо

Working file naming rules for chapter drafts in **Сияние. Книга I. Сампо**.

---

## Language folder rule

Book I uses language folders.

Current structure:

```text
ru/Drafts/
ru/Final/
en/Drafts/
en/Final/
pl/Drafts/
pl/Final/
```

Russian master drafts live in:

```text
ru/Drafts/
```

Russian final assembled files, when created, should live in:

```text
ru/Final/
```

English and Polish folders are prepared but may remain empty until translation/adaptation begins.

---

## Chapter file naming rule

All chapter draft files must use short technical names.

Pattern:

```text
Chapter_XX_vY.md
```

Where:

```text
XX = chapter number, always two digits
Y  = version number
```

Examples:

```text
Chapter_01_v1.md
Chapter_01_v2.md
Chapter_02_v1.md
Chapter_12_v3.md
```

With language folder:

```text
ru/Drafts/Chapter_01_v1.md
ru/Drafts/Chapter_01_v2.md
```

---

## What must not be included in chapter filenames

Do not include chapter titles in filenames.

Avoid names like:

```text
Chapter_01_Malenkoe_Sobytie_v1.md
Chapter_02_Sampo_And_The_Living_Earth_v1.md
```

The chapter title lives inside the file, not in the filename.

---

## Reason

Filenames are technical handles.

They should stay stable, short and easy to sort.

Chapter titles may change during drafting.

Version numbers track development without forcing renames every time the title changes.

Language folders separate Russian master drafts, English drafts, Polish drafts, and later final versions without changing the chapter filenames themselves.

---

## Current confirmed example

```text
ru/Drafts/Chapter_01_v1.md
```

Title inside the file:

```text
Глава первая. Маленькое событие
```
