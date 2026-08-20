# Evaluation Frameworks

_Last reviewed: 2026-08-19._

## General-purpose LLM benchmarks

| Framework | Focus |
|---|---|
| HELM (Holistic Evaluation of Language Models) | Broad multi-metric evaluation (accuracy, robustness, fairness, efficiency) across many scenarios |
| MMLU and similar academic benchmarks | Knowledge/capability benchmarking — useful for model selection, not a substitute for use-case evaluation |

## RAG and application-level evaluation

| Framework | Focus |
|---|---|
| RAGAS | Groundedness, context precision/recall, answer relevance for RAG pipelines |
| DeepEval | Configurable LLM application evaluation, integrates with test frameworks (pytest-style) |
| promptfoo | Prompt regression testing, red-teaming test cases, side-by-side model comparison |
| TruLens | Tracing and evaluation feedback functions for LLM apps |

## Safety and bias benchmark suites

Standardized adversarial/bias probe sets (varies by provider/research group) — useful as a baseline safety floor; supplement with use-case-specific adversarial testing per [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md), since generic benchmarks won't cover your specific deployment context.

## Agentic evaluation

Emerging category — frameworks for simulating multi-step agent tasks in sandboxed environments, measuring task success rate, tool-use correctness, and safety-boundary compliance. This space is less mature/standardized than Gen AI text evaluation; expect to build custom scripted task suites (per [07-agentic-ai/agentic-evaluation.md](../07-agentic-ai/agentic-evaluation.md)) alongside whatever framework tooling you adopt.

## Choosing a framework

- Use general benchmarks (HELM, MMLU-style) for **model selection** only
- Use RAG-specific frameworks (RAGAS) when grounding/citation quality is central to your use case
- Use application-level frameworks (DeepEval, promptfoo, TruLens) to build your **own regression suite** tied to your actual use case and requirements
- Build custom scripted evaluation for **agentic** systems, since off-the-shelf coverage is still maturing

## Related

- [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/)
- [06-generative-ai/genai-evaluation.md](../06-generative-ai/genai-evaluation.md)
