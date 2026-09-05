# Model Validation

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

## Purpose

Technical verification that a model/system actually performs as claimed, the assurance-layer counterpart to the lifecycle's [evaluation-and-validation.md](../02-ai-lifecycle/evaluation-and-validation.md) stage, with more emphasis on independence and rigor for higher-risk systems.

## Core validation activities

- **Performance validation**: does the model meet its accuracy/quality targets on a held-out, representative test set: not the training or development set?
- **Subgroup performance validation**: performance broken out by relevant subgroups, not just aggregate — a model with strong aggregate accuracy can still fail specific subgroups badly (see [05-responsible-ai-principles/fairness-and-bias.md](../05-responsible-ai-principles/fairness-and-bias.md))
- **Stability validation**: does performance hold up across reasonable input variation, or is it brittle to minor changes?
- **Assumption validation**: were the assumptions made in [02-ai-lifecycle/requirements-and-design.md](../02-ai-lifecycle/requirements-and-design.md) (about data distribution, user behavior, deployment context) actually true, checked against real evidence rather than left as unverified assumptions?

## Independence principle

Model validation should be performed, or at minimum independently reviewed, by someone other than the model's developer: see [independent-assessment.md](independent-assessment.md). Self-validation alone is appropriate only for Tier 3 systems.

## Gen AI validation specifics

- Groundedness/faithfulness validation for RAG systems
- Consistency validation across repeated/similar queries
- Validation against known hallucination-prone query categories relevant to the use case

## Agentic AI validation specifics

- End-to-end task success validation, not just component-level (e.g., validate the full multi-step workflow, not just that each tool call individually "worked")
- Validation under adversarial/edge-case conditions, not just the happy path
- Permission-boundary compliance validation, explicitly attempt to induce out-of-scope actions and confirm the system refuses/escalates

## Documentation

Validation results feed the model/system card and the risk register — see [evidence-and-traceability.md](evidence-and-traceability.md). Validation that isn't documented can't support a governance approval decision or survive an audit.

## Re-validation triggers

Material model, data, prompt, or tool-access changes; significant usage pattern shifts observed in monitoring; a defined periodic cadence for Tier 1 systems regardless of triggering events.
