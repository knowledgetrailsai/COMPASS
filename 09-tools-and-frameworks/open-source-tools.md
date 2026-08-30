# Open-Source Tools

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/commercial-platforms.md)*

_Last reviewed: 2026-08-19 — tool landscape moves quickly; verify current status/maintenance before adoption._

## Fairness and bias

| Tool | Purpose |
|---|---|
| Fairlearn | Fairness metrics and mitigation algorithms (Microsoft) |
| AIF360 (AI Fairness 360) | Broad fairness metrics/mitigation toolkit (IBM) |
| Aequitas | Bias audit toolkit with a policy-oriented reporting focus |

## Explainability

| Tool | Purpose |
|---|---|
| SHAP | Shapley-value-based feature attribution |
| LIME | Local surrogate-model explanations |
| InterpretML | Glassbox models plus explainability methods (Microsoft) |
| Captum | Model interpretability for PyTorch |

## Privacy

| Tool | Purpose |
|---|---|
| Microsoft Presidio | PII detection and redaction/anonymization |
| Opacus | Differential privacy for PyTorch training (DP-SGD) |
| TensorFlow Privacy | Differential privacy for TensorFlow training |
| Flower / FedML | Federated learning frameworks |

## Robustness and adversarial testing

| Tool | Purpose |
|---|---|
| Adversarial Robustness Toolbox (ART) | Adversarial attack/defense library (IBM) |
| Foolbox | Adversarial example generation |
| Garak | LLM vulnerability/red-teaming scanner |

## Guardrails and safety

| Tool | Purpose |
|---|---|
| NVIDIA NeMo Guardrails | Programmable guardrails for LLM applications |
| Guardrails AI | Output validation and structured guardrails framework |
| Llama Guard (and similar safety classifiers) | Input/output safety classification models |

## Gen AI / RAG evaluation

| Tool | Purpose |
|---|---|
| RAGAS | RAG-specific evaluation (groundedness, relevance, context precision/recall) |
| DeepEval | LLM application evaluation framework |
| promptfoo | Prompt testing, regression, and red-teaming CLI/framework |
| TruLens | LLM app evaluation and tracing |

## Selecting among these

See [tool-selection-matrix.md](tool-selection-matrix.md) for a decision guide by risk/lifecycle stage. Prefer tools with active maintenance and a track record for anything supporting a Tier 1 system's assurance evidence — an unmaintained tool undermines the credibility of the evidence it produces.
