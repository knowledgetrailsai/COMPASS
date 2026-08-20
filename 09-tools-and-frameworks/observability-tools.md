# Observability Tools

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/)*

## LLM/Gen AI tracing and monitoring

| Tool/category | Purpose |
|---|---|
| TruLens | Tracing and evaluation feedback loops for LLM applications |
| LangSmith-style tracing platforms | Prompt/chain tracing, latency and cost monitoring, debugging |
| Custom logging pipelines (OpenTelemetry-based) | Structured logging of prompts, outputs, and metadata into existing observability stacks |

## Agentic observability

Purpose-built agent tracing tools are an emerging category — capturing full action/tool-call sequences, decision points, and outcomes per [07-agentic-ai/agent-observability.md](../07-agentic-ai/agent-observability.md). Where dedicated tooling is immature for your stack, a well-structured custom logging schema (action, parameters, result, timestamp, triggering context, permission check outcome) into your existing observability platform is a reliable fallback.

## Drift and quality monitoring

| Tool/category | Purpose |
|---|---|
| Standard ML monitoring platforms (Evidently, WhyLabs, Arize, and similar) | Data/concept drift detection, model performance monitoring |
| RAGAS (production sampling mode) | Ongoing groundedness/relevance sampling in production, not just pre-launch |

## Integration principle

AI observability should extend, not replace, standard application observability (APM, logging, alerting) — route AI-specific signals into the same dashboards and on-call systems your engineering org already uses, rather than building a parallel, siloed AI monitoring stack no one checks regularly.

## What "good" observability looks like

- Traceable from a production incident back to the specific prompt/model version/data snapshot involved
- Dashboards accessible to the accountable system owner, not buried in a data science notebook
- Alerting tied to the thresholds defined in [02-ai-lifecycle/deployment-and-release.md](../02-ai-lifecycle/deployment-and-release.md), routed to a named on-call owner

## Related

- [08-controls-and-techniques/monitoring-and-observability](../08-controls-and-techniques/monitoring-and-observability/)
- [07-agentic-ai/agent-observability.md](../07-agentic-ai/agent-observability.md)
