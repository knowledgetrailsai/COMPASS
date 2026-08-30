# Risk Taxonomy

*[Home](../INDEX.md) › [01 · Foundations](../01-foundations/ai-ethics.md)*

A structured way to categorize what can go wrong with an AI system, used consistently across risk assessments (see [13-implementation-playbooks/conducting-an-ai-risk-assessment.md](../13-implementation-playbooks/conducting-an-ai-risk-assessment.md)).

## 1. Bias and fairness risk
Model or system produces systematically unfair outcomes for individuals or groups. Sources: unrepresentative training data, proxy variables for protected attributes, label bias, feedback loops.

## 2. Hallucination and factual accuracy risk (Gen AI)
Model generates plausible but false or unverifiable content, presented with unwarranted confidence. Especially dangerous in high-stakes domains (legal, medical, financial advice).

## 3. Privacy and data risk
Unauthorized collection, use, retention, or leakage of personal data — including model memorization of training data, PII surfacing in RAG context or outputs, and re-identification risk.

## 4. Security risk
Adversarial manipulation of the system: prompt injection, jailbreaks, data poisoning, model extraction, adversarial examples, and — for agentic systems — exploitation of tool access to take unauthorized actions.

## 5. Misuse and dual-use risk
Legitimate capability used for harmful purposes: deepfakes, disinformation, fraud, CSAM, weapons-related information, automated harassment.

## 6. IP and copyright risk
Generated content infringes third-party copyright or trademarks, or training data itself was used without proper rights; ambiguity around ownership of AI-generated output.

## 7. Autonomy and control risk (Agentic AI)
Agent takes actions beyond intended scope, misinterprets goals, or cascades errors across multi-step plans or multi-agent systems without adequate human oversight.

## 8. Robustness and reliability risk
System fails or degrades under distribution shift, edge cases, or unexpected inputs, producing silently wrong outputs rather than failing safely.

## 9. Societal and systemic risk
Aggregate effects across many users/deployments: labor market disruption, homogenization of information/opinion, erosion of trust in authentic content, concentration of power.

## 10. Environmental risk
Energy and water consumption from training and inference at scale, particularly for large generative models.

## 11. Legal and regulatory risk
Non-compliance with applicable law (EU AI Act, DPDP Act, sector regulation) resulting in fines, injunctions, or mandated system changes.

## Severity × likelihood framing

Each risk should be assessed on:
- **Severity**: reversibility, scale of harm, whether it affects vulnerable groups
- **Likelihood**: how easily triggered (accidental vs. requires adversarial effort)
- **Detectability**: how quickly the organization would notice if it occurred

This feeds directly into the risk-tiering approach in [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md).
