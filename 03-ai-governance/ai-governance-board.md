# AI Governance Board

## Purpose

The cross-functional decision-making body for AI risk — approves high-risk use cases, sets policy, resolves edge cases, and reviews incidents. Distinct from a single "AI ethics committee" in that it has real decision authority, not just advisory input.

## Composition

Typical membership: governance lead (chair), senior representation from product/engineering, legal, privacy, security, and — for organizations with the maturity for it — an ethics or DEI voice and a business-risk/compliance voice. Size should stay small enough to make timely decisions (5–8 members is typical) with the ability to pull in subject-matter experts per case.

## Responsibilities

- Approve or reject Tier 1 use cases before development investment and again before production deployment (per [02-ai-lifecycle/lifecycle-overview.md](../02-ai-lifecycle/lifecycle-overview.md))
- Set and periodically review organization-wide AI policy (acceptable use, approved model/vendor list, risk-tiering criteria)
- Review escalated edge cases where risk tier or ethical acceptability is genuinely unclear
- Review SEV1/SEV2 incidents and approve remediation plans
- Own the risk appetite statement — how much AI risk the organization is willing to accept, and where the hard lines are (Tier 0 prohibited uses)

## Operating cadence

- Regular standing meeting (e.g., biweekly) for the normal review queue
- Expedited/emergency process for time-sensitive approvals and incident response — define this in advance so it isn't improvised
- Periodic (e.g., quarterly) review of the full AI inventory and risk posture, not just individual case decisions

## Decision record-keeping

Every Board decision (approval, rejection, conditions attached) should be documented with rationale, tied to the specific system in the AI inventory — this is both a governance and an assurance artifact (see [04-ai-assurance](../04-ai-assurance/)).

## Avoiding bottleneck failure

A Board that reviews everything becomes a bottleneck teams route around. Keep the Board focused on genuinely Tier 1 decisions and policy-setting; push Tier 2–3 to well-designed self-certification (see [governance-models.md](governance-models.md)) so the Board's scrutiny stays high-value and timely.
