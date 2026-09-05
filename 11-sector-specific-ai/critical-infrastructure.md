# Critical Infrastructure

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/README.md)*

## Common AI use cases
Energy grid optimization and load balancing, water treatment monitoring, transportation/traffic control systems, telecommunications network management, industrial control system (ICS/SCADA) anomaly detection, agentic operational assistants for infrastructure control.

## Sector-specific risk emphasis
- **Systemic and cascading failure risk**: a failure isn't contained to one user or transaction — it can cascade across a grid, network, or region, making [05-responsible-ai-principles/robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md) and fail-safe design the central concern, arguably above even the manufacturing sector's emphasis given the scale of potential impact
- **Security as the dominant risk category**: critical infrastructure is a high-value target for adversarial attack (nation-state and criminal); AI components expand the attack surface described in [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md) and warrant the most rigorous application of [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md)
- **Agentic control authority**: an agent with actual control authority over infrastructure (not just monitoring/recommendation) is among the highest-stakes autonomy categories in this entire repository. Apply the most conservative end of [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md), generally reserving anything beyond L1 (human approval) for narrow, extensively validated scenarios
- **National security overlay**: critical infrastructure AI often intersects with national security regulation distinct from general AI/data protection law, adding a compliance dimension not present in most other sectors in this section

## Applicable regulation (illustrative)
Sector-specific critical infrastructure security regulation (e.g., NERC CIP for the North American power grid, equivalent bodies elsewhere) generally applies to AI components the same as any other control system element; general AI regulation frequently classifies critical infrastructure safety components as high-risk by default (e.g., EU AI Act); national cybersecurity/critical infrastructure protection law layers on top.

## Control emphasis
- Air-gapped or heavily restricted network access for AI components with control authority, consistent with existing ICS/OT security practice, extended to cover AI-specific attack vectors (prompt injection via any natural-language interface layered onto control systems)
- Extensive red-teaming specifically targeting AI-mediated attack paths into control systems; this sector should treat [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md) as continuous, not periodic
- Verified, tested fail-safe/manual-override capability independent of the AI system, maintained and drilled regularly

## Assurance emphasis
Integrate with existing critical infrastructure security assurance programs (which are typically mature and regulator-supervised) rather than building parallel AI-specific assurance — the goal is extending established rigor to cover new AI-specific risk, not creating a separate lower-rigor track for AI components.
