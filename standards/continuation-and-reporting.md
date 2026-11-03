# Continuation and reporting

**HB-AI-ENGINEERING-001 · v2.0**

## One current status

Each product identifies one current status location, such as `PROJECT_STATUS.md` or an authorized durable task/PR record. Maintain a compact account of the objective, acceptance state, branch, local revision, last verified remote revision and time, relevant test/deployment receipts, known failures and next bounded action.

Keep historical decisions or reference documents only when useful; do not maintain several competing current plans, blocker lists or status summaries. Receipts must distinguish what exists locally, what was verified remotely, what passed and what was integrated or deployed.

At continuation, read the current status once and inspect actual Git or runtime state. Prefer fresh verified evidence over stale status. Preserve completed work, resolve discrepancies, then reason about the next task. Refresh only affected evidence when it changes. Do not reload the entire history or repeat the plan.

## Token discipline and project continuation

Use targeted file reads and relevant excerpts. Do not dump raw PDFs, HTML or conversation histories. Convert unstructured material into clean Markdown only when needed; clean pasted text is used as-is unless the user requests a transformation.

Do not rewrap or resummarize clean input, repeat specifications or reproduce completed explanations. Keep implementation preambles minimal and show changed files or relevant changed lines only. Complete requested deliverables remain available in their proper artifact or repository.

A new session is a continuation from verified prior state, not a reason to redo accepted work. Follow [checkpoint and recovery](../policies/checkpoint-and-recovery.md) before handoff or long operations.

## Routine reporting

Routine progress and completion reports contain **only** this structure:

```text
STATUS
- Done: ...
- Tested: ...
- ESTIMATED FINISH TIME: ...
- ETA: ...
- Next: ...
```

Put blockers, their source and the required resolution in Done, Tested or Next. Do not add a separate Blocked field, extra headings, plans or commentary. Give additional explanation only when the user requests detail.

Done states the actual acceptance stage and changed scope. Tested names meaningful checks, the relevant revision and any **NOT TESTED** limitation. Next gives the next bounded action or confirms completion.

ESTIMATED FINISH TIME covers the **entire requested task**, expressed in hours or minutes when supportable; otherwise say **unknown** and give the missing dependency in Next. Never use the estimate for an initial partial result as the full-task finish.

ETA is a dated estimate in **Europe/Berlin**, including the local time and date when supportable; otherwise say **pending**. Account for daylight saving using the actual zone. Estimates are not guarantees. Do not invent an ETA, elapsed duration or successful completion to fill the format. When all work is complete, state zero remaining time and the verified completion time if known; otherwise keep ETA pending.
