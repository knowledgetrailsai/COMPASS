# Policy Management

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/AI-assurance.md)*

## Core AI policies an organization typically needs

### Acceptable Use Policy
What AI (including third-party Gen AI tools) can and cannot be used for internally — covers employee use of external AI tools (e.g., pasting confidential data into a public chatbot) as much as product-embedded AI.

### Approved Model/Vendor List
Which AI models and vendors have passed the organization's risk/security/privacy review and are approved for use, with any use-case-specific restrictions.

### Data Handling Policy for AI
Rules for what data can be used in training/fine-tuning, retention limits for prompts/outputs/logs, and requirements for vendor data processing agreements.

### Human Oversight Policy
Minimum human oversight requirements by risk tier (ties to [02-ai-lifecycle](../02-ai-lifecycle/lifecycle-overview.md) and [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md)) — e.g., "no Tier 1 automated decision without human review" as an organization-wide default.

### Disclosure and Transparency Policy
Requirements for disclosing AI involvement to users/customers, labeling AI-generated content, and providing explanation for automated decisions.

### Third-Party/Vendor AI Policy
Assessment and contracting requirements before adopting a third-party AI tool or model — see [13-implementation-playbooks/vendor-third-party-ai-assessment.md](../13-implementation-playbooks/vendor-third-party-ai-assessment.md).

## Policy lifecycle

1. **Draft** — governance lead drafts, informed by regulatory requirements ([10-regulations-and-standards](../10-regulations-and-standards/global-overview.md)) and organizational risk appetite
2. **Review** — legal, security, privacy, and business stakeholders review
3. **Approve** — governance board or executive sponsor approves
4. **Publish and communicate** — accessible, not buried; paired with training/awareness where behavior change is needed
5. **Enforce** — tie to actual gates (can't deploy without passing acceptable-use/vendor checks) rather than relying on voluntary compliance
6. **Review cadence** — revisit at least annually, and whenever relevant regulation changes materially

## Common failure mode

Publishing a policy without an enforcement mechanism — a policy that isn't checked at an actual gate (procurement, deployment pipeline, code review) tends to be honored only by teams who were already going to comply.
