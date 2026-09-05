# AI Supply Chain Security

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

## Why AI has a distinct supply chain risk

An AI system's "supply chain" includes not just code dependencies (as in traditional software) but base models, training/fine-tuning data, embeddings, and third-party tools/connectors an agent might call — each a potential point of compromise before the system ever reaches production.

## Supply chain components and risks

### Base/foundation models
Risk: a compromised, backdoored, or simply poorly-vetted third-party model. **Controls**: use models from vendors with transparent training/safety documentation; verify model provenance and checksums where distributed as artifacts; independent evaluation before adoption ([04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md)).

### Training and fine-tuning data
Risk: poisoned or IP-compromised data introduced via a third-party dataset or data vendor. **Controls**: data provenance requirements, datasheets ([02-ai-lifecycle/data-and-data-governance.md](../02-ai-lifecycle/data-and-data-governance.md)), vendor data-rights verification ([06-generative-ai/copyright-and-ip.md](../06-generative-ai/copyright-and-ip.md)).

### Embeddings and vector stores
Risk: compromised or poisoned embeddings affecting RAG retrieval quality/security. **Controls**: same provenance discipline as any data source, access control at the vector store layer ([06-generative-ai/RAG-governance.md](../06-generative-ai/RAG-governance.md)).

### Third-party tools/connectors (including MCP servers)
Risk: a compromised or overly permissive third-party tool extends an agent's attack surface and blast radius directly. **Controls**: review third-party tool data access and action capability with the same rigor as an internal tool, see [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md#third-party-mcp-tool-considerations).

### Open-source libraries and frameworks
Risk: standard software supply chain risk (vulnerable/malicious dependencies), applying to the ML/AI tooling stack (training frameworks, serving infrastructure, guardrail libraries) same as any software. **Controls**: standard software composition analysis and dependency scanning, extended to cover the AI-specific tooling stack.

### Vendor/SaaS AI features
Risk: covered in depth in [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md); data handling, sub-processor chains, and terms-of-service changes are the primary vectors.

## Practical controls summary

- Maintain a bill-of-materials for each AI system: base model + version, fine-tuning data sources, embedding model, vector store, third-party tools/connectors — feeds the AI inventory ([03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md))
- Apply vendor assessment ([13-implementation-playbooks/vendor-third-party-ai-assessment.md](../13-implementation-playbooks/vendor-third-party-ai-assessment.md)) to every supply chain component, not just the primary AI vendor
- Re-assess on component change (new base model version, new tool integration); treat as a material change per [02-ai-lifecycle/lifecycle-overview.md](../02-ai-lifecycle/lifecycle-overview.md)

## Related

- [09-tools-and-frameworks/OWASP-llm-top10.md](../09-tools-and-frameworks/OWASP-llm-top10.md) (Supply Chain Vulnerabilities category)
- [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md)
