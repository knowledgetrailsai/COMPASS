# Securing Agentic AI

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/)*

A consolidated security view over content already detailed in [07-agentic-ai](../07-agentic-ai/) — the highest-stakes security surface in this repository, since a compromised agent doesn't just say something wrong, it can *do* something wrong.

## Threat catalog

| Threat | Detail | Primary controls |
|---|---|---|
| Excessive agency | Agent granted broader permissions/autonomy than the task requires | Least privilege, autonomy-level matching to risk — [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md) |
| Insecure tool/plugin design | Tool interfaces that don't validate inputs or enforce scope independently of the model | Action allowlisting, schema validation before execution — [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md) |
| Identity/authorization compromise | Agent's credentials misused, or delegation scope abused | Scoped, time-boxed credentials, non-repudiation logging — [07-agentic-ai/identity-and-authorization.md](../07-agentic-ai/identity-and-authorization.md) |
| Prompt injection via tool outputs/environment | Malicious instructions in retrieved content or tool results hijack agent behavior | Untrusted-content handling, independent action validation — [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md) |
| Memory poisoning | False information deliberately fed for storage, influencing future behavior | Retention limits, explicit-over-implicit memory writes — [07-agentic-ai/memory-and-state-risk.md](../07-agentic-ai/memory-and-state-risk.md) |
| Multi-agent manipulation | Exploiting inter-agent trust/delegation for unintended cooperation or resource abuse | Bounded delegation, system-level circuit breakers — [07-agentic-ai/multi-agent-governance.md](../07-agentic-ai/multi-agent-governance.md) |
| Goal/specification gaming under adversarial pressure | Attacker steers the agent toward technically-compliant but harmful action | Outcome-based evaluation, human approval for high-stakes actions — [07-agentic-ai/planning-and-reasoning-risk.md](../07-agentic-ai/planning-and-reasoning-risk.md) |

## The containment principle

The documented real-world case in [12-case-studies/agentic-failures/aisi-unsanctioned-agent-behavior.md](../12-case-studies/agentic-failures/aisi-unsanctioned-agent-behavior.md) demonstrates the core lesson for this section: agent containment must be an independently enforced technical boundary (sandboxing, allowlisted actions validated outside the model), never an assumption based on the agent's intended scope or a testing context's presumed safety.

## Security review checklist for agentic systems

- [ ] Tool/action allowlist is default-deny, verified by testing an out-of-scope action attempt
- [ ] Credentials are scoped and time-boxed, distinct from any human operator's
- [ ] Action validation happens independent of the model's own "judgment"
- [ ] Kill switch tested under realistic production conditions, not just configuration review
- [ ] Prompt injection via tool outputs specifically red-teamed, not just direct-prompt jailbreaking
- [ ] Multi-agent systems (if applicable) have a system-level, not just per-agent, circuit breaker

## Testing and incident response

[security-testing-program.md](security-testing-program.md); [security-incident-response.md](security-incident-response.md) and its agentic-specific companion [07-agentic-ai/agent-incident-response.md](../07-agentic-ai/agent-incident-response.md).
