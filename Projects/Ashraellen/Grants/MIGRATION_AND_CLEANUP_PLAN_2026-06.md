# Grants migration and cleanup plan — 2026-06

Status: active cleanup plan  
Created: 2026-06-27  
Updated: 2026-06-27  
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
Projects/Ashraellen/Grants/START_HERE.md
Projects/Ashraellen/Grants/INDEX.md
Projects/Ashraellen/Grants/MASTER_Grants.md
Projects/Ashraellen/Grants/Outreach_Monitoring_2026.md
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
Projects/Ashraellen/Grants/legacy_grants_sources/
```

---

## 3. Files one level above the Grants workspace

These files may still exist under `Projects/Ashraellen/`:

```text
Projects/Ashraellen/Grants_Ashraellen_Master.md
Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md
Projects/Ashraellen/legacy_grants_sources/
```

Current status:

```text
Projects/Ashraellen/Grants_Ashraellen_Master.md           — redirect stub
Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md     — redirect stub
Projects/Ashraellen/legacy_grants_sources/                — old physical archive source folder, not active workspace
```

They should no longer be treated as the main active grant workspace.

---

## 4. Target migration

### 4.1. Master strategy

Old location:

```text
Projects/Ashraellen/Grants_Ashraellen_Master.md
```

Active location:

```text
Projects/Ashraellen/Grants/MASTER_Grants.md
```

Status:

```text
DONE: stable decisions consolidated into MASTER_Grants.md; old file turned into redirect stub.
```

Do not keep two active master files.

---

### 4.2. Outreach monitoring

Old location:

```text
Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md
```

Active location:

```text
Projects/Ashraellen/Grants/Outreach_Monitoring_2026.md
```

Status:

```text
PARTLY DONE: compact active outreach monitoring file created inside Grants; old file turned into redirect stub.
```

Note:

The full original journal was too large to migrate safely through the tool in one exact copy. The active Grants version contains the key operational monitoring data and points back to the old source history. Do not create partial copies under the same name.

---

### 4.3. Legacy grant source files

Old physical source folder:

```text
Projects/Ashraellen/legacy_grants_sources/
```

Target archive location:

```text
Projects/Ashraellen/Grants/legacy_grants_sources/
```

Status:

```text
PARTLY DONE: archive pointer created inside Grants. Physical copy of the large legacy files still requires a safe full-file method.
```

Expected legacy files:

```text
Grants_000.md
Grants_001.md
Grants_002.md
Grants_003.md
Grants_004.md
```

Rule:

Legacy files are archive sources, not active directives.

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
- [x] Create `Projects/Ashraellen/Grants/START_HERE.md` as the main entry point.
- [x] Turn `Projects/Ashraellen/Grants/INDEX.md` into compatibility pointer to START_HERE.
- [x] Update `Projects/Ashraellen/Grants/MASTER_Grants.md` as active grant master memory.
- [x] Create compact active `Projects/Ashraellen/Grants/Outreach_Monitoring_2026.md`.
- [x] Turn old `Projects/Ashraellen/Grant_Outreach_Monitoring_2026.md` into redirect stub.
- [x] Turn old `Projects/Ashraellen/Grants_Ashraellen_Master.md` into redirect stub.
- [x] Create `Projects/Ashraellen/Grants/legacy_grants_sources/README.md` as archive pointer.
- [ ] Physically copy large legacy source files into `Projects/Ashraellen/Grants/legacy_grants_sources/` using a safe full-file method.
- [ ] Review institution folders and add status to each.

---

## 9. Main rule

```text
All grant-specific work belongs in Projects/Ashraellen/Grants/.
Project-wide language and general memory may remain outside Grants/.
```
