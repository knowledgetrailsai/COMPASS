# AI Lifecycle Overview

Responsible AI is a lifecycle discipline, not a single gate. This section maps RAI checkpoints onto each stage of building and operating an AI system — including Generative AI and Agentic AI, which iterate faster than traditional ML but still pass through the same conceptual stages.

## The stages

| Stage | File | Core question |
|---|---|---|
| 1. Opportunity & use case | [opportunity-and-use-case.md](opportunity-and-use-case.md) | Should we build this, and how risky is it? |
| 2. Requirements & design | [requirements-and-design.md](requirements-and-design.md) | What does "responsible" mean for this specific system? |
| 3. Data & data governance | [data-and-data-governance.md](data-and-data-governance.md) | Is our data lawful, representative, and well-governed? |
| 4. Model development | [model-development.md](model-development.md) | Are we building/selecting the right model responsibly? |
| 5. Evaluation & validation | [evaluation-and-validation.md](evaluation-and-validation.md) | Does it actually work, fairly and safely? |
| 6. Deployment & release | [deployment-and-release.md](deployment-and-release.md) | Are guardrails live before real users are exposed? |
| 7. Monitoring & observability | [monitoring-and-observability.md](monitoring-and-observability.md) | Is it still behaving as expected in production? |
| 8. Incident & remediation | [incident-and-remediation.md](incident-and-remediation.md) | What happens when it doesn't? |
| 9. Retirement & decommissioning | [retirement-and-decommissioning.md](retirement-and-decommissioning.md) | How do we responsibly shut it down? |

## How this connects to governance and assurance

The lifecycle defines **when** checkpoints happen. [03-ai-governance](../03-ai-governance/) defines **who** owns each checkpoint and what process governs approval. [04-ai-assurance](../04-ai-assurance/) defines **how** you prove each checkpoint was done properly. Don't conflate the three — a project can nail the lifecycle steps but still fail governance (no one had authority to approve it) or assurance (no evidence trail exists).

## Change management as a lifecycle re-entry point

For Gen AI and Agentic AI especially, material changes — a new base model, a prompt rewrite, a new tool/data source, expanded autonomy — should re-enter this lifecycle at the appropriate stage (usually evaluation & validation at minimum) rather than being treated as a minor patch. Define "material change" explicitly for your systems so this isn't a judgment call made under launch-day pressure.

## Fast-iteration systems

Gen AI and agentic systems often change (prompts, tools, retrieval sources) far more often than a traditional model retrains. Build lightweight, automated versions of stages 5–6 (regression eval suites, guardrail tests in CI) so governance doesn't get silently bypassed by velocity — see [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/).
