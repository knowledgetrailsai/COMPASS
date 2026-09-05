# Safety and Security

*[Home](../INDEX.md) › [05 · Responsible AI Principles](../05-responsible-ai-principles/accountability-and-human-oversight.md)*

## Safety vs. security

- **Safety**: the system doesn't cause harm even when used as intended (or through foreseeable misuse) — unsafe outputs, unsafe autonomous actions, physical harm from embodied/robotic AI.
- **Security**: the system resists adversarial attack from parties trying to make it misbehave, extract data, or bypass controls.

> For the full practitioner-level security view (threat model, control catalog, testing program, incident response), see [14-ai-security](../14-ai-security/README.md): this page states the principle; that section operationalizes it.

## AI-specific security threats

| Threat | Description | Most relevant to |
|---|---|---|
| Prompt injection | Malicious instructions embedded in input (or retrieved content) hijack the model's behavior | Gen AI, Agentic AI (especially via tool outputs/web content) |
| Jailbreaking | Adversarial prompting to bypass safety training/guardrails | Gen AI |
| Data poisoning | Corrupting training data to embed backdoors or bias | Traditional ML, fine-tuned Gen AI |
| Model extraction | Reconstructing a proprietary model via API queries | All |
| Membership inference | Determining if specific data was in the training set | All, privacy-adjacent |
| Adversarial examples | Inputs crafted to fool a model (small perturbations) | Traditional ML (vision especially) |
| Tool/action abuse | Exploiting an agent's tool access to perform unauthorized actions | Agentic AI |
| Excessive agency | Agent granted more permission/autonomy than the task requires | Agentic AI |

## Safety practices

- Content/output filtering for harmful categories (violence, self-harm, CSAM, illegal activity), layered, not solely relying on base model training
- Rate limiting and abuse detection for public-facing systems
- Staged rollout (shadow mode → limited beta → GA) to catch unsafe behavior before broad exposure
- Human oversight/approval gates for high-consequence actions (see [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md))

## Security practices

- Treat prompt injection as an assumed threat for any system that processes untrusted input (user text, retrieved documents, web content, tool outputs) — don't rely on the model to "just not follow" injected instructions
- Least-privilege tool/API access for agents; no standing credentials broader than the task needs ([07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md))
- Sandboxing for code execution or file system access by agents
- Red-teaming / adversarial testing before launch and on a recurring cadence, see [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md)
- Input/output validation at every trust boundary, especially where agent output triggers a real-world action (e.g., don't let free-text model output become a raw shell command or SQL query without validation)

## Integration with existing security programs

AI security should extend, not replace, existing InfoSec practices: threat modeling, penetration testing, and incident response should treat AI components as part of the attack surface, with AI-specific playbooks layered on top (e.g., OWASP Top 10 for LLM Applications as a reference threat list).

## Related

- [14-ai-security/ai-threat-model.md](../14-ai-security/ai-threat-model.md): full attack-surface map
- [14-ai-security/security-testing-program.md](../14-ai-security/security-testing-program.md)
- [14-ai-security/security-incident-response.md](../14-ai-security/security-incident-response.md)
