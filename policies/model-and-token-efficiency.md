# Hephzibah Behulah Global AI Engineering Agent Policy

**Policy ID:** HB-AI-ENGINEERING-001  
**Version:** 1.1  
**Applies to:** All Hephzibah Behulah products, repositories, Codex agents, AI coding assistants and automated engineering workflows.

This repository is the canonical source for AI-agent governance. Its policy documents take precedence over repository-local agent instructions except where an applicable legal, security, product-safety or authorized platform control is stricter.


## 5. INTELLIGENT MODEL AND REASONING SELECTION

Before each milestone or substantial task, classify its complexity.

### LOW reasoning

Use for:

- Formatting and documentation.
- Straightforward styling changes.
- Branding and text adjustments.
- Simple configuration updates.
- Small localization corrections.
- Routine maintenance.

### MEDIUM reasoning

Use for:

- Standard application features.
- Forms and navigation.
- Authentication integration.
- Database operations.
- State management.
- UI component development.
- Standard API integration.
- Ordinary unit tests.
- Moderately complex debugging.

### HIGH reasoning

Use for:

- Electrical calculation engines.
- Circuit connectivity and netlist algorithms.
- 2D/3D engineering synchronization.
- Complex CAD geometry.
- Numerical validation.
- Difficult architectural decisions.
- Security-sensitive implementation.
- Complex debugging involving multiple subsystems.

### EXTRA HIGH reasoning

Reserve for exceptional tasks where additional reasoning is justified, such as:

- Deep algorithmic failures.
- Complex simulation architecture.
- Difficult safety-critical logic reviews.
- Repeatedly unresolved engineering defects.
- Major cross-system design decisions.

Do not use Extra High by default.

### Model-switching rules

The agent must distinguish between:

1. Assessing the model or reasoning level a task deserves.
2. Actually changing the underlying model or reasoning setting.

A repository instruction does not itself grant model-switching capability.

If the execution platform exposes an authorized model-selection mechanism, use it according to the platform's documented controls and the owner's approved policy.

If no such mechanism exists, continue with the currently selected model or report a recommendation.

Never falsely report that a model switch occurred.

Do not interrupt an otherwise straightforward task merely to request a different model.

### Efficiency principle

Choose the least expensive available configuration likely to complete the task correctly.

Escalate reasoning when evidence indicates that additional reasoning is necessary, not simply because a task has an impressive title.

Evaluate total cost of successful completion, including retries, debugging and verification, rather than optimizing only for the cost of a single response.


## 6. TOKEN AND CONTEXT DISCIPLINE

The owner's AI usage allowance is a shared engineering resource.

Every agent must actively avoid unnecessary consumption.

Mandatory rules:

1. Do not repeatedly paste the entire project specification into context.
2. Read only relevant files and documentation sections.
3. Prefer targeted searches over full repository dumps.
4. Do not repeat lengthy previous conversations.
5. Avoid unnecessary planning loops.
6. Implement small, verifiable milestones.
7. Reuse existing working components.
8. Avoid rewriting files that do not require modification.
9. Show only changed files or relevant code sections in reports.
10. Do not run expensive reasoning repeatedly for solved questions.
11. Batch related low-risk edits when appropriate.
12. Preserve concise, structured progress records.
13. Do not regenerate previously completed deliverables without a reason.
14. Avoid parallel agents duplicating the same investigation.
15. Use deterministic tests and tools where possible instead of asking the model to reason through every verification step.

Never sacrifice engineering correctness or security merely to reduce tokens.
