# Grants migration and cleanup plan — 2026-06

Status: active cleanup plan  
Created: 2026-06-27  
Workspace: `Projects/Ashraellen/Grants/`

---

## 1. Purpose

This file explains how to make the Ashraellen grant workspace clear, stable and easy to use in future chats.

The goal is not to delete useful material. The goal is to prevent competing master files, scattered instructions and broken references.

---

## 2. Current intended architecture

Main grant workspace:

```text
Projects/Ashraellen/Grants/
```

Core files:

```text
Projects/Ashraellen/Grants/INDEX.md
Projects/Ashraellen/Grants/MASTER_Grants.md
```

Project-wide language rule outside Grants:

```text
Projects/Ashraellen/Ashraellen_Language_Rule.md
```

Institution folders:

```text
Projects/Ashraellen/Grants/EV/
Projects/Ashraellen/Grants/ISRF/
Projects/Ashraellen/Grants/Kone/
Projects/Ashraellen/Grants/Panoptykon/
Projects/Ashraellen/Grants/Templeton/
Projects/Ashraellen/Grants/Visegrad/
```

Working folders:

```text
Projects/Ashraellen/Grants/Inbox_From_Chats/
Projects/Ashraellen/Grants/Prompts/
```

---

## 3. Files currently outside the Grants workspace

These files may still exist under `Projects/Ashraellen/`:

```text
Projects/Ashraellen/Grants_Ashraellen_Master.md
Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md
Projects/Ashraellen/legacy_grants_sources/
```

They should no longer be treated as the main active grant workspace.

---

## 4. Target migration

### 4.1. Master strategy

Source / old location:

```text
Projects/Ashraellen/Grants_Ashraellen_Master.md
```

Target / active location:

```text
Projects/Ashraellen/Grants/MASTER_Grants.md
```

Action:

- consolidate stable decisions into `MASTER_Grants.md`;
- then turn the old file into a short redirect, or archive it.

Do not keep two active master files.

---

### 4.2. Outreach monitoring

Source / old location:

```text
Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md
```

Target / active location:

```text
Projects/Ashraellen/Grants/Outreach_Monitoring_2026.md
```

Action:

- copy / move the full monitoring journal into Grants;
- update references in `MASTER_Grants.md` and `INDEX.md`;
- then turn the old file into a short redirect, or archive it.

---

### 4.3. Legacy grant source files

Source / old location:

```text
Projects/Ashraellen/legacy_grants_sources/
```

Target / active archive location:

```text
Projects/Ashraellen/Grants/legacy_grants_sources/
```

Action:

- copy / move the legacy source folder into Grants;
- make clear that these files are archive sources, not active directives;
- then turn the old folder reference into a redirect if needed.

---

## 5. Do not move

The language rule should remain outside Grants because it applies to the whole Ashraellen project:

```text
Projects/Ashraellen/Ashraellen_Language_Rule.md
```

---

## 6. Future workflow

For any new grant / institution / application:

1. create or use one folder inside `Projects/Ashraellen/Grants/`;
2. keep institution-specific files inside that folder;
3. place raw chat imports in `Inbox_From_Chats/` first;
4. promote only stable decisions into `MASTER_Grants.md`;
5. record submissions and replies in the relevant `Submission_Log.md` or outreach monitoring file;
6. never start grant strategy from zero if `MASTER_Grants.md` already covers the issue.

---

## 7. Recommended status labels

```text
IDEA       — possible direction, not yet checked
RESEARCH   — eligibility and conditions being checked
DRAFT      — working draft exists
READY      — ready for review or submission
SENT       — submitted or sent
WAITING    — waiting for reply / result
ANSWERED   — reply received, requires processing
CLOSED     — finished / not relevant / rejected / no further action
ARCHIVED   — preserved for record only
```

---

## 8. Immediate checklist

- [x] Confirm that `Projects/Ashraellen/Grants/` exists.
- [x] Update `Projects/Ashraellen/Grants/INDEX.md` as the main workspace map.
- [x] Update `Projects/Ashraellen/Grants/MASTER_Grants.md` as active grant master memory.
- [ ] Create / move `Outreach_Monitoring_2026.md` into Grants.
- [ ] Move / mirror `legacy_grants_sources/` into Grants.
- [ ] Turn old top-level grant files into redirect stubs after safe migration.
- [ ] Review institution folders and add status to each.

---

## 9. Main rule

```text
All grant-specific work belongs in Projects/Ashraellen/Grants/.
Project-wide language and general memory may remain outside Grants/.
```
