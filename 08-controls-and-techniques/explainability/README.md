# Explainability Techniques

*[Home](../../INDEX.md) › [08 · Controls & Techniques](../../08-controls-and-techniques/README.md) › [explainability](../../08-controls-and-techniques/explainability/README.md)*

Implements [05-responsible-ai-principles/transparency-and-explainability.md](../../05-responsible-ai-principles/transparency-and-explainability.md) as concrete methods.

## Model-agnostic post-hoc methods

- **SHAP (SHapley Additive exPlanations)**: game-theoretic feature attribution, consistent and locally accurate, but computationally expensive for large feature sets/models
- **LIME (Local Interpretable Model-agnostic Explanations)**: approximates local model behavior with an interpretable surrogate model around a specific prediction
- **Permutation importance**: measures feature importance by observing performance change when a feature is shuffled
- **Partial dependence plots**: show marginal effect of a feature on predicted outcome

## Inherently interpretable models

For high-stakes decisions, consider whether a simpler, inherently interpretable model (decision trees, linear/logistic regression, generalized additive models) meets the performance bar. Avoiding the need for post-hoc explanation entirely is often preferable to explaining a black box, per [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md).

## Counterfactual explanations
"What would need to change for a different outcome" — often the most actionable explanation format for an affected individual (e.g., "if income were $X higher, this application would be approved"), and increasingly a regulatory expectation for automated decisions with legal/significant effect.

## Gen AI explainability techniques

- **Citation/attribution**: surfacing the specific retrieved source(s) an answer draws from (RAG)
- **Chain-of-thought / reasoning traces**: surfacing intermediate reasoning steps, useful for debugging, with the caveat (per [07-agentic-ai/planning-and-reasoning-risk.md](../../07-agentic-ai/planning-and-reasoning-risk.md)) that stated reasoning isn't guaranteed faithful to the actual generation process
- **Attention visualization**: for some architectures, visualizing which input tokens most influenced output: a research-stage rather than production-standard technique for most applications

## Choosing a technique

Match the technique to the audience: a data scientist debugging a model needs different explanation depth than an end user trying to understand why their loan was denied. Design explanations for the actual audience, not the easiest technique to implement.

## Tooling

See [09-tools-and-frameworks/open-source-tools.md](../../09-tools-and-frameworks/open-source-tools.md) (SHAP, LIME, InterpretML libraries).
