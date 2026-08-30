# Evaluation and Benchmarking

*[Home](../../INDEX.md) › [08 · Controls & Techniques](../../08-controls-and-techniques/README.md) › [evaluation-and-benchmarking](../../08-controls-and-techniques/evaluation-and-benchmarking/README.md)*

The general evaluation methodology referenced throughout this repository; see [06-generative-ai/genai-evaluation.md](../../06-generative-ai/genai-evaluation.md) and [07-agentic-ai/agentic-evaluation.md](../../07-agentic-ai/agentic-evaluation.md) for technology-specific depth.

## Evaluation design principles

- **Match the metric to the requirement**: evaluate against the specific, testable acceptance criteria set in [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md), not a generic off-the-shelf benchmark alone
- **Representative test data**: held-out test sets/scenarios that reflect real deployment conditions, including realistic subgroup distribution, not just clean/easy cases
- **Multiple evaluation methods**: combine automated metrics, model-based evaluation (LLM-as-judge), and human evaluation — each catches different failure types
- **Regression testing**: maintain a versioned evaluation suite that runs on every material change, so quality/safety regressions are caught before they reach production, not after

## Benchmark types

| Type | Use |
|---|---|
| Public general-purpose benchmarks | Baseline capability comparison across models (useful for model selection, insufficient alone for production readiness) |
| Domain-specific benchmarks | Closer to real use case, still may not reflect your exact data/users |
| Custom use-case benchmarks | Built from your own realistic scenarios — the most reliable signal for production readiness |
| Safety/bias benchmark suites | Standardized adversarial/bias probes — a floor, not a ceiling, for safety evaluation |

## Human evaluation design

- Clear, structured rubrics rather than open-ended "rate this 1-5" to improve inter-rater consistency
- Multiple raters per item where feasible, with disagreement analysis
- Rater diversity relevant to the use case (e.g., raters familiar with the domain for domain-specific quality judgments)

## Statistical rigor

Report evaluation results with sample sizes and, where meaningful, confidence intervals — a metric computed on too few examples can be noise, particularly for subgroup breakdowns. Flag when a subgroup sample is too small for reliable conclusions rather than reporting a number without that caveat.

## Tooling

See [09-tools-and-frameworks/evaluation-frameworks.md](../../09-tools-and-frameworks/evaluation-frameworks.md).
