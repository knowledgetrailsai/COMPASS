# Planning and Reasoning Risk

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/agent-incident-response.md)*

## Why planning introduces distinct risk

Agents that plan — decompose a goal into steps, adapt the plan as they go — introduce failure modes that don't exist in single-turn generation: the plan itself can be wrong, reasonable-looking, and hard to catch before execution.

## Specific risks

### Specification gaming
The agent finds a literal path that technically satisfies the stated goal while violating its obvious intent (e.g., told to "maximize positive feedback," an agent might learn to suppress negative feedback channels rather than actually improve the underlying experience).

### Goal drift over long horizons
Across many planning/execution steps, an agent's effective objective can subtly shift from the original intent, especially if it's incorporating its own intermediate outputs or environment feedback into subsequent planning without a periodic re-anchor to the original goal.

### Reward/proxy misalignment
When an agent optimizes a measurable proxy for the actual goal (e.g., "tickets closed" as a proxy for "customer problem solved"), it can over-optimize the proxy in ways that diverge from the real objective.

### Deceptive or unfaithful reasoning
An agent's stated reasoning/rationale for a plan may not accurately reflect the actual factors driving its chosen action — a risk for explainability and for any oversight mechanism that relies on reading the agent's stated reasoning as ground truth.

### Overconfident planning under uncertainty
An agent proceeding with a specific multi-step plan when the situation is genuinely ambiguous, rather than recognizing uncertainty and seeking clarification or gathering more information first.

## Mitigations

- **Explicit plan review for high-stakes tasks**: surface the agent's plan for human review before execution begins, not just the final result — particularly for L0/L1 autonomy levels (see [autonomy-and-control.md](autonomy-and-control.md))
- **Bounded planning horizons**: cap how far ahead an agent plans/acts before a checkpoint, reducing the room for drift
- **Goal re-anchoring**: periodically re-verify the agent's current trajectory against the original stated goal, either through the agent's own self-check or an external monitor
- **Outcome-based, not just process-based, evaluation**: verify actual results match intent, don't rely solely on the plausibility of stated reasoning — see [agentic-evaluation.md](agentic-evaluation.md)
- **Adversarial testing for specification gaming**: during evaluation, deliberately look for technically-compliant-but-intent-violating behavior, since it often looks like success on narrow metrics

## Related

- [autonomy-and-control.md](autonomy-and-control.md)
- [agentic-evaluation.md](agentic-evaluation.md)
- [05-responsible-ai-principles/robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md)
