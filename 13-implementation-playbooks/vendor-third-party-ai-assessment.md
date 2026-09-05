# Playbook: Vendor / Third-Party AI Assessment

*[Home](../INDEX.md) › [13 · Implementation Playbooks](../13-implementation-playbooks/agentic-deployment-checklist.md)*

Working checklist implementing [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md).

## Discovery
- [ ] Identify what AI capability the vendor product actually uses (ask directly (don't assume from marketing)) which model(s), whether it's agentic/tool-using
- [ ] Determine what data will flow to the vendor and in what form

## Risk tiering
- [ ] Apply [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) tiering to the vendor's AI feature the same as an internal system

## Data handling
- [ ] Confirm whether your data is used to train the vendor's models (default should be no for enterprise use), get this in writing, not just in a sales conversation
- [ ] Confirm retention, deletion, and data residency terms
- [ ] Confirm sub-processor list (does the vendor itself rely on another AI provider?)

## Security
- [ ] Vendor security review appropriate to data sensitivity and access level
- [ ] For agentic vendor features: what tool/action access does the vendor's AI have on your behalf, and how is it scoped? ([07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md))

## Evaluation evidence
- [ ] Request available bias/safety testing results or documentation (model card / system card equivalent)
- [ ] If unavailable, weigh this gap explicitly in the risk assessment rather than assuming compliance

## Legal and IP
- [ ] IP indemnification for output infringement claims ([06-generative-ai/copyright-and-ip.md](../06-generative-ai/copyright-and-ip.md))
- [ ] Liability allocation for AI errors/incidents
- [ ] Data Processing Agreement in place for any personal data

## Regulatory alignment
- [ ] Vendor supports your compliance obligations for applicable jurisdictions ([10-regulations-and-standards](../10-regulations-and-standards/global-overview.md))
- [ ] For EU AI Act-applicable use: clarity on provider vs. deployer obligation split with the vendor

## Ongoing governance
- [ ] Entry added to AI inventory, tracked alongside internal systems
- [ ] Recurring review cadence set (not a one-time sign-off) — vendor features and terms change
- [ ] Vendor AI incidents included in your incident response scope if they affect your data/users

## Decision
- [ ] Approve / approve with conditions / reject, documented with rationale, routed per [03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md) for Tier 1 vendor use cases
