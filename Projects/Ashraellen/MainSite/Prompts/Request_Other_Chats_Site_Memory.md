# MainSite Old Chat Import Workflow

Status: canonical workflow file
Updated: 2026-06-22

This file is the detailed instruction for importing website memory from older chats into the Ashraellen APM repository.

## 1. Target

Extract only information related to the Ashraellen main website / ashraellen.com and save it as a Markdown file.

## 2. Repository and folder

Repository:

`Ashraellen/apm`

Target folder:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/`

## 3. File naming

Use the next free short filename:

`MS_01.md`, `MS_02.md`, `MS_03.md`.

Check the target folder first. If `MS_01.md` and `MS_02.md` already exist, use `MS_03.md`.

If the folder cannot be checked, use temporary name `MS_XX.md` and mention this in the report.

## 4. Collect

Collect site-related material only:

- accepted decisions;
- completed or prepared work;
- pages, sections and structure;
- languages and translations;
- technical notes: GitHub Pages, paths, URLs, redirects, sitemap, JSON-LD, SEO, llms.txt, PWA, language auto-detection, manual language choice;
- grant and institutional positioning;
- ready website text fragments;
- open tasks;
- outdated, rejected or uncertain ideas;
- material to move later into `MASTER_MainSite.md`.

Keep confirmed decisions separate from discussion, drafts, uncertain notes and rejected ideas.

## 5. File template

```markdown
# MS_NN — MainSite chat memory

Source chat:
Date of extraction:
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
```

## 6. Final report

After saving the file, the chat report should be compact:

- filename;
- full path;
- commit SHA if available;
- one or two lines about what was collected.

If saving is impossible, provide a short reason and the file text for manual saving.
