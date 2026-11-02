# Product agent instructions template

> Copy this file into a product repository and replace bracketed values. Do not place product code or secrets in this template.

# [Product name] agent guidance

## Authority and startup

1. Read the product README, this file, the active specification and current status records.
2. Read the applicable [global AI policy](https://github.com/HephzibahBehulahHQ/hb-AI-policy), [design system](https://github.com/HephzibahBehulahHQ/hb-design-system) and division guidance.
3. Inspect the actual branch, uncommitted work, recent commits, tests and open review work.
4. Resume the next approved, bounded milestone from verified project state.

The global policy governs agent operation. The product specification governs product behavior. The design system governs visual assets and reusable components. Division guidance applies only to its domain.

## Required practice

Use an isolated branch or worktree; implement a bounded milestone; run applicable checks; commit verified work; prepare a pull request; and update concise project records under `docs/agent/`:

- `PROJECT_STATUS.md`
- `MILESTONES.md`
- `DECISIONS.md`
- `BLOCKERS.md`
- `NEXT_TASKS.md`

Use only implemented and authorized integrations. Validate tool inputs, protect secrets, preserve user control and report limitations honestly. Do not claim a model switch, test, deployment, push, certification or external integration without evidence.

## Reporting

STATUS

- Done:
- Tested:
- Model: verified model or recommendation only
- Environment: verified cloud/local state only
- Branch:
- Blocked:
- Next:
