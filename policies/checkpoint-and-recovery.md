# Checkpoint and recovery

**HB-AI-ENGINEERING-001 · v2.0**

## Recovery cadence

Begin the clock when useful work first changes. Make the first useful WIP commit and verified remote push within **5 minutes**. While changes continue, checkpoint and push changed work at intervals no greater than **5 minutes**, and before long operations, environment transitions, handoffs and other safe stopping boundaries.

Do not create empty commits or churn unchanged status merely to satisfy a timer. When nothing changed, retain the last verified receipt. A long operation must start from a recoverable checkpoint; arrange the next checkpoint if it will itself produce changing work.

Incomplete or failing work may be committed and pushed to an authorized work branch as clearly marked **WIP**. Record known failures. Run cheap checkpoint checks without waiting for full CI; full merge and release gates still apply before those actions.

## Safe synchronization

1. Inspect the working tree, selected files and staged diff; exclude secrets and unrelated work.
2. Coordinate shared writers using ownership or a lock. Record the branch and observed remote head.
3. Create a scoped commit. Use expected-SHA checks where supported and a normal fast-forward push; never force-push.
4. Read the intended remote branch back and verify it points to the exact pushed commit. A command exit code alone is insufficient.
5. Update the one current status with the local SHA, verified remote SHA, time and relevant check receipts.

If the remote moves concurrently, fetch and inspect it. Preserve both contributors' work and reconcile before another push. A later branch head that contains the pushed commit may establish backup through a verified ancestry check, but report that exact distinction rather than claiming head equality.

Record receipts without secrets. If the latest status update itself changes a tracked file after the push, say it is locally pending and include it in the next checkpoint; do not claim that update is already remote. A receipt may instead live in an authorized durable PR or task status without creating a self-referential commit cycle.

## Failure and offline exception

After two unchanged synchronization failures, diagnose and change the approach. At **10 minutes of unresolved synchronization**, stop new feature work. Repair synchronization, protect existing work and report the blocker. Do not continue building an unbounded unsynchronized change set.

When the user explicitly permits offline work, or the operating environment is demonstrably offline, record an **offline exception**: reason, last verified remote SHA, local checkpoint location, known durability limits and the condition for resuming synchronization. Continue only within the agreed bounded offline scope; absent an agreed continuation scope, stop new feature work at the ten-minute boundary. Do not treat a network error or access denial as permission to bypass controls.

Use honest states: saved locally, verified remotely, synchronization pending or remote state unknown. Local ephemeral storage is not a durable remote backup. On reconnection, inspect the current remote head, reconcile and verify the exact commit before claiming synchronization.

Session-end hooks and shutdown callbacks are best effort. They cannot guarantee that work is backed up; periodic verified checkpoints provide recovery evidence.

## Recovery and adoption validation

Checkpoint mechanisms belong in the product repository. Before relying on them, document and exercise this nonexecutable validation plan:

| Scenario | Acceptance evidence |
| --- | --- |
| Normal changed work | Useful first push within five minutes; later changed checkpoints meet cadence |
| Failing feature check | Marked WIP reaches the work branch with failure recorded; merge/release remains gated |
| Long operation or handoff | Latest useful change is verified remotely before the operation |
| Remote advances concurrently | Stale write fails safely; both contributions survive reconciliation |
| Interrupted push or unavailable network | Remote state is checked; uncertainty and ten-minute stopping rule are honored |
| Secret or unrelated file in the working tree | Unsafe or unowned paths are excluded; no bypass or force push |
| Fresh checkout recovery | Another clean environment restores the checkpoint, follows current status and reproduces the recorded next step |

Record which scenarios were actually tested, their revision and results. Untested scenarios remain **NOT TESTED**. Policy adoption alone does not prove the product's recovery mechanism works.
