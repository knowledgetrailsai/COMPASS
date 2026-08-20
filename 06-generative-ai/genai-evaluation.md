# Generative AI Evaluation

## Why standard ML evaluation isn't sufficient

Generative outputs don't have a single "correct answer" the way a classification label does — evaluation needs methods suited to open-ended, often subjective output quality, alongside the specific Gen AI risk categories (hallucination, safety, groundedness).

## Evaluation dimensions

- **Quality/helpfulness**: does the output actually address the request well? Often requires human or model-based (LLM-as-judge) evaluation, not just automated metrics
- **Groundedness/faithfulness** (RAG): does the output follow from cited sources? See [hallucination-and-grounding.md](hallucination-and-grounding.md)
- **Safety**: rate of generating disallowed content categories under both normal and adversarial (jailbreak) conditions
- **Fairness**: representation and stereotyping patterns across demographic references in generated content — test with structured probes (e.g., varying only a demographic detail in otherwise-identical prompts and comparing outputs)
- **Consistency**: variance in output across repeated identical or near-identical queries
- **Robustness**: quality degradation under realistic input variation (typos, informal phrasing, non-native speaker patterns, long context)

## Evaluation methods

- **Golden test sets**: curated prompts with known-good reference answers or rubrics, run as regression tests on every material change
- **LLM-as-judge**: using a separate (often stronger or differently-tuned) model to score outputs against a rubric — useful for scale, but validate periodically against human judgment since judge models have their own biases and blind spots
- **Human evaluation**: essential for nuanced quality/safety judgment, especially for high-stakes or novel use cases; use structured rubrics and multiple raters for consistency
- **A/B and production sampling**: real-world output sampling and user feedback signals as an ongoing complement to pre-launch evaluation

## Benchmark suites

Public benchmarks (e.g., safety/bias benchmark suites, domain-specific QA sets) offer a useful baseline but rarely reflect your specific use case closely enough to substitute for use-case-specific evaluation — treat them as a floor, not a substitute for [02-ai-lifecycle/evaluation-and-validation.md](../02-ai-lifecycle/evaluation-and-validation.md). See [09-tools-and-frameworks/evaluation-frameworks.md](../09-tools-and-frameworks/evaluation-frameworks.md) for specific tools (RAGAS, DeepEval, promptfoo, HELM).

## Continuous evaluation

Because prompts and underlying models change frequently, build evaluation into CI — automated regression suites that run on every prompt/model/RAG-corpus change, not just at initial launch. See [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/).
