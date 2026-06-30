# REPORT NNN — <Task title>

Date: YYYY-MM-DD
Executor: <chat/session if known>
Command file used: `COMMAND_NNN_<name>.md`
Status: draft / complete / blocked / needs approval

## 1. Files read

List every repository file read for this report.

```text
Ashraellen/apm:
- ...

Ashraellen/ashraellen:
- ...
```

If a required file was missing or unreadable, record it here.

## 2. Scope performed

State exactly what was done.

```text
- audit only
- planning only
- files changed
- no files changed
```

## 3. Findings

Summarize findings by category.

Use short subsections such as:

```text
### Workflow
### Formula pages
### Metadata quality
### Legacy URLs
### Sitemap / IndexNow
### Risks
```

## 4. Proposed changes

List proposed changes without ambiguity.

For every proposed change, include:

```text
- target repository
- target file(s)
- type of change
- reason
- risk level: low / medium / high
- whether approval is required before implementation
```

## 5. Files changed

If this was an approved implementation command, list exact changed files and commit hashes.

If no files were changed, write:

```text
No files changed.
No commits created.
```

## 6. Validation performed

List validations performed.

Examples:

```text
- read back changed files
- ran or inspected metadata audit
- checked representative HTML pages
- checked workflow syntax by inspection
- checked sitemap policy by inspection
```

If validation was not performed, explain why.

## 7. Open questions

List only questions that block the next phase.

Do not include broad speculation.

## 8. Decision request

End with one or more of these exact labels:

```text
REQUEST_APPROVAL_WORKFLOW_SPLIT
REQUEST_APPROVAL_FORMULA_STATICIZATION
REQUEST_APPROVAL_METADATA_QUALITY_PASS
REQUEST_APPROVAL_LEGACY_URL_POLICY
REQUEST_MORE_ARCHITECT_REVIEW
```

Add a short one-paragraph explanation after each requested decision.

## 9. Recommended next command

Propose the next command file title and the intended scope.

Example:

```text
Recommended next command:
COMMAND_002_Workflow_Split.md

Scope:
Make sitemap workflow safe by separating permanent automatic tasks from manual emergency repair tasks.
```
