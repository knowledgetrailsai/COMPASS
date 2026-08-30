# Stage 1: Opportunity & Use Case

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/lifecycle-overview.md)*

## Purpose

Before any building starts: define what problem the AI system solves, for whom, and how risky that is — the cheapest point in the lifecycle to catch a use case that shouldn't proceed, or that needs a fundamentally different design.

## Activities

- **Problem framing**: what decision or task is being augmented or automated, and why AI (vs. a simpler rules-based or human process)?
- **Intended use and out-of-scope use**: explicitly document what the system is for, and — equally important — what it is not approved for. Most AI incidents happen when a system is used outside its validated scope.
- **Affected stakeholders**: identify not just direct users but people impacted by the system's outputs/actions (e.g., loan applicants affected by a credit model they never directly interact with).
- **Initial risk tiering**: apply [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) to get a preliminary tier — this determines how much rigor the rest of the lifecycle requires.
- **Ethics screen**: for Tier 1 or ethically ambiguous use cases, route through an ethics review — see [01-foundations/ai-ethics.md](../01-foundations/ai-ethics.md).
- **Build vs. buy vs. prompt-only decision** (Gen AI): fine-tuning a model, using RAG over a base model, or prompt engineering alone carry different risk and governance profiles — decide deliberately, not by default to whatever's fastest.
- **Autonomy scoping** (Agentic AI): what level of autonomy does the task actually require? Default to the minimum — see [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md).

## Outputs

- A one-page use case brief: problem, intended users, intended/out-of-scope use, preliminary risk tier, accountable owner
- Entry in the AI inventory ([03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md))

## Gate

Tier 0 (prohibited) use cases stop here. Tier 1 use cases require governance board awareness before development investment proceeds. Tier 2–3 can proceed with standard checklist self-certification.
