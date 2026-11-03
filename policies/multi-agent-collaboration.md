# Multi-agent collaboration

**HB-AI-ENGINEERING-001 · v2.0**

## Default and justification

Use one implementer by default. Add a specialist for a bounded independent task such as reference research, a focused review or a separate module when it saves time or improves correctness. Do not split trivial work, ask several agents to repeat the same broad analysis or create an unbounded agent tree.

Every delegated task states the outcome, allowed files, inputs, acceptance evidence, time or stopping boundary and how to return results. Share only the relevant context and verified state.

## Ownership and synchronization

Give each writer a distinct branch or isolated worktree when possible. A useful branch convention is `agent/<product>/<issue-or-milestone>-<short-description>`; follow established product conventions where present.

Assign one owner to a shared file or interface at a time. Use coordination or locks before overlapping edits. A dedicated synchronizer may commit combined work only with explicit ownership and contributor coordination; otherwise each writer checkpoints its owned scope.

Preserve other contributors' work. Never overwrite, discard, force-push or resolve a conflict by blindly choosing one side. Inspect both intentions, retain compatible changes and test the combined behavior. Ask only when an actual unresolved product decision remains.

## Integration

The lead implementer owns final integration and evidence. Review changed files, reconcile interface or schema changes, and refresh the candidate revision after integration. Required merge or release checks must match that candidate.

Each writer follows [checkpoint and recovery](checkpoint-and-recovery.md). A returned agent answer or session-end hook is not a backup. Report whether results are local, synchronized, verified or integrated with exact receipts; do not imply that another agent's claim independently verifies the work.

Stop duplicate or obsolete owned work when safe. Keep one current product status and use the [routine report format](../standards/continuation-and-reporting.md#routine-reporting).
