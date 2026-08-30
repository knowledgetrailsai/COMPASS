# Controls and Techniques

*[Home](../INDEX.md) › [08 · Controls & Techniques](../08-controls-and-techniques/README.md)*

This section implements the **Risk → Control → Technique → Test** chain referenced in [00-navigation-and-methodology/knowledge-map.md](../00-navigation-and-methodology/knowledge-map.md).

**Risk**: a specific way a system could cause harm (defined in 01, 06, 07).
**Control**: a policy or architectural measure that reduces the risk.
**Technique**: a concrete method implementing a control.
**Test**: how you verify the control/technique actually works ([04-ai-assurance](../04-ai-assurance/assurance-overview.md)).

## Example

| Risk | Controls | Techniques | Test |
|---|---|---|---|
| Prompt injection | Input isolation, tool permission boundaries, trusted/untrusted content separation, human approval | Prompt sanitization, content classification, sandboxing, policy enforcement | Adversarial prompts, red-team scenarios, tool-abuse tests |

## Subsections

| Folder/file | Covers |
|---|---|
| [fairness-testing/](fairness-testing/README.md) | Bias metrics, mitigation techniques |
| [explainability/](explainability/README.md) | Feature attribution, counterfactuals, interpretability methods |
| [privacy-techniques/](privacy-techniques/README.md) | Differential privacy, federated learning, anonymization, PII handling |
| [robustness-testing/](robustness-testing/README.md) | Adversarial testing, stress testing |
| [evaluation-and-benchmarking/](evaluation-and-benchmarking/README.md) | Evaluation methodology and benchmark design |
| [monitoring-and-observability/](monitoring-and-observability/README.md) | Production monitoring techniques |
| [guardrails-and-controls.md](guardrails-and-controls.md) | Runtime content/action controls |

Each technique file links back to the risk(s) it mitigates and the tool(s) that implement it in [09-tools-and-frameworks](../09-tools-and-frameworks/commercial-platforms.md).
