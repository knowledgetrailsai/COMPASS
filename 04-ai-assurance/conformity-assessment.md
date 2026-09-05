# Conformity Assessment

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

## What it is

A formal process demonstrating that an AI system meets a specific regulatory standard's requirements before it can be placed on the market or put into service — most concretely defined today under the EU AI Act for high-risk AI systems.

## EU AI Act conformity assessment (illustrative — verify current requirements)

High-risk AI systems under the EU AI Act generally require:
- A documented risk management system spanning the system's lifecycle
- Data governance meeting specified quality criteria
- Technical documentation (comparable to a detailed system card)
- Record-keeping / logging capability
- Transparency and instructions for use
- Human oversight measures
- Accuracy, robustness, and cybersecurity requirements

Depending on the specific high-risk category, conformity assessment is either:
- **Internal (self-assessment)**: the provider assesses and declares conformity itself, for most high-risk categories
- **Third-party (notified body)**: an accredited external body assesses conformity, required for specific higher-scrutiny categories (e.g., certain biometric systems)

See [10-regulations-and-standards/EU/eu-ai-act.md](../10-regulations-and-standards/EU/eu-ai-act.md) for detail, and verify current requirements with legal counsel given this is an actively-implemented regulation.

## General conformity assessment pattern (applies beyond the EU AI Act)

1. Determine which regulatory regime(s) apply based on jurisdiction and use case
2. Map the regime's specific requirements to your system's actual design and documentation
3. Conduct the assessment (self or third-party, per the regime's requirement)
4. Produce a conformity declaration / certificate
5. Register the system where required (e.g., an EU database for certain high-risk categories)
6. Maintain conformity post-market, re-assess on material system changes

## Relationship to other assurance activities

Conformity assessment is the most formal, regulation-anchored form of assurance in this section; it typically requires the outputs of [AI-impact-assessment.md](AI-impact-assessment.md), [model-validation.md](model-validation.md), and [evidence-and-traceability.md](evidence-and-traceability.md) as inputs, rather than being a standalone exercise.

## Practical note

Conformity assessment obligations are new and evolving across jurisdictions. Treat this file as a conceptual map, not a compliance checklist — confirm current, binding requirements with legal counsel before relying on any specific procedural detail.
