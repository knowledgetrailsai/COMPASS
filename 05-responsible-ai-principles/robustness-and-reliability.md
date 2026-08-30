# Robustness and Reliability

*[Home](../INDEX.md) › [05 · Responsible AI Principles](../05-responsible-ai-principles/accountability-and-human-oversight.md)*

## What it means

The system performs consistently and predictably under normal conditions, edge cases, and distribution shift — and fails safely (visibly, gracefully) rather than silently producing confidently wrong output.

## Dimensions

- **Statistical robustness**: performance holds up across the real-world distribution of inputs, not just the test set
- **Adversarial robustness**: resistance to inputs deliberately crafted to cause failure (see [safety-and-security.md](safety-and-security.md))
- **Distribution shift resilience**: graceful degradation (or detection and fallback) when real-world data drifts from training data over time
- **Operational reliability**: uptime, latency, consistent behavior across infrastructure conditions — standard SRE concerns applied to AI-serving systems

## Gen AI-specific reliability concerns

- **Consistency**: same/similar input producing wildly different outputs across calls (relevant for deterministic-seeming use cases like classification-via-LLM)
- **Groundedness (RAG)**: output should be traceable to retrieved source material; ungrounded generation is a robustness failure, not just a hallucination framing issue
- **Degradation under long context / complex tasks**: performance often drops as task complexity or context length increases — test at realistic complexity, not just simple demo cases

## Agentic AI-specific reliability concerns

- **Error compounding**: small per-step error rates compound across long multi-step plans — a 95%-reliable-per-step agent doing 20 steps is far less than 95% reliable end-to-end
- **Recovery behavior**: does the agent notice when a step failed or a tool returned an error, and recover sensibly, or does it plow ahead on bad information?
- **Environment drift**: agents operating against live systems (APIs, file systems, web) need to handle the environment changing between planning and execution

## Testing approaches

See [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md): stress testing, chaos-engineering-style fault injection, adversarial test suites, long-horizon task evaluation for agents, and shadow-mode deployment to observe real-world performance before it affects users.

## Fail-safe design principles

- Prefer explicit failure/refusal over confident guessing when the system is out of its reliable operating range
- Define and test fallback behavior (e.g., hand off to a human, return "I don't know" with appropriate caveats, halt an agent rather than let it improvise on an unrecoverable error)
- Set and monitor SLOs for AI-specific reliability metrics (hallucination rate, task success rate, action error rate), not just infrastructure uptime
