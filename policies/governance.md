# Governance

**HB-AI-ENGINEERING-001 · v2.0**

## Authority and adoption

This policy applies where a user or repository owner explicitly adopts it. System and developer instructions, runtime permissions and applicable user instructions remain authoritative. Respect branch protections and access controls. Product rules may add justified domain, legal, security or safety requirements; resolve conflicts according to the actual instruction hierarchy.

Adoption records must identify the policy version and an actual immutable commit SHA or release tag resolved from this repository. Do not invent a tag, silently follow a moving branch, or present a link as a global installation. Upgrades require an explicit recorded adoption decision.

## Work within a bounded task

Before changing work, read the product entrypoint and its one current status once. Inspect the actual branch, working tree and relevant source or evidence. Read additional policy and specifications only when the task needs them. Identify the requested outcome, affected scope, acceptance criteria, dependencies and stopping conditions. Use verified prior state to reason about the next action; do not restart completed work or repeat the full plan.

Complete authorized work through its agreed acceptance state. Routine commits, pushes, PR creation or updates and deployments already covered by standing permission proceed without another conversational permission request. Authorization has scope: do not infer permission for a new audience, spend, destructive change or unrelated product. Explain a real approval or access blocker and its source when one prevents progress.

## Corporate and repository responsibilities

The organizational relationship is **Hephzibah Behulah → Division → Product**.

| Responsibility | Canonical reference |
| --- | --- |
| Corporate representation | [HephzibahBehulahHQ.github.io](https://github.com/HephzibahBehulahHQ/HephzibahBehulahHQ.github.io) |
| Shared agent policy | [hb-AI-policy](https://github.com/HephzibahBehulahHQ/hb-AI-policy) |
| Design identity, tokens and approved assets | [hb-design-system](https://github.com/HephzibahBehulahHQ/hb-design-system) |
| Electrical division | [hb-elektroniker](https://github.com/HephzibahBehulahHQ/hb-elektroniker) |
| Trading division | [hb-trading](https://github.com/HephzibahBehulahHQ/hb-trading) |
| AI division | [hb-artificial-intelligence](https://github.com/HephzibahBehulahHQ/hb-artificial-intelligence) |
| Evangelism division | [hb-evangelism](https://github.com/HephzibahBehulahHQ/hb-evangelism) |
| Politics division | [hb-politics](https://github.com/HephzibahBehulahHQ/hb-politics) |

Follow the [ownership standard](../standards/repository-ownership.md). Use each product's approved scope, language and roadmap. English, German, Yoruba and Nigerian Pidgin apply where the product's requirements adopt them; electrical examples and division requirements are not universal product defaults.

## Evidence and acceptance

Report only observed capabilities, tests, integrations and publication results. Clearly distinguish:

| State | Required evidence |
| --- | --- |
| Saved | Identified local file or commit exists |
| Synchronized | Exact commit verified at the intended remote branch |
| Verified | Named checks passed against the identified candidate |
| Integrated | Merge receipt and resulting target revision confirmed |
| Deployed | Deployment succeeded for the identified revision; required production checks completed |
| Complete | Every agreed acceptance criterion is satisfied, with material limitations recorded |

One state does not establish the next. A PR, green build or reachable page alone does not prove completion. Use [quality and testing](quality-and-testing.md) and the [reporting standard](../standards/continuation-and-reporting.md) for the evidence needed.
