# Playbook: Gen AI App Launch Checklist

## Requirements and design
- [ ] Intended use and out-of-scope use documented ([02-ai-lifecycle/opportunity-and-use-case.md](../02-ai-lifecycle/opportunity-and-use-case.md))
- [ ] Risk tier assigned ([03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md))
- [ ] Hallucination tolerance and grounding approach defined for this use case ([06-generative-ai/hallucination-and-grounding.md](../06-generative-ai/hallucination-and-grounding.md))

## Data and grounding
- [ ] RAG corpus (if applicable) access-controlled at retrieval time, not just at the source ([06-generative-ai/RAG-governance.md](../06-generative-ai/RAG-governance.md))
- [ ] Fine-tuning data (if applicable) governed per [06-generative-ai/fine-tuning-governance.md](../06-generative-ai/fine-tuning-governance.md)
- [ ] PII handling reviewed for prompts, outputs, and logs ([06-generative-ai/data-leakage.md](../06-generative-ai/data-leakage.md))

## Safety and security
- [ ] Input/output guardrails implemented and tested ([08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md))
- [ ] Prompt injection and jailbreak red-teaming completed ([06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md), [06-generative-ai/jailbreaks.md](../06-generative-ai/jailbreaks.md))
- [ ] OWASP LLM Top 10 checklist reviewed ([09-tools-and-frameworks/OWASP-llm-top10.md](../09-tools-and-frameworks/OWASP-llm-top10.md))

## Evaluation
- [ ] Golden test set / regression suite in place ([06-generative-ai/genai-evaluation.md](../06-generative-ai/genai-evaluation.md))
- [ ] Fairness/bias probes run on generated content ([08-controls-and-techniques/fairness-testing](../08-controls-and-techniques/fairness-testing/))
- [ ] Groundedness/citation quality validated for RAG outputs

## Transparency
- [ ] AI-interaction disclosure implemented for end users
- [ ] AI-generated content labeling implemented where applicable ([06-generative-ai/content-provenance.md](../06-generative-ai/content-provenance.md))

## Deployment
- [ ] Staged rollout plan defined ([02-ai-lifecycle/deployment-and-release.md](../02-ai-lifecycle/deployment-and-release.md))
- [ ] Rollback criteria defined and kill switch tested
- [ ] Monitoring dashboards and alerting live before traffic ([02-ai-lifecycle/monitoring-and-observability.md](../02-ai-lifecycle/monitoring-and-observability.md))

## Governance
- [ ] Model/system card completed ([model-card-template.md](model-card-template.md))
- [ ] Tier 1: governance board sign-off obtained ([03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md))
- [ ] Entry added to AI inventory

## Legal/IP
- [ ] Vendor terms reviewed for data use and IP indemnification ([06-generative-ai/copyright-and-ip.md](../06-generative-ai/copyright-and-ip.md))
- [ ] Applicable regulation reviewed for jurisdiction/sector ([10-regulations-and-standards](../10-regulations-and-standards/), [11-sector-specific-ai](../11-sector-specific-ai/))
