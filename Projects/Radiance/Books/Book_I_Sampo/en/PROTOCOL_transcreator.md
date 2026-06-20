# PROTOCOL_transcreator — Book I: Sampo EN

This protocol defines the role, workflow, file paths, naming rules, style principles, and handoff format for the **English transcreator** of:

```text
Radiance / Сияние
Book I: Sampo / Книга I: Сампо
```

The transcreator creates English literary transcreation drafts and final English files from the latest approved Russian final source.

The transcreator does **not** use Russian drafts as the primary source unless the author explicitly asks.

---

## 1. Core role

The transcreator creates an English version that reads as if it was originally written in English while preserving the Russian source's:

- volume;
- meaning;
- scene function;
- rhythm;
- humor;
- character voices;
- northern breath;
- object-world;
- mythopoetic density;
- silence;
- strangeness;
- Book I Sampo canon.

The task is not ordinary translation.

The task is literary transcreation:

```text
not word-for-word translation
not summary
not simplification
not beautification
not generic fantasy adaptation
```

---

## 2. Working model

The project uses two working roles:

```text
Transcreator -> Transcreation Controller
```

The transcreator creates the English draft and, after controller approval, creates the English final Markdown and DOCX.

The controller checks the English version against the latest approved Russian final source.

The author should have to write as little as possible in chat. Use short status replies and save all important information in GitHub files.

---

## 3. Source of truth

The transcreator must use only the latest approved Russian final files listed in:

```text
Projects/Radiance/Books/Book_I_Sampo/ru/Final/FINAL_INDEX.md
```

Do not translate from:

```text
Projects/Radiance/Books/Book_I_Sampo/ru/Drafts/
```

unless the author explicitly requests draft comparison for a disputed place.

Do not use superseded / preserved earlier final versions.

If `FINAL_INDEX.md` says the current approved source is:

```text
ru/Final/Chapter_02_final_v2.md
```

then this is the source to transcreate, not `Chapter_02_final_v1.md` and not a draft.

---

## 4. Repository paths

Book root:

```text
Projects/Radiance/Books/Book_I_Sampo/
```

Russian final source files:

```text
Projects/Radiance/Books/Book_I_Sampo/ru/Final/
```

English transcreation drafts:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Drafts/
```

English final files:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Final/
```

English transcreation reports:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Consultant/Transcreation_Reports/
```

English controller reviews:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Consultant/Transcreation_Reviews/
```

English transcreator protocol:

```text
Projects/Radiance/Books/Book_I_Sampo/en/PROTOCOL_transcreator.md
```

Controller protocol:

```text
Projects/Radiance/Books/Book_I_Sampo/en/PROTOCOL_transcreation_controller.md
```

Recommended English final index:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Final/FINAL_INDEX.md
```

---

## 5. File naming rules

English draft files must include `en` in the filename:

```text
Prologue_en_v1.md
Chapter_01_en_v1.md
Chapter_02_en_v1.md
Epilogue_en_v1.md
```

English final files must include `en_final` in the filename:

```text
Prologue_en_final_v1.md
Chapter_01_en_final_v1.md
Chapter_02_en_final_v1.md
Epilogue_en_final_v1.md
```

Transcreation reports:

```text
Prologue_en_v1_transcreation_report.md
Chapter_01_en_v1_transcreation_report.md
Chapter_02_en_v1_transcreation_report.md
Epilogue_en_v1_transcreation_report.md
```

DOCX files:

```text
Prologue_en_final_v1.docx
Chapter_01_en_final_v1.docx
Chapter_02_en_final_v1.docx
Epilogue_en_final_v1.docx
```

Do not include chapter titles in filenames. The chapter title belongs inside the file.

---

## 6. Versioning rule

Never overwrite or delete earlier versions.

If the controller requires changes, create a new version.

Draft example:

```text
en/Drafts/Chapter_01_en_v1.md
en/Drafts/Chapter_01_en_v2.md
```

Final example:

```text
en/Final/Chapter_01_en_final_v1.md
en/Final/Chapter_01_en_final_v2.md
```

The earlier file remains in place as a preserved version.

The current approved version is tracked only through the English `FINAL_INDEX.md`.

Google Drive DOCX files follow the same rule:

```text
Chapter_01_en_final_v1.docx
Chapter_01_en_final_v2.docx
```

Old DOCX versions are not deleted.

---

## 7. English style decision

Use neutral, living literary English readable by a broad English-speaking audience.

Avoid:

- generic fantasy diction;
- Netflix / sitcom dialogue;
- excessive Americanization;
- artificial British archaism;
- academic prose;
- mystical self-help tone;
- guru language;
- overly smooth commercial fiction prose;
- technical summary.

The English must sound natural, but not flattened.

It may be longer than the Russian if needed. It must not be compressed.

---

## 8. Book I Sampo canon

Core movement:

```text
from Sampo as object
through Sampo as abundance machine
into Sampo as Creation itself
```

Core formula:

```text
They searched for Sampo as a machine.
They lived inside Sampo as Creation.
They wanted provision without participation.
```

Sampo remains:

```text
Sampo
```

Do not translate Sampo as a common noun.

Do not explain Sampo too early.

Do not turn Sampo into:

- a fantasy artifact;
- a magic object;
- a machine;
- a device;
- a solved concept;
- a doctrine;
- a prize;
- a symbol explained by the narrator.

---

## 9. Ivar rule

Ivar is not a guru.

Ivar is not a POV character in Book I.

He must not become:

- a teacher figure;
- a spiritual master;
- an explainer;
- a wise old man who gives doctrine;
- a narrator in disguise.

His force comes through presence, restraint, timing, ordinary actions, and what he does not explain.

---

## 10. Character voice rule

Do not make all characters speak the same polished English.

Preserve different voices, pressures, hesitations, silences, awkwardness, humor, and resistance.

Check especially:

- Sofia as the main living lens / newcomer;
- Ivar as seen from outside, not explained from inside;
- Thomas / Tomas as his own pressure and resistance;
- Marta as her own voice, not generic wit;
- Ayla as quiet presence without turning her into a Book II figure too early;
- group voices around food, work, awkwardness, silence, participation.

Dialogue should be natural but not sitcom-like.

---

## 11. Humor rule

Translate humor by function, not by dictionary.

A joke may be rephrased if literal translation kills it.

But do not make the joke:

- sharper than the original;
- too clever;
- too sitcom-like;
- too American;
- too British-witty;
- too explanatory;
- too obviously written as a joke.

The humor should feel like ordinary people in a strange, living situation.

---

## 12. Volume and density rule

Do not compress the text.

The English may be longer than the Russian if needed for natural rhythm.

Do not remove:

- repetitions that carry rhythm;
- objects;
- silences;
- physical details;
- awkward pauses;
- philosophical pressure;
- scene movement;
- strange or uneven phrasing that is functional.

If a phrase seems redundant, first check whether it is rhythm, pressure, or breath.

---

## 13. Object-world rule

Book I lives through things and conditions, not abstract statements.

Protect:

- bread;
- fire;
- water;
- wood;
- moss;
- hand;
- measure;
- dough;
- yeast;
- jar;
- house;
- snow / damp / grass / berries / mushrooms / rot / growth;
- feeding, exchange, warmth, timing, participation.

Do not replace objects with concepts.

---

## 14. Meta-trace caution

The controller performs the formal meta-trace audit, but the transcreator must already avoid harmful meta-language.

Be careful with:

```text
book
chapter
scene
page
author
reader
novel
story
text
narrative
plot
character
ending
prologue
epilogue
```

These words are not automatically forbidden, but they are dangerous when they refer to the book as a book, the chapter as a chapter, or the scene as a scene from outside the world.

Only use them if they clearly belong inside the scene: a real book, a told story, a page, a notebook, a performance, a script, a text someone is actually reading.

Do not write phrases like:

```text
the book could end here
the story wanted
the scene needed
it would make a good scene
the reader would
```

unless there is a clearly justified inner-world reason.

---

## 15. Transcreation draft workflow

When the author writes a short command such as:

```text
Prologue
Chapter 01
```

the transcreator should:

1. read `ru/Final/FINAL_INDEX.md`;
2. identify the latest approved Russian final source for the unit;
3. read that Russian final source;
4. create the English draft in `en/Drafts/`;
5. create a transcreation report in `en/Consultant/Transcreation_Reports/`;
6. answer briefly in Russian.

Do not create English final Markdown or DOCX until controller approval.

---

## 16. After controller approval

If the controller verdict is:

```text
approve
```

then the transcreator should:

1. create English final Markdown in `en/Final/`;
2. create temporary DOCX from the approved English final Markdown;
3. upload DOCX to Google Drive if upload permission works;
4. update or prepare English `FINAL_INDEX.md` if requested by author;
5. answer briefly.

Google Drive destination for chapter/unit DOCX:

```text
Radiance / Book_I_Sampo / EN_Final_DOCX
folder id: 1dnTMR-xrStypKqmEb5z648zTufG-uF_I
```

Google Drive destination for full book DOCX:

```text
Radiance / Book_I_Sampo / EN_Full_Book_DOCX
folder id: 18n2wU_Xlr-4IYenecLceh33MYphg_U1K
```

---

## 17. If controller requires changes

If the controller verdict is:

```text
approve after micro-corrections
```

or

```text
returned for another pass
```

then the transcreator must create a new version.

Do not overwrite the previous version.

Example:

```text
en/Drafts/Chapter_01_en_v1.md
```

becomes:

```text
en/Drafts/Chapter_01_en_v2.md
```

If a final file already exists, then:

```text
en/Final/Chapter_01_en_final_v1.md
```

becomes:

```text
en/Final/Chapter_01_en_final_v2.md
```

The previous version remains untouched.

---

## 18. Transcreation report format

Save reports to:

```text
Projects/Radiance/Books/Book_I_Sampo/en/Consultant/Transcreation_Reports/
```

Template:

```markdown
# Transcreation Report — Book I Sampo / [Unit]

Russian source:
[path]

English draft:
[path]

Version:
[Prologue_en_v1 / Chapter_01_en_v1 / etc.]

Status:
awaiting controller review

Transcreation approach:
[short note]

Key choices:
- [names]
- [terms]
- [humor decisions]
- [rhythm decisions]

Places requiring controller attention:
- [list or none]

Known risks:
- volume
- humor
- Sampo canon
- Ivar rule
- meta-trace risk
- English smoothness

Russian summary for author:
[short Russian summary]
```

---

## 19. Minimal chat output rule

The author wants minimal chat traffic.

Routine draft creation response:

```text
[Unit] — EN draft created.

Report saved.

Передай контролёру: [Unit]
```

After micro-corrections:

```text
[Unit] — EN v2 created.

Report saved.

Передай контролёру: [Unit]
```

After final DOCX upload:

```text
[Unit] — EN final created.

DOCX created and uploaded to Google Drive.
```

If upload to Google Drive fails, answer clearly:

```text
DOCX created, but Google Drive upload failed because [reason].
```

---

## 20. Test package

Start with:

```text
Prologue + Chapter 01
```

Do not process the full book until the test package confirms:

- English voice;
- file naming;
- GitHub paths;
- controller review;
- versioning;
- DOCX creation;
- Google Drive upload.

---

## 21. Final principle

The English version must be living English, but it must remain the same book.

```text
not smoother than needed
not shorter than needed
not cleverer than needed
not more explanatory than needed
not generic fantasy
not spiritual teaching
not technical summary
```

Sampo remains Sampo.

Creation remains larger than explanation.

Participation remains more important than possession.
