# Securing Traditional ML

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

## Threat catalog

### Adversarial examples
Inputs deliberately perturbed (often imperceptibly to humans) to cause misclassification. **Controls**: adversarial training, input preprocessing/sanitization, ensemble methods, robustness testing: see [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md).

### Data poisoning
Corrupting training data to embed bias, backdoors, or degraded performance triggered by specific inputs. **Controls**: data provenance verification ([02-ai-lifecycle/data-and-data-governance.md](../02-ai-lifecycle/data-and-data-governance.md)), anomaly detection on training data, trusted data pipeline access controls.

### Model extraction / model theft
Reconstructing a proprietary model's parameters or decision logic through systematic API querying. **Controls**: query rate limiting, output rounding/perturbation, watermarking model outputs, monitoring for query patterns consistent with extraction attempts.

### Membership inference
Determining whether a specific record was part of the training set, a privacy attack rather than a pure security one. **Controls**: differential privacy during training ([08-controls-and-techniques/privacy-techniques](../08-controls-and-techniques/privacy-techniques/README.md)), regularization, limiting confidence-score granularity in API responses.

### Model inversion
Reconstructing representative training examples (e.g., recognizable faces from a facial recognition model) from model outputs. **Controls**: same as membership inference — differential privacy, output granularity limits.

### Backdoor attacks
A model trained (via poisoning or malicious fine-tuning) to behave normally except when a specific trigger pattern is present. **Controls**: training data provenance, anomaly detection for trigger patterns, independent model validation ([04-ai-assurance/model-validation.md](../04-ai-assurance/model-validation.md)).

## Control summary table

| Threat | Primary control | Test method |
|---|---|---|
| Adversarial examples | Adversarial training, input sanitization | Adversarial robustness testing |
| Data poisoning | Data provenance, pipeline access control | Anomaly detection audits |
| Model extraction | Rate limiting, output perturbation | Query-pattern monitoring |
| Membership inference | Differential privacy | Privacy red-teaming |
| Model inversion | Differential privacy, output limits | Privacy red-teaming |
| Backdoor | Data provenance, independent validation | Trigger-pattern scanning |

## Testing

See [security-testing-program.md](security-testing-program.md) and [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md): tools like the Adversarial Robustness Toolbox (ART) and Foolbox ([09-tools-and-frameworks/open-source-tools.md](../09-tools-and-frameworks/open-source-tools.md)) implement much of this testing directly.

## Related

- [ai-threat-model.md](ai-threat-model.md)
- [09-tools-and-frameworks/MITRE-ATLAS.md](../09-tools-and-frameworks/MITRE-ATLAS.md)
