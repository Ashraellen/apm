# Public Thoughts — full transcreation / no reduction rule

Date: 2026-06-26  
Project: Ashraellen MainSite / Public Thoughts  
Status: active rule

## Rule

For all future multilingual Public Thoughts work, every language version must be created by full literary transcreation, not by summary, compression or shortened adaptation.

The Russian master text remains the authorial source.

Other language versions must preserve the full weight of the master text:

```text
meaning
structure
inner rhythm
central image
humor, where present
examples and scenes
philosophical density
emotional pressure
final turn / final strike
```

## No reduction

Future transcreation must not reduce the main text.

Do not remove:

```text
scenes
examples
comic turns
repetitions that create rhythm
slow buildup
contrast pairs
transitional paragraphs
final softening or final blow
```

A language version may change wording, syntax and idiom so that the text lives naturally in that language.

It may not shorten the work merely to make implementation easier.

## Difference between transcreation and compression

Allowed:

```text
literary rephrasing
idiomatic adaptation
local sentence rhythm
natural word order in the target language
minor cultural smoothing when literal form would sound dead
```

Not allowed:

```text
summarizing the full text
removing major examples
turning a long authorial passage into a short explanation
cutting the comic or dramatic mechanism
flattening the final turn
using technical constraints as a reason to reduce the authorial text
```

## Technical constraint rule

If a connector, editor, API, or commit operation blocks a long language page, do not solve it by reducing the text.

Use a safer technical method instead:

```text
retry with a smaller batch
create the file locally and upload once
split the implementation work into separate commits
use the latest successful same-type page as template
ask for a technical pause if needed
```

The text itself must remain complete.

## Existing multilingual pages 0019–0024

The already published multilingual pages for `0019–0024 / ДУГА 0004` may remain as they are.

They are accepted as the current implemented layer.

This rule governs future work from the next arc onward, starting with:

```text
0025–0030 / ДУГА 0005
```

unless the author explicitly decides to revise older language versions.

## Practical instruction for future chats

Before creating a new multilingual support-thought page:

```text
1. Read the Russian master text fully.
2. Preserve the complete authorial text in the target language.
3. Transcreate, do not summarize.
4. Keep every essential scene, example, image, rhythm and final turn.
5. If the implementation becomes technically difficult, solve the technical problem, not by shortening the text.
```

## Related references

```text
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Multilingual_Rollout_Decisions_2026-06-23.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Current_Status_Addendum_2026-06-26.md
```
