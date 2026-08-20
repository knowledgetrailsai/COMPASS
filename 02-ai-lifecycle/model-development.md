# Stage 4: Model Development

## Purpose

Build or select the model/system in a way that's proportionate to the risk tier and satisfies the requirements set in [requirements-and-design.md](requirements-and-design.md).

## Activities

- **Architecture/model selection**: choose complexity proportionate to need — favor interpretable models for high-stakes decisions where they meet the performance bar; for Gen AI, choose between prompt engineering, RAG, and fine-tuning based on risk, cost, and control requirements (fine-tuning gives more control but adds governance overhead — see [06-generative-ai/fine-tuning-governance.md](../06-generative-ai/fine-tuning-governance.md)).
- **Baseline and benchmark selection**: establish what "good enough" looks like before training/tuning, including fairness and safety benchmarks, not just accuracy.
- **Iterative fairness/safety checks during development**: don't defer all testing to a single evaluation gate — catch major issues early when they're cheap to fix.
- **Guardrail integration**: build in content/action filters, input validation, and (for agents) permission enforcement as part of the system, not as an afterthought bolted on before launch — see [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md).
- **Documentation as you go**: capture design decisions, known limitations, and rejected alternatives in real time — reconstructing this after the fact for a model card is unreliable.

## Agentic AI-specific

- Implement tool access exactly as scoped in requirements — least privilege from the first integration, not "broad access now, narrow later"
- Build in escalation/uncertainty handling as a first-class behavior, not an edge case handled by whatever the model does by default
- Design action validation (schema/allowlist checks before a tool call executes) as part of the architecture

## Outputs

- Working model/system meeting baseline requirements
- Draft model card / system card
- Guardrails implemented and unit-testable

## Gate

Move to evaluation only once the system meets its design-time requirements on internal testing — evaluation & validation ([evaluation-and-validation.md](evaluation-and-validation.md)) is the independent check, not a substitute for developer-level testing during this stage.
