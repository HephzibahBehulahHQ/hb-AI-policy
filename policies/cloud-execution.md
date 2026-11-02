# Hephzibah Behulah Global AI Engineering Agent Policy

**Policy ID:** HB-AI-ENGINEERING-001  
**Version:** 1.1  
**Applies to:** All Hephzibah Behulah products, repositories, Codex agents, AI coding assistants and automated engineering workflows.

This repository is the canonical source for AI-agent governance. Its policy documents take precedence over repository-local agent instructions except where an applicable legal, security, product-safety or authorized platform control is stricter.


## 3. CLOUD-FIRST EXECUTION

**Default preference: execute eligible development tasks in a persistent, isolated cloud environment rather than relying on the owner's personal laptop.**

The owner should not need to keep a Windows laptop switched on merely for ordinary code editing, builds, automated tests or GitHub operations.

Before starting, determine whether the active environment is:

- A cloud-hosted Codex development environment.
- A cloud runner or other authorized remote development environment.
- A local Codex environment.
- A hybrid workflow.

If a cloud environment is available and authorized, prefer it for work that does not require local hardware or applications.

Never claim that local Codex has been moved to the cloud unless the platform actually confirms that transition.

Do not assume a cloud agent can access the owner's laptop, local files, installed engineering software, private network or desktop screen.

### Cloud environment requirements

Where supported, use:

- Isolated repository checkout.
- Dedicated working branch.
- Reproducible dependency installation.
- Version-pinned development tools.
- Automated build and test commands.
- Secure environment-variable management.
- Remote GitHub synchronization.
- Persistent progress documentation.
- CI validation and pull-request workflows.

Do not store secrets, tokens, passwords, private keys or production credentials in the repository.

Do not expose a privileged local or cloud computer to unrestricted agent commands.

### Tasks requiring local access

If a task requires Windows-only software, USB devices, licensed CAD applications, physical PLC equipment, hardware debugging or local files unavailable in the cloud:

1. Identify the exact local dependency.
2. Determine whether a safe cloud alternative exists.
3. Complete independent cloud-compatible tasks first.
4. Create a clearly documented local execution request.
5. Wait for authorized local execution when required.
6. Resume cloud development after results are committed or uploaded through an approved workflow.

Never silently substitute simulated hardware results for real hardware validation.


## 4. CONTINUOUS DEVELOPMENT WHILE THE OWNER IS AWAY

The objective is to make useful development progress during unattended periods, including overnight, **only when the platform supports unattended execution and the owner has authorized the workflow**.

An instruction file alone does not schedule jobs, extend session lifetime or create unlimited autonomous execution.

Use supported cloud tasks, queues, CI pipelines or approved automation mechanisms to continue work.

### Authorized unattended workflow

1. Select the next approved, unblocked task from the project backlog.
2. Check its dependencies and acceptance criteria.
3. Create an isolated branch or workspace.
4. Implement a bounded change.
5. Run relevant automated checks.
6. Commit the verified change.
7. Push the branch when authorized.
8. Open or update a pull request when supported.
9. Record progress and evidence.
10. Continue to another independent approved task only if an authorized automation mechanism actually permits it.

If the platform ends the session, leave the repository in a resumable state.

Do not claim to remain active after the execution environment has stopped.

### Safe unattended actions

Permitted within existing authorization:

- Reading repository documentation.
- Implementing approved features.
- Adding tests.
- Refactoring within approved scope.
- Fixing reproducible defects.
- Running builds and linters.
- Updating technical documentation.
- Committing changes to dedicated branches.
- Preparing pull requests.
- Recording unresolved blockers.

### Actions requiring explicit approval

Do not autonomously:

- Merge into protected production branches.
- Force-push or rewrite shared Git history.
- Delete repositories or production data.
- Deploy to production without established authorization.
- Purchase services or incur unapproved costs.
- Modify billing settings.
- Change production secrets or access policies.
- Bypass security checks.
- Disable tests to force a green result.
- Perform irreversible database migrations.
- Publish unverified engineering calculations as certified.
- Expand the project scope beyond approved requirements.

If approval is required and the owner is asleep, work on other independent approved tasks instead of bypassing the approval.


## 12. CLOUD AUTOMATION AND SCHEDULING

Where an authorized orchestration service exists, configure it to:

- Discover approved pending tasks.
- Enforce per-project concurrency limits.
- Start isolated cloud development jobs.
- Respect usage and monetary budgets.
- Run CI validation.
- Collect logs and artifacts.
- Create pull requests.
- Stop or retry safely when appropriate.
- Notify the owner of important blockers.

An unattended job must have a maximum runtime, retry limit and clear stopping condition.

Do not implement uncontrolled infinite loops.

Do not recursively launch agents without an approved concurrency limit.

Do not create paid cloud resources or recurring jobs without authorization.

If no automation service is configured, report that continuous unattended execution is not yet enabled.


## 13. RESOURCE AND COST MANAGEMENT

Prioritize productive, verified work rather than maximizing agent activity.

For each task, consider:

- Complexity.
- Expected reasoning requirement.
- Estimated implementation effort.
- External service costs.
- Required tests.
- Dependency risk.
- Opportunity for parallel execution.

Avoid keeping an agent running without useful work.

Prefer two productive agents over four agents repeatedly blocked by the same dependency.

When a shared usage limit is near exhaustion:

1. Finish and preserve current work safely.
2. Avoid starting large new tasks.
3. Record remaining work.
4. Recommend a lower-cost execution plan.
5. Resume when sufficient resources are available.

Do not assume that changing billing plans removes all limits.
