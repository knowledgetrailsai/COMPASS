# Core Principles

*[Home](../INDEX.md) › [01 · Foundations](../01-foundations/ai-ethics.md)*

Most organizational and regulatory RAI frameworks (OECD AI Principles, NIST AI RMF, EU AI Act, ISO/IEC 42001) converge on a similar set of principles. This guide organizes them into eight pillars; each has a dedicated deep-dive in [05-responsible-ai-principles](../05-responsible-ai-principles/accountability-and-human-oversight.md).

## 1. Fairness and non-discrimination
AI systems should not create or amplify unjust bias against individuals or groups, particularly on protected attributes (race, gender, age, disability, etc.). Applies to training data, model outputs, and downstream decisions.

## 2. Transparency and explainability
Stakeholders should be able to understand, to an appropriate degree, how and why an AI system produced a given output. And should know when they are interacting with AI at all (disclosure).

## 3. Privacy and data protection
AI systems must respect data minimization, consent, and purpose limitation, and protect personal data from misuse, leakage, or re-identification: across training data, retrieval context, and generated outputs.

## 4. Safety and security
Systems should be robust against misuse, adversarial attacks (prompt injection, jailbreaks, data poisoning), and should not cause physical, psychological, financial, or societal harm.

## 5. Accountability and human oversight
There must be clear ownership for AI system behavior, mechanisms for human review/override, and the ability to contest or appeal AI-driven decisions. Critical for Agentic AI, where autonomous action raises the stakes.

## 6. Robustness and reliability
Systems should perform consistently under normal and edge-case conditions, degrade gracefully, and be resilient to distribution shift, adversarial inputs, and unexpected environments.

## 7. Accessibility and human-centered design
AI systems should be usable by and beneficial to a broad range of people, and designed with the people affected by them in mind — not just the people building them.

## 8. Sustainability
Consideration of the environmental cost (compute, energy, water) of training and operating AI systems, particularly large generative models, and efforts to reduce it where feasible.

## How these apply differently by system type

| Principle | Traditional ML | Generative AI | Agentic AI |
|---|---|---|---|
| Fairness | Bias in scoring/classification | Biased or stereotyped generated content | Bias in autonomous decisions/actions |
| Transparency | Feature importance, model cards | Content disclosure, source attribution | Action logs, decision rationale |
| Privacy | Training data protection | PII leakage in outputs, memorization | Data accessed via tool calls |
| Safety | Model misuse | Jailbreaks, harmful content generation | Unauthorized/harmful actions via tools |
| Accountability | Model owner sign-off | Content moderation ownership | Human-in-the-loop approval gates |

## Using these principles

Principles alone don't prevent harm; they need to be translated into concrete checkpoints (section 02), techniques (section 06), and tooling (section 07). Treat this page as the shared vocabulary the rest of the guide builds on.
