# Hallucination and Grounding

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/)*

## Definition

Hallucination: generative output that is plausible-sounding but false, fabricated, or unsupported by any legitimate source — presented with the same fluent confidence as accurate output, giving users no inherent signal to distinguish the two.

## Why it happens

Generative models predict statistically likely continuations, not verified facts — they have no built-in mechanism to distinguish "this is something I know to be true" from "this is a plausible-sounding continuation." Common triggers: questions at the edge or outside training data coverage, requests for specific structured facts (citations, statistics, names, dates), long-context tasks where earlier facts get inconsistently carried forward, and adversarial or leading prompts.

## Grounding as the primary mitigation

**Grounding** means constraining/connecting generation to verifiable source material rather than relying on parametric (trained-in) knowledge alone.

- **Retrieval-Augmented Generation (RAG)**: ground responses in retrieved documents, with citation back to source — see [RAG-governance.md](RAG-governance.md)
- **Tool-based verification**: have the model call a calculator, database, or search tool for factual claims rather than generating them from memory
- **Structured output constraints**: for tasks with a known-correct answer format, constrain output to only what's verifiable

## Detection and measurement

- **Groundedness/faithfulness scoring**: does the claim follow from the cited source? (See [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/) and tools like RAGAS in [09-tools-and-frameworks](../09-tools-and-frameworks/).)
- **Consistency checking**: sample the same query multiple times; high variance in factual claims is a hallucination signal
- **Domain-specific fact-checking**: for high-stakes domains (legal, medical, financial), automated or human verification against authoritative sources before output reaches the end user

## Mitigations beyond grounding

- Confidence calibration and appropriate hedging language, rather than uniform confident tone regardless of certainty
- Explicit "I don't know" / refusal behavior when the model lacks reliable grounding, trained/prompted as a first-class acceptable response rather than treated as failure
- Human review gates for high-stakes outputs (legal, medical, financial advice) regardless of grounding quality
- User education: clear disclosure that outputs can be wrong and should be verified for consequential decisions

## Risk is not uniform

Hallucination risk should be assessed per use case, not treated as a single global metric — a creative writing assistant's hallucination tolerance is entirely different from a legal research tool's. Set the acceptance bar during [02-ai-lifecycle/requirements-and-design.md](../02-ai-lifecycle/requirements-and-design.md), not as an afterthought.
