# Cloud execution

**HB-AI-ENGINEERING-001 · v2.0**

## Choose by capability

Use an environment that can perform the requested operation and provide its evidence. Confirm access to the repository, tools, dependencies, network, secrets and required runtime before relying on it.

Cloud is suitable for supported builds, repository work and remote services. Local execution is needed when the task depends on the user's operating system, attached devices, USB equipment, desktop CAD/PLC tools or other unavailable hardware. A simulator or remote build does not establish hardware behavior.

Laptop-independent execution is possible only through a confirmed hosted runtime. Do not claim work will continue after the session, shutdown or disconnection unless a real execution mechanism supports that claim. Do not promise cloud token discounts or fabricated capacity.

## Bounded execution

Define a finite objective, acceptance checks, maximum useful retry strategy and a safe stopping condition. Use actual configured resource limits and provider quotas when known. Do not invent them or create endless loops, recursive agents or indefinite polling.

After two unchanged failures, inspect evidence, identify the likely cause and change the approach or report the blocker. Keep checkpoints before long operations and within the [five-minute recovery cadence](checkpoint-and-recovery.md).

Scheduled or unattended work requires an authorized scheduler, confirmed credentials and execution environment, durable status, observable results, failure handling and an explicit stopping policy. Creating a schedule is not proof that a run succeeded. Follow the user's requested cadence using supported controls; do not imply background work from a chat promise.

## Handoff and publication

Preserve the exact repository, branch, revision and pending work when moving between environments. A fresh environment must resume from verified durable state and follow the recovery procedure.

Perform already authorized deployment steps without asking again. Preserve the approved audience and settings. Verify the saved revision, deployment receipt and required user flows before reporting a deployment as successful. Environment changes never justify bypassing access restrictions or branch protections.

Store production secrets in approved secret mechanisms. Keep reusable policy here and runtime scripts, CI configuration and deployment implementation in the product repository.
