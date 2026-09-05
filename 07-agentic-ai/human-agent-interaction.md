# Human-Agent Interaction

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/agent-incident-response.md)*

## Why this deserves its own focus

Even a well-controlled agent creates risk if the humans overseeing or working alongside it don't have the right information, at the right time, in a usable form, to exercise meaningful oversight. Human-agent interaction design is a control in its own right, not just a UX nicety.

## Design considerations

### Clarity about agent status and capability
Users/operators should always know: is an agent currently acting autonomously, awaiting approval, or paused? What is it authorized to do? Ambiguity here leads to both over-trust (assuming oversight exists when it doesn't) and under-trust (unnecessary manual intervention that defeats the point of automation).

### Actionable approval requests
When an agent requests human approval (see [autonomy-and-control.md](autonomy-and-control.md)), the request should present enough context for a genuinely informed decision — not just "approve/deny" with no visibility into the agent's reasoning or the action's consequences. A reviewer who can't understand what they're approving will either rubber-stamp or block everything.

### Avoiding automation bias
Humans reviewing agent-proposed actions tend, over time, to trust the agent's judgment more than warranted and reduce genuine scrutiny (the same automation bias risk as in [06-generative-ai/genai-specific-risks.md](../06-generative-ai/genai-risk-landscape.md), amplified because agent proposals often look procedurally thorough). Counter with periodic deliberate scrutiny audits, rotating reviewers, and tracking override rates as a governance signal.

### Escalation UX
When an agent escalates due to uncertainty, the escalation should clearly convey what's uncertain and why. A generic "I need help" without context pushes the cognitive burden of diagnosis back onto the human, undermining the value of delegation.

### Interruptibility
Users/operators should be able to interrupt or redirect an in-progress agent task easily and have confidence the interruption actually takes effect; see the kill-switch requirement in [autonomy-and-control.md](autonomy-and-control.md).

### Feedback loops
Give users/operators an easy way to flag agent errors or undesired behavior, and ensure that feedback actually reaches the team that can act on it (evaluation, retraining, guardrail tuning) — not just logged and unread.

## Trust calibration as a design goal

The goal is *calibrated* trust; users should trust the agent roughly in proportion to how reliable it actually is for a given task type, neither more nor less. Overly confident agent framing/UX can create miscalibrated trust even when the underlying reliability is fine; design and measure for calibration, not just for user satisfaction with the interaction.

## Related

- [autonomy-and-control.md](autonomy-and-control.md)
- [05-responsible-ai-principles/accountability-and-human-oversight.md](../05-responsible-ai-principles/accountability-and-human-oversight.md)
