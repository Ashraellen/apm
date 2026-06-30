# MainSite Editorial Stabilization — Exchange Workspace

Date opened: 2026-06-30
Project: Ashraellen MainSite
Live repository: `Ashraellen/ashraellen`
Memory repository: `Ashraellen/apm`
Status: active coordination workspace

## Purpose

This directory is the repository-based exchange space between:

```text
- Architect / reviewer chat
- Executor chat
- User, with minimal manual transfer between chats
```

The goal is to coordinate the editorial stabilization after the 2026-06-30 static metadata repair without requiring the user to copy long reports between chats.

## Communication rule

Instructions and reports must be exchanged through repository files, not through long pasted chat messages.

The user may simply tell the executor chat:

```text
Read the current command file in:
Projects/Ashraellen/MainSite/Editorial_Stabilization/

Work only according to that file and write your report back into the same workspace.
```

The user may then tell the reviewer chat:

```text
Please review the latest executor report in:
Projects/Ashraellen/MainSite/Editorial_Stabilization/
```

## Current command file

Executor must start with:

```text
COMMAND_001_Editorial_Stabilization_Plan.md
```

## Report template

Executor must write reports using:

```text
REPORT_TEMPLATE.md
```

Recommended report filename pattern:

```text
REPORT_001_Editorial_Stabilization_Plan.md
REPORT_002_<short-task-name>.md
```

## Working roles

### Architect / reviewer chat

Responsible for:

```text
- defining command files;
- reviewing reports;
- deciding whether work is accepted, rejected, paused or narrowed;
- protecting site architecture and editorial principles;
- preventing broad automatic repair scripts from becoming the permanent editorial model.
```

### Executor chat

Responsible for:

```text
- reading the command file;
- reading the required source files;
- performing only the requested work;
- making repository changes only inside the allowed scope;
- writing concise but complete reports into this directory;
- asking for approval through a report when a decision exceeds the command scope.
```

### User

The user should not need to transfer long reports manually.

The user only needs to move short commands between chats, such as:

```text
Executor: read command 001 and write report 001.
Reviewer: read report 001 and give the next command.
```

## Non-negotiable constraints

```text
- Do not manually edit sitemap.xml as normal workflow.
- Do not create a second sitemap generator.
- Do not use client-side JavaScript to repair SEO/social metadata after page load.
- Do not treat broad metadata repair scripts as the permanent editorial model.
- Do not mix Public Posts / Formula with Public Thoughts.
- Do not bypass the site-wide transcreation rule for public multilingual content.
- Do not change APM canon files unless explicitly requested.
- Do not make destructive changes without a report and approval.
```

## Required source files for executor

Before starting any task, executor must read:

```text
Projects/Ashraellen/MainSite/INDEX.md
Projects/Ashraellen/WEB.md
Projects/Ashraellen/Website_Static_Metadata_Repair_2026-06-30.md
Projects/Ashraellen/MainSite/Decisions/Site_Wide_Transcreation_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Technical/Sitemap_Automatic_Generation_Rule_2026-06-28.md
Projects/Ashraellen/MainSite/Decisions/Public_Posts_Formulas_Working_Rule_2026-06-26.md
Projects/Ashraellen/MainSite/Decisions/Public_Thoughts_Working_Reference_2026-06-26.md
```

## Review cycle

```text
1. Reviewer writes or updates COMMAND_NNN.
2. Executor reads the command and required sources.
3. Executor performs allowed work or prepares a plan if approval is required.
4. Executor writes REPORT_NNN.
5. Reviewer reads REPORT_NNN directly from the repo.
6. Reviewer writes next command or acceptance note.
```

## Current first goal

Prepare editorial stabilization so the site moves from emergency automatic metadata repair toward stable page-specific, transcreated, static metadata and self-contained public content pages.
