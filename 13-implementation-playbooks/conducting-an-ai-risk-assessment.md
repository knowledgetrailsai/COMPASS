# Playbook: Conducting an AI Risk Assessment

Working, step-by-step version of [04-ai-assurance/AI-risk-assessment.md](../04-ai-assurance/AI-risk-assessment.md) and [04-ai-assurance/AI-impact-assessment.md](../04-ai-assurance/AI-impact-assessment.md).

## Step 1: Describe the system
- Purpose, intended use, out-of-scope use
- Technology type (traditional ML / Gen AI / Agentic AI) — pull in the relevant section (05/06/07)
- Data used, including any RAG corpus or fine-tuning data
- Autonomy level if agentic ([07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md))

## Step 2: Identify affected parties
- Direct users
- Indirect/non-user affected individuals
- Vulnerable or historically marginalized groups specifically

## Step 3: Walk the risk taxonomy
For each category in [01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md), assess applicability: bias/fairness, hallucination (Gen AI), privacy, security, misuse, IP, autonomy/control (Agentic AI), robustness, societal, environmental, legal/regulatory. Document why a category doesn't apply rather than silently skipping it.

## Step 4: Score each identified risk
Severity × Likelihood × Detectability (1–5 scale each) — see [04-ai-assurance/AI-risk-assessment.md](../04-ai-assurance/AI-risk-assessment.md) methodology.

## Step 5: Determine risk tier
Apply [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) tiering criteria based on the highest-severity applicable risks and the nature of the decision/action the system influences.

## Step 6: Map mitigations
For each risk above the acceptability threshold, identify the specific control from [08-controls-and-techniques](../08-controls-and-techniques/) that addresses it, and the residual risk after mitigation.

## Step 7: Check regulatory and sector requirements
Cross-reference [10-regulations-and-standards](../10-regulations-and-standards/) for applicable jurisdictions and [11-sector-specific-ai](../11-sector-specific-ai/) for the relevant industry.

## Step 8: Document and route for approval
Complete the risk register entry; route to governance board if Tier 1 ([03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md)).

## Step 9: Set review cadence
Define re-assessment triggers (material change) and periodic review date regardless of triggering events.

## Output
A completed risk register entry, referenced by the system's model/system card and available for any future audit ([04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md)).
