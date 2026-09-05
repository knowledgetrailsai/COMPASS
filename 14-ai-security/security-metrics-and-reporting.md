# Security Metrics and Reporting

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

## Purpose

What to measure to demonstrate AI security posture to governance, leadership, and (where relevant) auditors/regulators — feeding into the broader assurance reporting process in [04-ai-assurance/assurance-reporting.md](../04-ai-assurance/assurance-reporting.md).

## Core metrics

| Metric | What it signals |
|---|---|
| Red-team findings by severity, open vs. closed | Whether known vulnerabilities are being remediated, and how fast |
| Guardrail/classifier trigger rate over time | Rising rate may indicate increased adversarial probing or upstream config drift |
| Blocked/attempted permission-boundary violations (agentic) | Early signal of misconfiguration, injection attempts, or scope-creep pressure |
| Time-to-remediate for critical findings | Program responsiveness |
| Coverage: % of Tier 1 systems with current red-team results | Whether the testing program ([security-testing-program.md](security-testing-program.md)) is keeping pace with the AI portfolio |
| Incident count and severity trend (AI security incidents specifically) | Overall exposure trend, distinct from quality/fairness incident trend |
| Supply chain assessment coverage | % of AI systems with a documented, current bill-of-materials ([supply-chain-security.md](supply-chain-security.md)) |

## Reporting cadence and audience

Follow the structure in [04-ai-assurance/assurance-reporting.md](../04-ai-assurance/assurance-reporting.md), system-owner-level detail continuously, governance board summary at each Tier 1 gate and on a recurring cadence, executive/portfolio-level rollup quarterly.

## Avoid vanity metrics

A metric like "number of red-team tests run" says nothing about actual security posture without pairing it with findings severity and remediation status: prefer outcome-oriented metrics (open critical findings, mean time to remediate) over pure activity counts.

## Related

- [04-ai-assurance/assurance-reporting.md](../04-ai-assurance/assurance-reporting.md)
- [03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md)
