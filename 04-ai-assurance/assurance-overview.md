# AI Assurance — Overview

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

## Definition

AI Assurance answers: "How do I know that my AI system is actually responsible?" — the systematic, evidence-based verification that principles, governance, and controls are functioning as intended, not just documented as intended.

## The assurance chain

```
Principles → Risks → Requirements → Controls → Test/Evaluate → Evidence → Assurance
```

Assurance sits at the end of this chain but depends on every link before it: you can't produce credible assurance evidence for controls that were never tested, or for requirements that were never made specific enough to test against.

## Assurance activities in this section

| File | Covers |
|---|---|
| [AI-impact-assessment.md](AI-impact-assessment.md) | Structured assessment of an AI system's potential impact before/during development |
| [AI-risk-assessment.md](AI-risk-assessment.md) | Structured risk identification and scoring methodology |
| [conformity-assessment.md](conformity-assessment.md) | Formal assessment against a regulatory standard (e.g., EU AI Act high-risk conformity) |
| [model-validation.md](model-validation.md) | Technical validation that a model performs as claimed |
| [independent-assessment.md](independent-assessment.md) | Why and how to use assessors independent of the build team |
| [audit.md](audit.md) | Periodic, systematic review of live systems and governance processes |
| [red-teaming.md](red-teaming.md) | Adversarial testing methodology |
| [evidence-and-traceability.md](evidence-and-traceability.md) | Documentation artifacts that make assurance possible |
| [assurance-reporting.md](assurance-reporting.md) | How assurance findings get communicated to governance, leadership, and regulators |

## Levels of assurance

| Level | Who verifies | Appropriate for |
|---|---|---|
| **Self-assessment** | Build team | Tier 3 (low risk) |
| **Internal independent review** | Different internal team (e.g., central RAI/security function) | Tier 2, and Tier 1 as a baseline |
| **Third-party independent assessment** | External auditor/assessor | Tier 1, regulatory-mandated conformity assessment, high public trust stakes |
| **Certification** | Accredited certification body against a standard (e.g., ISO/IEC 42001) | Organization-wide management system claims, contractual/regulatory requirement |

Higher assurance levels cost more and take longer — match the level to the risk tier from [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) rather than defaulting to maximum rigor everywhere or minimum rigor everywhere.

## Assurance is continuous, not a one-time certificate

A system validated at launch can drift out of compliance as data, usage, or the model itself changes. Assurance activities should recur — audits, periodic red-teaming, and re-validation — tied into [02-ai-lifecycle/monitoring-and-observability.md](../02-ai-lifecycle/monitoring-and-observability.md).
