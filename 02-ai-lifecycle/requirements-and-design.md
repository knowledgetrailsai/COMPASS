# Stage 2: Requirements & Design

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/)*

## Purpose

Translate the risk tier and intended use into concrete, testable requirements — what "responsible" specifically means for this system — before development locks in architectural choices that are expensive to unwind later.

## Activities

- **Principle-to-requirement translation**: for each applicable principle ([05-responsible-ai-principles](../05-responsible-ai-principles/)), define what it requires concretely for this system (e.g., "fairness" becomes "parity of approval rate across gender within 5 percentage points, tested pre-launch and quarterly").
- **Explainability requirements**: decide the level of explainability needed given the decision's stakes and audience, and choose architecture accordingly — don't default to the most opaque model available if a simpler, more interpretable one meets the accuracy bar for a high-stakes decision.
- **Human oversight design**: decide the autonomy/oversight model upfront (see [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md) for agentic systems) — retrofitting approval gates after launch is harder than designing them in.
- **Data requirements**: what data is needed, what's the lawful basis, what representativeness is required — feeds into [data-and-data-governance.md](data-and-data-governance.md).
- **Tool/permission scoping** (Agentic AI): define the minimum tool access and action scope the agent needs, before any implementation grants broader access "to be safe."
- **Regulatory requirements mapping**: identify applicable law/regulation for this use case and jurisdiction ([10-regulations-and-standards](../10-regulations-and-standards/)) and translate into design constraints.

## Outputs

- A requirements document covering functional requirements plus RAI-specific acceptance criteria (fairness thresholds, explainability level, human oversight model, permission scope)
- Draft evaluation plan (what will be tested before launch — feeds [evaluation-and-validation.md](evaluation-and-validation.md))

## Common failure mode

Treating RAI requirements as implicit ("we'll be fair, obviously") rather than specific and testable. If a requirement can't be tested, it can't be verified at the evaluation stage — write requirements as acceptance criteria, not aspirations.
