# Agentic Evaluation

## Why standard Gen AI evaluation isn't sufficient

Evaluating a single response for quality/safety doesn't capture whether a multi-step, tool-using agent reliably accomplishes tasks safely across a realistic range of scenarios, recovers from errors, and respects its permission boundaries.

## Evaluation dimensions

### Task success rate
Did the agent actually accomplish the intended goal, end-to-end, across a representative set of realistic tasks (not just easy demo cases)? Measure across varying task complexity and length.

### Safety and permission compliance
Did the agent stay within its scoped tool/action permissions across the full task, including under adversarial conditions (injected instructions, misleading tool outputs, edge-case inputs)? This should be tested adversarially, not just observed in normal operation.

### Recovery and error handling
When a tool call fails, returns unexpected data, or the environment doesn't match the agent's plan, does the agent notice and recover sensibly (retry, ask for help, halt) rather than proceeding on bad assumptions or looping unproductively?

### Efficiency
Number of steps/tool calls/tokens consumed to complete a task — relevant both for cost and as a signal of whether the agent is looping or taking unnecessarily risky/broad actions to accomplish something a narrower approach could achieve.

### Groundedness of decisions
For agents that reason before acting, does the stated rationale actually match and justify the action taken — useful both for explainability and as a debugging signal when the agent misbehaves.

### Human-in-the-loop friction
Does the agent escalate appropriately (neither too often, causing approval fatigue, nor too rarely, missing genuinely uncertain/high-stakes moments)?

## Evaluation methods

- **Scripted task suites**: predefined tasks with known correct outcomes, run regularly (regression testing) as the agent/model/prompts change
- **Adversarial/red-team scenarios**: deliberately inject misleading tool outputs, conflicting instructions, or prompt injection attempts to test resilience
- **Simulation environments**: sandboxed versions of real tools/environments that let agents be tested at scale without real-world side effects
- **Long-horizon task evaluation**: specifically test tasks requiring many steps, since failure rates often compound with task length (see [05-responsible-ai-principles/robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md))
- **Human evaluation of action logs**: periodic human review of a sample of real agent action logs in production, not just pre-launch testing

## Metrics to track in production

- Task success/failure rate by task type
- Human override/intervention rate (too low can indicate rubber-stamping; too high can indicate the agent isn't ready for its autonomy level)
- Escalation rate and appropriateness
- Incidents/near-misses per volume of agent actions

## Related

- [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/)
- [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md) — agent action logs
