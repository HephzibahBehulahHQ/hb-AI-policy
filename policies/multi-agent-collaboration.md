# Hephzibah Behulah Global AI Engineering Agent Policy

**Policy ID:** HB-AI-ENGINEERING-001  
**Version:** 1.1  
**Applies to:** All Hephzibah Behulah products, repositories, Codex agents, AI coding assistants and automated engineering workflows.

This repository is the canonical source for AI-agent governance. Its policy documents take precedence over repository-local agent instructions except where an applicable legal, security, product-safety or authorized platform control is stricter.


## 7. MULTI-AGENT COLLABORATION

Multiple agents may work concurrently, but each must have clearly separated responsibilities.

### Workspace isolation

Each agent must use an isolated cloud workspace, working directory or Git worktree as appropriate.

Each agent must use its own task branch.

Suggested branch naming:

`agent/<product>/<issue-or-milestone>-<short-description>`

Example:

`agent/adiguneplanai/m03-schematic-editor`

Never allow two agents to edit the same working tree concurrently without an explicit coordination mechanism.

### Shared resources

Before modifying shared files, design tokens, schemas, APIs or configuration:

1. Identify affected repositories and agents.
2. Check for open changes or conflicting branches.
3. Prefer a separate pull request for shared changes.
4. Document compatibility requirements.
5. Avoid breaking other products.
6. Coordinate integration before merging.

Do not use destructive Git commands to resolve collaboration problems.

### Conflict handling

If a merge conflict occurs:

- Preserve both sides.
- Identify the intended behavior.
- Resolve with tests.
- Request review for ambiguous or high-risk conflicts.
- Never discard another agent's work merely to complete a merge quickly.
