# EU AI Act

*[Home](../../INDEX.md) › [10 · Regulations & Standards](../../10-regulations-and-standards/global-overview.md) › [EU](../../10-regulations-and-standards/EU/eu-ai-act.md)*

_Type: Law (Regulation (EU) 2024/1689). Last reviewed: 2026-08-19 — this is an actively evolving regulation; confirm current deadlines and requirements with legal counsel before relying on any specific date below._

## Overview

The EU AI Act is the first comprehensive, horizontal (cross-sector) AI-specific law, using a risk-tiered approach: obligations scale with the AI system's potential risk to health, safety, and fundamental rights.

## Risk tiers

| Tier | Examples | Obligation level |
|---|---|---|
| **Unacceptable risk** | Social scoring, manipulative/subliminal techniques, most real-time remote biometric identification in public spaces for law enforcement | Prohibited outright |
| **High risk** | AI in employment, credit/lending, education access, law enforcement, critical infrastructure, migration/asylum, certain medical devices | Extensive obligations: risk management system, data governance, technical documentation, logging, transparency, human oversight, accuracy/robustness/cybersecurity, conformity assessment |
| **Limited risk** | Chatbots, deepfakes, emotion recognition systems | Transparency obligations (disclosure that AI is involved / content is AI-generated) |
| **Minimal risk** | Most AI applications (spam filters, AI-enabled games) | No mandatory obligations beyond general law |

## General-Purpose AI (GPAI) obligations

Separate obligations apply to providers of general-purpose AI models (the foundation models underlying many Gen AI applications), including technical documentation, transparency to downstream providers, and — for models with "systemic risk" (generally the most capable models by compute/capability thresholds) — additional risk assessment, adversarial testing, and incident reporting obligations.

## Timeline status (as of this review)

The AI Act entered into force in August 2024 with a phased implementation. Prohibited-practice obligations and AI literacy requirements applied earliest (2025). GPAI obligations followed. **High-risk system obligations, originally targeted for August 2026, have been postponed to December 2027** under the EU's "Digital Omnibus" simplification package — a timeline adjustment, not a removal of the underlying obligations. Confirm the current official timeline via the European Commission's AI Act service desk before planning against any specific date.

## Practical implications for this repository's framework

- Use [03-ai-governance/risk-management.md](../../03-ai-governance/risk-management.md) tiering, aligned to this Act's tier structure, for any EU-exposed system
- High-risk system requirements map closely to [04-ai-assurance](../../04-ai-assurance/assurance-overview.md) (conformity assessment, [conformity-assessment.md](../../04-ai-assurance/conformity-assessment.md)) and [02-ai-lifecycle](../../02-ai-lifecycle/lifecycle-overview.md) (risk management system across the lifecycle)
- Transparency obligations for limited-risk systems (chatbot disclosure, AI-content labeling) map to [06-generative-ai/content-provenance.md](../../06-generative-ai/content-provenance.md)

## Enforcement

Non-compliance penalties are tiered by severity, with the highest fines (for prohibited-practice violations) set as a percentage of global annual turnover or a fixed amount, whichever is higher — among the most significant AI-specific penalty regimes globally. Confirm current fine structures with counsel given ongoing legislative refinement.

## Related

- [conformity-assessment.md](../../04-ai-assurance/conformity-assessment.md)
- [global-overview.md](../global-overview.md)

Sources:
- [EU AI Act Omnibus Agreement — Postponed High-Risk Deadlines and Other Key Changes (Gibson Dunn)](https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/)
- [The Digital Omnibus and the postponement of high-risk obligations to December 2027](https://www.aiactblog.nl/en/posts/digital-omnibus-high-risk-postponement-december-2027)
- [EU AI Act Timeline — European Commission AI Act Service Desk](https://ai-act-service-desk.ec.europa.eu/en/ai-act/timeline/timeline-implementation-eu-ai-act)
