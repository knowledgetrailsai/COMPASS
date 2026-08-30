# Third-Party AI Governance

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/AI-assurance.md)*

## Why this needs its own discipline

Most organizations' AI risk increasingly comes from AI embedded in third-party products (SaaS tools with AI features, foundation model APIs, AI-powered vendor services) rather than AI built entirely in-house. Third-party AI needs assessment and ongoing governance, not a one-time procurement checkbox.

## What to assess before adoption

- **Model/vendor transparency**: what model(s) power the feature, and does the vendor disclose enough to assess risk (or is it an opaque black box with no documentation)?
- **Data handling**: is your data used to train the vendor's models? What are retention, deletion, and data residency terms? (See [09-tools-and-frameworks](../09-tools-and-frameworks/commercial-platforms.md) for platform-specific notes.)
- **Security posture**: has the vendor undergone security review appropriate to the data/access it will have?
- **Bias/safety testing evidence**: has the vendor conducted and can they share evaluation results relevant to your use case?
- **IP/liability terms**: indemnification for output infringement claims, liability allocation for AI errors — see [06-generative-ai/copyright-and-ip.md](../06-generative-ai/copyright-and-ip.md)
- **Regulatory alignment**: does the vendor support your compliance obligations (e.g., EU AI Act provider/deployer obligations, DPDP Act data processor requirements)?
- **Agentic-specific**: if the vendor's AI can take actions on your behalf (send communications, modify records, make purchases), assess the same tool-permission and autonomy questions as an internally-built agent — see [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md).

## Ongoing governance (not just at onboarding)

- Track vendor AI features in the AI inventory alongside internally-built systems
- Monitor for vendor changes (new AI features silently enabled by default, changed data-use terms) — a recurring review cadence, not a one-time sign-off
- Include vendor AI incidents in your own incident response scope if they affect your data or users

## Process

Full assessment checklist: [13-implementation-playbooks/vendor-third-party-ai-assessment.md](../13-implementation-playbooks/vendor-third-party-ai-assessment.md).

## Risk tiering applies here too

Apply [risk-management.md](risk-management.md) tiering to third-party AI the same way as internal systems — a vendor chatbot handling sensitive customer data is Tier 1 regardless of who built the underlying model.
