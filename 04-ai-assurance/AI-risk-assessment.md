# AI Risk Assessment

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

## Purpose

The structured methodology for identifying, scoring, and tracking risks for a specific AI system. Feeds risk tiering ([03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md)) and informs what controls and assurance level are proportionate.

## Methodology

### 1. Risk identification
Walk through the risk taxonomy ([01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md)) systematically against the specific system: bias, hallucination, privacy, security, misuse, IP, autonomy/control, robustness, societal, environmental, legal. Not every category applies to every system; document why a category is excluded, not just the ones that are included.

### 2. Scoring
For each identified risk:
- **Severity**: harm magnitude if it occurs (reversibility, scale, vulnerable-group impact)
- **Likelihood**: probability of occurrence (accidental trigger vs. requires adversarial effort)
- **Detectability**: how quickly the organization would notice if it occurred

A simple 1–5 scale per dimension, combined into an overall risk score, is usually sufficient — the goal is consistent relative prioritization, not false precision.

### 3. Mitigation mapping
For each risk above an acceptability threshold, identify the specific control(s) that address it (from [08-controls-and-techniques](../08-controls-and-techniques/README.md)) and the residual risk after mitigation.

### 4. Risk register
Maintain a living risk register per system: risk, score, mitigation, residual score, owner, review date. This is a core assurance artifact: see [evidence-and-traceability.md](evidence-and-traceability.md).

### 5. Review cadence
Re-score at each material lifecycle change ([02-ai-lifecycle](../02-ai-lifecycle/lifecycle-overview.md)) and on a periodic cadence (e.g., annually for Tier 1) regardless of change, since the external threat/regulatory landscape evolves independently of the system itself.

## Agentic AI-specific additions

Score autonomy level and action reversibility explicitly as risk multipliers. The same underlying model error is a higher risk when it can trigger an autonomous, irreversible action than when it produces a reviewed text output. See [07-agentic-ai/agentic-risk-landscape.md](../07-agentic-ai/agentic-risk-landscape.md).

## Output feeds

- [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) tiering decision
- [AI-impact-assessment.md](AI-impact-assessment.md) for broader impact framing
- Governance board review materials for Tier 1 approval
