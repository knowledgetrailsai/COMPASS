# Red-Teaming

## Purpose

Adversarial testing that deliberately tries to make an AI system fail, misbehave, or be misused — surfaces the gap between "works in normal testing" and "resists a motivated adversary or determined misuse attempt."

## Scope by system type

### Traditional ML
Adversarial examples, data poisoning simulation, model extraction attempts, fairness stress-testing with deliberately constructed edge-case subgroups.

### Generative AI
Jailbreak attempts (known techniques and novel ones), prompt injection via realistic untrusted content, attempts to elicit disallowed content categories, attempts to extract training data or system prompts, IP-infringing generation attempts.

### Agentic AI
Attempts to induce out-of-scope tool use, prompt injection via tool outputs/retrieved content designed to hijack agent behavior, attempts to exploit permission boundaries, multi-agent manipulation (in multi-agent systems), and testing whether the agent escalates appropriately under adversarial ambiguity rather than guessing.

## Methodology

1. **Threat modeling**: identify plausible adversaries (curious users, motivated bad actors, competitors, automated attack tools) and their likely goals for this specific system
2. **Reference known attack patterns**: use established taxonomies (OWASP LLM Top 10, MITRE ATLAS — see [09-tools-and-frameworks](../09-tools-and-frameworks/)) as a starting checklist, not a complete list
3. **Manual and automated testing**: combine structured manual red-teaming (creative, adaptive human testers) with automated adversarial test suites for scale and regression coverage
4. **Realistic conditions**: test in an environment as close to production as feasible, including real tool integrations (sandboxed) for agentic systems
5. **Severity rating and reporting**: findings rated by exploitability and impact, reported with enough detail for remediation, retained as an assurance artifact

## Cadence

Before any Tier 1 launch, after material changes (new model version, new tool access, expanded autonomy), and on a recurring cadence (e.g., quarterly) for externally-exposed Gen AI/agentic systems, since new attack techniques emerge continuously.

## Who performs it

Internal security/red-team function at minimum for Tier 1–2; external specialist red-teaming firms for the highest-stakes systems or where independent verification is required for regulatory/customer trust reasons — see [independent-assessment.md](independent-assessment.md).

## Gate

Unresolved high-severity findings should block launch or continued operation regardless of risk tier — red-teaming findings are not advisory for critical severity issues.
