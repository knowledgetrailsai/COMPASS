# Fairness and Bias

*[Home](../INDEX.md) › [05 · Responsible AI Principles](../05-responsible-ai-principles/accountability-and-human-oversight.md)*

## What it means

Ensuring AI systems don't produce systematically unfair outcomes across individuals or groups, particularly on protected or sensitive attributes (race, gender, age, disability, religion, caste, etc., subject to local law).

## Sources of bias

- **Historical bias**: training data reflects past discriminatory patterns (e.g., hiring data reflecting past exclusion)
- **Representation bias**: underrepresentation of certain groups in training data
- **Measurement bias**: proxies used for the target variable correlate with protected attributes (e.g., zip code as a proxy for race)
- **Aggregation bias**: a single model applied uniformly when subgroups need different treatment
- **Evaluation bias**: benchmarks/test sets that don't reflect real-world subgroup distribution
- **Gen AI-specific**: stereotyped or unrepresentative content generation (e.g., image generators defaulting to one demographic for a profession)

## Fairness definitions (there is no single "fair")

Different, sometimes mutually incompatible, formal definitions exist:
- **Demographic parity**: outcome rates equal across groups
- **Equal opportunity**: true positive rates equal across groups
- **Equalized odds**: true and false positive rates equal across groups
- **Individual fairness**: similar individuals receive similar outcomes
- **Counterfactual fairness**: outcome unchanged if a protected attribute were different, all else equal

Choice of definition should be a deliberate, documented decision involving legal/compliance and domain experts — not a default left to the engineering team, since definitions can conflict.

## Mitigation approaches

| Stage | Techniques |
|---|---|
| Pre-processing | Reweighting, resampling, data augmentation for underrepresented groups |
| In-processing | Fairness constraints during training, adversarial debiasing |
| Post-processing | Threshold adjustment per group, calibration |

See [08-controls-and-techniques/fairness-testing](../08-controls-and-techniques/fairness-testing/README.md) for tooling.

## Gen AI considerations

Bias shows up in generated text/images/code (stereotyped roles, skewed representation), and in whose voice/dialect is treated as "default" vs. "other." Mitigate via diverse training/fine-tuning data, output filtering, and explicit prompt/system instructions promoting balanced representation, combined with evaluation against bias benchmarks.

## Agentic AI considerations

Bias can compound across multi-step autonomous decisions — a slightly biased scoring step feeding into an autonomous action amplifies rather than staying a static, reviewable output. Test fairness at the level of end-to-end outcomes, not just individual model components.

## Practical checklist

- Define the protected attributes relevant to your jurisdiction and use case
- Choose and document a fairness definition appropriate to the decision context
- Test on representative, sufficiently large subgroup samples (not just aggregate accuracy)
- Re-test after any data or model change, not just at launch
