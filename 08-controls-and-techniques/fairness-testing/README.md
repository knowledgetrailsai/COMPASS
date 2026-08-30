# Fairness Testing

*[Home](../../INDEX.md) › [08 · Controls & Techniques](../../08-controls-and-techniques/README.md) › [fairness-testing](../../08-controls-and-techniques/fairness-testing/README.md)*

Implements the fairness principle ([05-responsible-ai-principles/fairness-and-bias.md](../../05-responsible-ai-principles/fairness-and-bias.md)) as testable controls.

## Metrics

- **Demographic parity difference/ratio**: gap in positive outcome rate across groups
- **Equal opportunity difference**: gap in true positive rate across groups
- **Equalized odds**: gap in both true and false positive rates across groups
- **Disparate impact ratio**: ratio of selection rates between groups (four-fifths/80% rule is a common regulatory reference point in some contexts, not a universal legal standard)
- **Calibration**: whether predicted probabilities mean the same thing across groups

## Testing process

1. Identify relevant subgroups for the use case and jurisdiction (protected attributes vary by law and context)
2. Ensure sufficient subgroup sample size for statistically meaningful testing — flag when a subgroup is too small to test reliably rather than silently skipping it
3. Compute chosen metric(s) per the fairness definition selected in [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md)
4. Compare against the pre-defined acceptability threshold
5. For Gen AI: structured probe testing — vary only a demographic detail in otherwise-identical prompts and compare outputs for stereotyping or differential treatment

## Mitigation techniques

| Stage | Technique |
|---|---|
| Pre-processing | Reweighting, resampling, augmentation for underrepresented groups |
| In-processing | Fairness constraints/regularization during training, adversarial debiasing |
| Post-processing | Per-group threshold adjustment, calibration |
| Gen AI | Balanced fine-tuning/prompt data, output filtering for stereotyped content, instruction-based debiasing |

## Tooling

See [09-tools-and-frameworks/open-source-tools.md](../../09-tools-and-frameworks/open-source-tools.md) for specific libraries (Fairlearn, AIF360, Aequitas).

## Test cadence

Pre-launch, on every material data/model change, and on a recurring cadence in production (see [02-ai-lifecycle/monitoring-and-observability.md](../../02-ai-lifecycle/monitoring-and-observability.md)) since population and usage patterns shift over time.
