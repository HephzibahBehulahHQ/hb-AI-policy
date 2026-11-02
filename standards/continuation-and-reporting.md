# Hephzibah Behulah Global AI Engineering Agent Policy

**Policy ID:** HB-AI-ENGINEERING-001  
**Version:** 1.1  
**Applies to:** All Hephzibah Behulah products, repositories, Codex agents, AI coding assistants and automated engineering workflows.

This repository is the canonical source for AI-agent governance. Its policy documents take precedence over repository-local agent instructions except where an applicable legal, security, product-safety or authorized platform control is stricter.


## 11. CONTINUATION AND RECOVERY

Each product repository should maintain:

`docs/agent/PROJECT_STATUS.md`

`docs/agent/MILESTONES.md`

`docs/agent/DECISIONS.md`

`docs/agent/BLOCKERS.md`

`docs/agent/NEXT_TASKS.md`

These files must contain concise operational information, not copies of the entire master specification.

### PROJECT_STATUS.md

Record:

- Current milestone.
- Last verified commit.
- Implemented features.
- Test status.
- Current branch.
- Outstanding risks.
- Next recommended task.

### NEXT_TASKS.md

Record a prioritized list of approved, independent and actionable tasks.

### BLOCKERS.md

Record dependencies requiring the owner's approval, credentials, local hardware or third-party access.

### DECISIONS.md

Record significant architectural choices and their reasons.

### Resume protocol

At the beginning of a new session:

1. Read these progress files.
2. Check repository and branch state.
3. Verify recent commits and tests.
4. Identify the next approved task.
5. Continue without rebuilding completed features.

If the status files disagree with the actual repository, trust verified repository evidence and correct the documentation.


## 16. MANDATORY RESPONSE FORMAT

Use concise progress reports.

STATUS

- Done: Actual changes completed.
- Tested: Checks run, including failures and skipped tests.
- Model: Current model if verifiable; recommended reasoning level if relevant.
- Environment: Cloud or local, only if verified.
- Branch: Current working branch.
- Blocked: Unresolved dependencies or approvals.
- Next: One concrete next action.

Do not repeat the full policy or master specification in routine updates.


## 17. FINAL DIRECTIVE

Operate as a disciplined engineering agent.

Prefer cloud execution where genuinely available.

Continue approved work autonomously only within the capabilities and authorization of the execution platform.

Use the appropriate reasoning effort without pretending to change models.

Protect Git history and shared files.

Minimize unnecessary token consumption.

Produce functional, tested, traceable engineering software.

When execution stops, preserve enough verified state for the next session to resume efficiently.

**The objective is not uninterrupted AI activity. The objective is continuous, measurable delivery of correct and reliable software.**


## Response discipline

Use concise updates that state what actually changed, what was tested, what is blocked and the next action. Do not paste raw PDFs, HTML dumps, full chat history, full files or unchanged architecture plans unless asked. Prefer targeted references to specifications and changed files. Do not use an implementation preamble in place of completed work.

A normal update is:

STATUS

- Done: actual completed work
- Tested: passed, failed and skipped checks
- Blocked: unresolved dependency or approval
- Next: one concrete action

Detail is appropriate only when the requester asks for it or a blocker needs enough context to resolve. Reviewers should reject PR descriptions that restate full specifications, include generated/reformatted material without purpose, or claim completion without evidence.


When client-provided text is already clear plain text, treat it as the source: do not re-convert, reformat or re-summarize it unless asked. When a large source needs processing, use the smallest relevant clean Markdown excerpt rather than repeating raw material. Do not paste entire files unless requested. Routine PR descriptions should identify changed files and evidence, not reproduce the specification.
