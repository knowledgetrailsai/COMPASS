# Sustainability

*[Home](../INDEX.md) › [05 · Responsible AI Principles](../05-responsible-ai-principles/accountability-and-human-oversight.md)*

## Why it's part of Responsible AI

Training and operating large models — especially large generative models — consumes significant energy, water (for data center cooling), and hardware resources. As AI adoption scales, the aggregate environmental footprint becomes a material consideration alongside the more immediate risks covered elsewhere in this guide.

## Where the footprint comes from

- **Training**: a one-time (per model version) but often very large energy cost, concentrated at large model providers
- **Fine-tuning**: smaller but recurring cost as organizations customize base models
- **Inference**: the ongoing, cumulative cost of serving every query — at scale, inference can exceed training energy cost over a model's lifetime
- **Hardware lifecycle**: manufacturing and disposal of specialized AI hardware (GPUs/TPUs)
- **Agentic AI amplification**: agentic workflows often make many more model calls per user task (planning, tool calls, self-correction loops) than a single Gen AI response — inference cost per task can be significantly higher

## Practical levers for organizations building on AI (not training frontier models)

- **Model right-sizing**: use the smallest/most efficient model that meets the task's quality bar rather than defaulting to the largest available model for every call
- **Caching and reuse**: cache repeated queries/embeddings; avoid redundant re-computation, especially in agentic loops
- **Efficient prompting**: shorter, well-structured prompts and context reduce token processing without sacrificing quality
- **Batching and off-peak scheduling**: where latency allows, batch inference and schedule non-urgent workloads to align with lower-carbon-intensity grid periods
- **Vendor selection**: consider a cloud/model provider's disclosed energy efficiency and renewable energy commitments as a selection criterion, alongside cost and capability
- **Right level of agentic autonomy**: avoid open-ended agent loops (excessive self-correction/retry cycles) that multiply inference cost without proportionate value — bound iteration counts

## Reporting

Where material, include AI-related energy/compute considerations in existing corporate sustainability/ESG reporting, particularly for organizations deploying AI at significant scale. Some regulatory frameworks (EU AI Act, for general-purpose AI models) include energy consumption disclosure requirements — see [10-regulations-and-standards/eu-ai-act.md](../10-regulations-and-standards/EU/eu-ai-act.md).

## Balancing act

Sustainability should inform architecture and vendor choices, not be used to justify skipping safety/evaluation steps ("we didn't have compute budget to red-team this") — treat it as one more design constraint alongside, not traded off against, the other principles.
