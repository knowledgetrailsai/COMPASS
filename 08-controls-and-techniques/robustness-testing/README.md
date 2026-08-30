# Robustness Testing

*[Home](../../INDEX.md) › [08 · Controls & Techniques](../../08-controls-and-techniques/README.md) › [robustness-testing](../../08-controls-and-techniques/robustness-testing/README.md)*

Implements [05-responsible-ai-principles/robustness-and-reliability.md](../../05-responsible-ai-principles/robustness-and-reliability.md) as concrete testing practices.

## Techniques

### Stress testing
Testing under high load, extreme or boundary input values, and unusual combinations of inputs to find breaking points before real users do.

### Adversarial testing
Deliberately crafted inputs designed to cause misclassification or unwanted behavior — adversarial examples for traditional ML (small perturbations causing large output changes), jailbreak/injection attempts for Gen AI ([06-generative-ai/jailbreaks.md](../../06-generative-ai/jailbreaks.md), [06-generative-ai/prompt-injection.md](../../06-generative-ai/prompt-injection.md)).

### Chaos-engineering-style fault injection
For agentic/compound systems: deliberately inject tool failures, malformed tool outputs, and unexpected environment states to verify the system recovers or fails safely rather than propagating errors silently — see [07-agentic-ai/agentic-evaluation.md](../../07-agentic-ai/agentic-evaluation.md).

### Distribution shift simulation
Testing against data that deliberately diverges from the training/validation distribution (different time period, different population segment, different input format) to characterize graceful-degradation behavior ahead of real-world drift.

### Long-horizon/complexity testing
For Gen AI and agentic systems specifically: performance often degrades as task length/complexity increases — test at realistic, not just simple demo-level, complexity.

### Red-teaming
The most comprehensive adversarial technique, combining creative human testing with structured methodology — see [04-ai-assurance/red-teaming.md](../../04-ai-assurance/red-teaming.md) for full treatment.

## Test design principles

- Include both realistic "accidental" edge cases and deliberately adversarial ones — they surface different failure modes
- Automate what can be automated (regression suites) and reserve creative/manual red-teaming for genuinely novel adversarial thinking
- Test failure *handling*, not just failure *avoidance* — does the system degrade safely when it does fail?

## Tooling

See [09-tools-and-frameworks](../../09-tools-and-frameworks/commercial-platforms.md) for adversarial testing frameworks and MITRE ATLAS as a threat-pattern reference.

## Related

- [14-ai-security/security-testing-program.md](../../14-ai-security/security-testing-program.md) — how this fits into the full AI security testing cadence
