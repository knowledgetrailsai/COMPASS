# Samsung Employees' Confidential Data Leak via ChatGPT

*[Home](../../INDEX.md) › [12 · Case Studies](../../12-case-studies/) › [privacy-incidents](../../12-case-studies/privacy-incidents/)*

**Context**: Samsung Semiconductor, reported in 2023.

**AI system**: Generative AI — a third-party public Gen AI chatbot (ChatGPT) used informally by employees.

**What happened**: Multiple Samsung employees reportedly pasted confidential company information into a public Gen AI chatbot for legitimate-seeming purposes — including source code to check for errors and to optimize, and confidential meeting notes to generate a summary. Because the data was submitted to a third-party consumer AI service, it left the organization's control, and Samsung had no ability to guarantee it wouldn't be retained, reviewed, or otherwise incorporated by the third party. Samsung subsequently restricted internal use of public generative AI tools and moved toward internally-controlled AI tooling.

**Root cause**: No Acceptable Use Policy governing employee use of external Gen AI tools with confidential data at the time of the incident — a governance gap, not a technical failure of any specific AI system ([03-ai-governance/policy-management.md](../../03-ai-governance/policy-management.md)).

**Risk category**: Privacy and data risk (also a trade-secret/IP exposure risk, adjacent to but distinct from the personal-data-focused privacy risk category).

**Lifecycle stage where it could have been caught**: This falls outside the standard system-development lifecycle entirely — it's a policy/governance gap ([03-ai-governance](../../03-ai-governance/)) applying to third-party tool usage rather than a system Samsung built, illustrating why [03-ai-governance/third-party-ai-governance.md](../../03-ai-governance/third-party-ai-governance.md) needs to cover employee tool use, not just procured/embedded AI products.

**Control failure**: No Acceptable Use Policy restricting confidential data input to external AI tools; no technical control (e.g., data-loss-prevention tooling) blocking sensitive data from leaving the network via a browser-based AI tool.

**Impact**: Source code and internal meeting content exposed to a third party outside company control; scope of downstream risk not fully knowable given data, once submitted, was outside Samsung's visibility.

**Regulatory implications**: No confirmed public regulatory enforcement action reported; the incident became a widely cited example driving many organizations' subsequent adoption of Gen AI acceptable-use policies.

**Lessons learned**: The most common enterprise Gen AI privacy risk is often not a sophisticated technical attack but simple employee use of public consumer tools with sensitive data, absent clear policy. This risk category needs to be addressed before or alongside any internally-built Gen AI system, not after.

**Preventive controls**: Acceptable Use Policy explicitly addressing external Gen AI tool use ([03-ai-governance/policy-management.md](../../03-ai-governance/policy-management.md)); approved-tool list with vetted data-handling terms ([03-ai-governance/third-party-ai-governance.md](../../03-ai-governance/third-party-ai-governance.md)); employee training/awareness; technical DLP controls where feasible.

**Sources**: Widely reported by multiple technology and business outlets in 2023 (e.g., Bloomberg, TechCrunch) covering Samsung's internal memo and subsequent restriction of external Gen AI tool use.
