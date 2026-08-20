# RAG-Specific Considerations

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/)*

Retrieval-Augmented Generation (RAG) grounds model outputs in retrieved documents, and is the most common enterprise Gen AI pattern — it introduces its own responsible-AI considerations distinct from a standalone LLM.

## Access control at retrieval time

The single most common RAG security failure: indexing documents with mixed sensitivity/permission levels into one vector store without enforcing the original document-level access controls at query time. A user can end up seeing content from documents they were never authorized to access, because retrieval doesn't know or check permissions.
**Fix**: enforce access control as a hard filter in the retrieval step (metadata filtering tied to the querying user's actual permissions), not as an instruction to the model ("only use documents the user can see" is not a security boundary).

## Groundedness and citation

- Require/encourage outputs to cite the specific retrieved source(s) they draw from
- Evaluate **groundedness**: does the generated claim actually follow from the retrieved content, or did the model add ungrounded information?
- Surface citations to users so they can verify — this is both a trust and an explainability practice (see [05-responsible-ai-principles/transparency-and-explainability.md](../05-responsible-ai-principles/transparency-and-explainability.md))

## Data freshness and correctness

Retrieved content can be stale, contradictory across sources, or simply wrong (garbage in, confidently-stated garbage out). Maintain data pipeline hygiene: source freshness monitoring, deduplication, and conflict handling for contradictory documents.

## Prompt injection via retrieved content

Documents in the retrieval corpus can contain injected instructions (deliberately, if the corpus includes external/untrusted content like web pages or user-submitted documents) that hijack model behavior. Treat retrieved content as untrusted input, same as any other external content — see [prompt-and-output-safety.md](prompt-and-output-safety.md).

## Evaluation

Standard Gen AI evals aren't sufficient — RAG systems need retrieval-quality metrics alongside generation-quality metrics:
- Retrieval precision/recall (did we retrieve the right documents?)
- Groundedness/faithfulness (does the answer match the retrieved content?)
- Answer relevance (does the answer address the question?)

See [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/) and tools like RAGAS ([09-tools-and-frameworks/evaluation-frameworks.md](../09-tools-and-frameworks/evaluation-frameworks.md)).

## Data governance for the corpus

Apply the same data lifecycle discipline to the retrieval corpus as to any data asset: ownership, classification, retention, and a clear process for removing documents (including handling deletion requests that must actually remove content from the index, not just the source system).
