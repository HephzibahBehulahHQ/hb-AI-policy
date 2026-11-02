# Hephzibah Behulah Global AI Engineering Agent Policy

**Policy ID:** HB-AI-ENGINEERING-001  
**Version:** 1.1  
**Applies to:** All Hephzibah Behulah products, repositories, Codex agents, AI coding assistants and automated engineering workflows.

This repository is the canonical source for AI-agent governance. Its policy documents take precedence over repository-local agent instructions except where an applicable legal, security, product-safety or authorized platform control is stricter.


## 8. MILESTONE-BASED EXECUTION

Every feature must be broken into bounded, testable milestones.

A milestone should contain:

- Objective.
- Scope.
- Dependencies.
- Acceptance criteria.
- Implementation tasks.
- Tests.
- Known risks.
- Definition of done.

Do not begin with an uncontrolled request to build the entire application in one uninterrupted operation.

Complete the smallest meaningful vertical slice first.

For engineering applications, prioritize:

1. Working project foundation.
2. Functional workspace and navigation.
3. Canonical engineering data model.
4. Real editor interactions.
5. Connectivity and validation.
6. Calculations.
7. 3D integration.
8. Exports and persistence.
9. AI-assisted workflows.
10. Expanded verified project libraries.

Use the product-specific implementation specification as the authoritative source for exact feature scope and milestone order.


## 9. TESTING AND ENGINEERING VALIDATION

No feature is complete simply because its interface renders.

Every milestone must include applicable checks:

- Type checking.
- Linting.
- Unit tests.
- Integration tests.
- Build verification.
- End-to-end interaction tests.
- Security checks.
- Accessibility checks.
- Regression tests.
- Engineering reference-case validation.

For electrical engineering software, distinguish clearly between:

- Demonstration examples.
- Numerically verified calculations.
- Standards-informed engineering workflows.
- Hardware-tested behavior.
- Certified or independently validated functionality.

Do not invent manufacturer specifications, component ratings, test evidence or compliance claims.

If a test cannot be performed, mark it as **NOT TESTED**, explain why and document what remains necessary.

Do not use mock outputs as proof that real calculations or integrations work.


## 15. DEFINITION OF DONE

A task is complete only when:

1. The requested behavior is implemented.
2. Relevant tests have been executed.
3. Results are accurately reported.
4. No known critical regression has been introduced.
5. Documentation is updated where necessary.
6. Changes are committed to the correct branch.
7. The work is available for review through the authorized workflow.
8. Remaining limitations are documented.

A successful build alone is not sufficient proof of functional completion.
