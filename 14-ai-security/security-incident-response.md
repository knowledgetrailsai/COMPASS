# AI Security Incident Response

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

## Relationship to other incident response content

This file is the security-specific lens on the processes detailed in [02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md) (general AI incidents) and [07-agentic-ai/agent-incident-response.md](../07-agentic-ai/agent-incident-response.md) (agentic-specific containment). Use those for full process detail; this file focuses on what's distinct about a *security* incident specifically (as opposed to a quality, fairness, or reliability incident).

## What distinguishes a security incident

Evidence of adversarial intent or exploitation — a successful or attempted prompt injection, jailbreak, model extraction attempt, data exfiltration, or unauthorized action traced to a compromised credential or manipulated input, as opposed to an accidental quality failure with no adversary involved.

## Security-specific triage additions

- **Attribute the vector**: which threat category from [ai-threat-model.md](ai-threat-model.md) does this match? This determines the applicable containment playbook.
- **Assess scope beyond the immediate incident**: if this exploited a systemic weakness (e.g., a guardrail bypass technique), assume it may have been used elsewhere/before; check logs across all systems sharing the vulnerable configuration, not just the one where it was caught.
- **Preserve forensic evidence before remediation**: security incidents often need evidence (attack payloads, exact input sequences) preserved for investigation and potential legal/regulatory response, not just enough to root-cause a bug fix.
- **Determine credential/access compromise**: if the incident involved a compromised credential (an agent's API key, a service account), rotate it immediately — this is a security-team-led action, not just an AI-system-owner action.

## Integration with existing security incident response

Route AI security incidents through the organization's existing security incident response process and severity classification (SEV levels, on-call, forensics), with AI-specific expertise looped in; don't build a parallel, disconnected AI-only incident process. The AI-specific additions above should slot into existing playbook templates as an appendix/checklist, not replace them.

## Regulatory/disclosure considerations

Security incidents involving personal data trigger breach notification obligations under applicable law ([10-regulations-and-standards](../10-regulations-and-standards/global-overview.md)), loop in legal/privacy immediately for any incident involving data exfiltration or unauthorized access to personal data, on the same timeline as any other security breach.

## Post-incident

Feed the specific attack technique into [security-testing-program.md](security-testing-program.md) as a new regression test case, and consider whether the vulnerability class (not just the specific instance) exists in other systems.

## Related

- [02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md)
- [07-agentic-ai/agent-incident-response.md](../07-agentic-ai/agent-incident-response.md)
