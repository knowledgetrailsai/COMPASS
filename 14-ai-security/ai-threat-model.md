# AI Threat Model

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/)*

## Purpose

A single, structured map of the AI-specific attack surface — organized by attack lifecycle stage (following the pattern of MITRE ATLAS and OWASP) and by system type, so a security review can systematically check what applies rather than working from an ad hoc list.

## Attack lifecycle stages

| Stage | Adversary goal | Applies most to |
|---|---|---|
| **Reconnaissance** | Learn about the model, training data, or system architecture | All |
| **Resource development** | Acquire tools, poisoned data, or access needed for the attack | All |
| **Initial access** | Get adversarial input into the system (direct prompt, poisoned document, malicious tool response) | Gen AI, Agentic AI |
| **ML/model attack staging** | Craft adversarial examples, jailbreak prompts, or poisoned training data | Traditional ML, Gen AI |
| **Execution** | Trigger the desired misbehavior (misclassification, harmful generation, unauthorized action) | All |
| **Persistence** | Establish a lasting foothold (poisoned memory, backdoored model, compromised credentials) | Agentic AI (memory), fine-tuned Gen AI |
| **Privilege escalation** | Get the system to exceed its intended permission/action scope | Agentic AI |
| **Exfiltration** | Extract training data, system prompts, proprietary model details, or sensitive retrieved content | Gen AI, Agentic AI |
| **Impact** | Achieve the ultimate harm — fraud, data breach, unauthorized action, service disruption, reputational damage | All |

## By system type

- **Traditional ML** → [securing-traditional-ml.md](securing-traditional-ml.md): adversarial examples, data poisoning, model extraction, membership inference
- **Generative AI** → [securing-genai.md](securing-genai.md): prompt injection, jailbreaks, data leakage, output-triggered attacks
- **Agentic AI** → [securing-agentic-ai.md](securing-agentic-ai.md): tool-use abuse, identity/authorization compromise, excessive agency, multi-agent manipulation
- **Supply chain** → [supply-chain-security.md](supply-chain-security.md): compromised base models, poisoned pretraining/fine-tuning data, vulnerable dependencies, malicious third-party tools/connectors

## Using this threat model

1. During [02-ai-lifecycle/requirements-and-design.md](../02-ai-lifecycle/requirements-and-design.md), walk each lifecycle stage against the system's actual architecture and note which apply
2. Map applicable threats to controls — see each system-type file's control table
3. Feed applicable threats into [security-testing-program.md](security-testing-program.md) scope
4. Reference [09-tools-and-frameworks/MITRE-ATLAS.md](../09-tools-and-frameworks/MITRE-ATLAS.md) and [09-tools-and-frameworks/OWASP-llm-top10.md](../09-tools-and-frameworks/OWASP-llm-top10.md) for the detailed technique-level taxonomies this model summarizes

## Related

- [01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md) — security risk sits within the broader risk taxonomy
- [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md) — the principle this threat model operationalizes
