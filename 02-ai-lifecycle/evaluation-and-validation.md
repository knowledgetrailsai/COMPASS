# Stage 5: Evaluation & Validation

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/lifecycle-overview.md)*

## Purpose

Independently verify the system meets its fairness, safety, robustness, and performance requirements before it's exposed to real users, the primary technical gate in the lifecycle.

## Activities

- **Fairness/bias testing** across relevant subgroups at realistic sample sizes: see [08-controls-and-techniques/fairness-testing](../08-controls-and-techniques/fairness-testing/README.md)
- **Robustness and adversarial testing**: edge cases, distribution shift, adversarial inputs: see [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md)
- **Explainability validation**: confirm explanations are accurate and usable by the intended audience, not just technically present
- **Gen AI**: hallucination rate, groundedness (RAG), jailbreak resistance, see [06-generative-ai/genai-evaluation.md](../06-generative-ai/genai-evaluation.md)
- **Agentic AI**: task success rate, permission compliance under adversarial conditions, recovery behavior — see [07-agentic-ai/agentic-evaluation.md](../07-agentic-ai/agentic-evaluation.md)
- **Red-teaming** for Tier 1 systems and any externally-exposed Gen AI/agentic system, see [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md)
- **Independence check**: for Tier 1 systems, evaluation should involve reviewers who weren't part of the build team, to avoid confirmation bias

## Validating against the original requirements

Evaluation should test against the specific, testable acceptance criteria set in [requirements-and-design.md](requirements-and-design.md) (not a generic checklist) so a pass/fail is unambiguous rather than a judgment call at launch time.

## Outputs

- Evaluation report against each requirement (pass/fail/conditional, with evidence)
- Red-team report with findings and remediation status
- Updated model/system card with actual (not just target) performance figures, including subgroup breakdowns

## Gate

Tier 1 systems require governance board sign-off on the evaluation report before deployment ([03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md)). Unresolved high-severity red-team findings should block launch regardless of tier.
