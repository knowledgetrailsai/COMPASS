# Agentic AI — Risk Landscape

## What makes agentic AI different

Agentic AI systems plan, use tools, take multi-step actions, and often operate with some degree of autonomy toward a goal — as opposed to producing a single response to a single prompt. This shifts the risk profile from "the output might be wrong" to "the system might *do* something wrong," often with real-world, sometimes irreversible, consequences.

## Distinct risk categories

### Autonomy and goal misalignment
The agent pursues a stated goal in a literal or unintended way that technically satisfies the instruction but violates its intent ("specification gaming"), or continues pursuing a goal past the point a human would have stopped it. See [autonomy-and-control.md](autonomy-and-control.md).

### Tool-use and action risk
Agents with access to tools (APIs, code execution, file systems, email, payment systems) can take unauthorized, excessive, or harmful actions — either through model error, prompt injection, or under-scoped permissions. See [tool-use-and-permissions.md](tool-use-and-permissions.md).

### Cascading and compounding failures
Errors in early planning/reasoning steps propagate and amplify through subsequent steps; a single bad tool call or misread result can send a long-running agent far off course before a human notices. See [robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md).

### Multi-agent emergent behavior
Systems of multiple interacting agents (negotiating, delegating, competing for resources) can produce emergent behaviors not present in any single agent, including unintended collusion, resource contention, or conflicting sub-goals. See [multi-agent-governance.md](multi-agent-governance.md).

### Memory and state accumulation risk
Agents with persistent memory can accumulate incorrect beliefs, stale information, or sensitive data over time without clear correction or deletion mechanisms. See [memory-and-state-risk.md](memory-and-state-risk.md).

### Prompt injection via the environment
Because agents consume tool outputs, web content, and other external data as part of their operating loop, injected instructions in that content are a direct path to hijacking agent behavior — a higher-stakes version of the Gen AI prompt injection risk, since the payoff for an attacker is an action, not just bad text.

### Reduced human oversight at scale
As organizations deploy more agents doing more autonomous work, the practical ability of humans to review every action degrades — oversight has to shift from per-action review to sampling, anomaly detection, and well-designed approval gates for the highest-stakes actions.

## Why standard Gen AI controls aren't sufficient

Content filtering and hallucination mitigation address what an agent *says*; agentic risk requires controlling what it *does* — permissioning, action validation, approval gates, and monitoring of the action stream, not just the text stream.

## Risk-proportionate autonomy

Treat autonomy level as a dial, not a binary — see [autonomy-and-control.md](autonomy-and-control.md) for a structured way to decide how much independence an agent should have for a given task and risk tier.
