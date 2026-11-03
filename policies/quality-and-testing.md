# Quality and testing

**HB-AI-ENGINEERING-001 · v2.0**

## Acceptance before expansion

Work in bounded milestones with an objective, affected scope, dependencies, acceptance criteria and risks. Establish a useful end-to-end user flow early, then extend it in the product's approved order. Do not confuse an initial partial result with completion of the full task.

A functional feature performs its promised behavior using the intended inputs, outputs and persistence. Dummy content, placeholders, hardcoded success messages and fake integrations must never be represented as finished functionality. Label deliberate fixtures, prototypes and simulations clearly. Record missing external access as a limitation.

## Verification tiers

| Tier | Purpose and evidence |
| --- | --- |
| Checkpoint | Cheap inspection of staged scope and secret risk, plus quick syntax or formatting checks where useful. Record known failures. Permit clearly marked WIP backup without waiting for full CI. |
| Feature | Focused tests of changed behavior and affected interfaces; relevant type, lint, unit, integration or build checks. Test meaningful failure cases and regressions. |
| Merge / release | All required product and branch-protection gates on the exact merge or release candidate SHA, plus acceptance checks appropriate to the release. |

Checkpoint backup and release approval are separate decisions. A failing test does not justify losing work, and a successful backup does not authorize integration or release.

After a candidate changes, rerun affected checks and every gate required for its new SHA. If a merge queue or merge operation creates another revision, verify the required checks against the actual integrated or release candidate. Deploy the verified artifact or revision and record the production receipt.

Reuse valid results for the same revision where the gate allows it. Avoid duplicate CI triggers; cancel obsolete owned runs when cancellation is safe and does not cancel another contributor's work. Do not weaken required gates to save time.

## Test what users experience

Choose checks according to risk; avoid tests that merely restate trivial implementation details. For applications, exercise actual user flows, persistence, errors and recovery. Verify real integrations when access exists and distinguish mock coverage from live coverage.

For UI changes, inspect functional behavior, keyboard and focus use, labels and accessible names, readable contrast, responsive layouts and visual quality at relevant screen sizes. Automated checks complement direct inspection. A successful build or screenshot alone is insufficient.

After two unchanged failures, diagnose the cause and change the repair or test strategy before retrying. Mark unrun checks **NOT TESTED**, explain why and identify the next verification step.

## Engineering references and rights

For electrical, numerical or other consequential domain features, record the applicable standard edition, manufacturer source, assumptions, units, operating conditions and reference calculations. Verify specifications rather than inventing ratings, tolerances, formulas or safety claims.

Respect copyright, licenses and access rights for standards, manufacturer material, software and assets. Cite or link authoritative references; do not copy restricted source beyond authorized use.

Distinguish demonstration, numerical/reference validation, standards-informed analysis, hardware-tested behavior and independently certified compliance. Evidence at one level does not prove another. Claim hardware testing or certification only with actual records.

## Completion evidence

A milestone is complete when the agreed behavior works, relevant checks pass, required reviews or integration steps are confirmed, documentation reflects the change and remaining limitations are explicit. Use the [acceptance states](governance.md#evidence-and-acceptance); report the full task's remaining effort honestly.
