# Manufacturing

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/)*

## Common AI use cases
Predictive maintenance, quality control/defect detection, supply chain optimization, robotics and autonomous equipment control, agentic production-planning assistants.

## Sector-specific risk emphasis
- **Physical safety**: AI controlling or informing physical equipment/robotics carries direct worker and public safety risk — closely related to but distinct from healthcare's safety emphasis, with industrial safety standards as the relevant baseline rather than clinical ones
- **Robustness under real-world operating conditions**: manufacturing environments are noisy, variable, and safety-critical — [05-responsible-ai-principles/robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md) is central, with particular emphasis on graceful failure (safe shutdown) over silent wrong output
- **Agentic control of physical systems**: an agent with the ability to actually control equipment (not just recommend) is a materially higher-stakes autonomy category than most software-only agentic use cases — apply the most conservative end of [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md)
- **Supply chain/vendor AI risk**: AI embedded in third-party industrial equipment/software extends the assessment scope beyond internally-built systems — see [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md)

## Applicable regulation (illustrative)
Existing industrial safety and equipment regulation (occupational safety authorities, sector-specific machinery safety standards) generally applies to AI-driven equipment the same as any other control system; general AI regulation may classify safety-component AI in critical machinery as high-risk (e.g., EU AI Act's treatment of AI as a safety component of regulated products).

## Control emphasis
- Fail-safe design as a hard requirement for any AI with physical control authority — default to safe shutdown/human handoff on uncertainty, not "best guess and continue"
- Extensive real-world condition testing (not just clean lab/simulation data) before deployment — see [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/)
- Human oversight/kill-switch requirements verified under realistic operating conditions, not just in a test environment

## Assurance emphasis
Integrate AI assurance activities with existing industrial safety certification processes (e.g., functional safety standards) rather than building a parallel AI-only assurance track — the physical safety domain already has mature assurance practice that AI-specific assurance should extend, not duplicate.
