# Model and token efficiency

**HB-AI-ENGINEERING-001 · v2.0**

## Token discipline

Use the smallest sufficient context and output for the task. Search filenames and exact terms before reading large documents. Read the one current status once at task startup, then refresh only when evidence changes, another writer updates it or a consequential action needs a fresh guard.

Do not dump raw PDFs, HTML, full histories, entire repositories or repeated tool envelopes into the conversation. Extract the relevant passage. Convert unstructured source into clean Markdown only when that conversion is needed. Use clean pasted text as-is; do not rewrap, reformat or summarize it again unless requested.

Reason freshly from verified prior state. Do not repeat plans, specifications, completed explanations or source material. Keep implementation preambles minimal. Show changed files or relevant changed lines only; provide full material when the user requests it or a complete deliverable requires it.

Batch independent targeted reads. Preserve useful results rather than searching again. Limit diagnostics to the evidence needed to choose a repair. After two unchanged failures, diagnose and change the approach; repeating the same call is not progress.

## Actual model controls

Choose effort appropriate to uncertainty and impact:

| Work | Typical effort |
| --- | --- |
| Small documentation, formatting or isolated style edits | Low |
| Bounded features, API changes, ordinary debugging | Moderate |
| Security, architecture, electrical algorithms or numerical correctness | High |
| Unusually unresolved research or coupled high-impact decisions | Exceptional, justified |

These are planning judgments, not claims that a model or runtime changed. Select a different model or reasoning level only through a real exposed control that the user or runtime authorizes. If none exists, continue with available capability and describe any material limitation honestly.

Optimize total effort, including retries and review, rather than choosing a weak approach that repeatedly fails. Do not invent token quotas, savings percentages, time limits or usage measurements. Use measured provider data where available and label estimates as estimates.

## Environment and delegation

Cloud execution offers capability and availability differences; it does not inherently guarantee lower token use or a token discount. Choose the environment through [cloud execution](cloud-execution.md).

Use one implementer by default. Delegate a bounded, independently useful specialist task only when its benefit exceeds coordination and duplicated context. Follow [multi-agent collaboration](multi-agent-collaboration.md). Routine reporting uses only the [five-field STATUS format](../standards/continuation-and-reporting.md#routine-reporting).
