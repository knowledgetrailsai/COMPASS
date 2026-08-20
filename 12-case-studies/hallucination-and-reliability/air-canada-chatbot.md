# Air Canada Chatbot Bereavement Fare Case

**Context**: Air Canada customer service chatbot, incident and subsequent tribunal ruling reported in early 2024.

**AI system**: Generative AI — a customer-facing support chatbot on Air Canada's website.

**What happened**: A customer asked the airline's chatbot about bereavement fare policy; the chatbot gave inaccurate information (stating the customer could apply for a bereavement discount retroactively after booking at full price), which contradicted the airline's actual policy. The customer relied on the chatbot's answer, booked accordingly, and was later denied the discount. Air Canada argued the chatbot was "a separate legal entity responsible for its own actions" and that the airline shouldn't be liable for its output. Canada's Civil Resolution Tribunal rejected this argument, ruled Air Canada responsible for information provided by its chatbot, and ordered the airline to pay damages.

**Root cause**: A hallucinated/incorrect policy statement from the Gen AI chatbot, combined with no apparent grounding mechanism tying chatbot answers to authoritative, current policy documentation, and no human review before the information reached the customer — see [06-generative-ai/hallucination-and-grounding.md](../../06-generative-ai/hallucination-and-grounding.md).

**Risk category**: Hallucination and factual accuracy risk; accountability risk (the "chatbot is a separate entity" defense being a direct test of [05-responsible-ai-principles/accountability-and-human-oversight.md](../../05-responsible-ai-principles/accountability-and-human-oversight.md)).

**Lifecycle stage where it could have been caught**: [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md) (should have required grounding for policy-sensitive answers) and [02-ai-lifecycle/evaluation-and-validation.md](../../02-ai-lifecycle/evaluation-and-validation.md) (hallucination testing on policy-related queries specifically).

**Control failure**: No RAG-style grounding tying chatbot responses to the airline's actual current policy documents ([06-generative-ai/RAG-governance.md](../../06-generative-ai/RAG-governance.md)); no apparent disclaimer or human-verification step for policy-specific, financially consequential answers.

**Impact**: Direct financial harm to the individual customer (relatively small in this instance), but the ruling's significance is much broader — establishing that an organization is legally accountable for its Gen AI chatbot's output, a precedent widely cited afterward.

**Regulatory implications**: Tribunal ruling holding the company liable — not a regulatory fine, but a legal precedent frequently cited in subsequent discussions of Gen AI accountability and a cautionary example used across industries.

**Lessons learned**: "The AI said it, not us" is not a viable legal or practical defense — organizations are accountable for their Gen AI systems' output as they would be for any employee's statements. Any customer-facing Gen AI system answering policy/financial questions needs grounding and disclosure appropriate to the stakes.

**Preventive controls**: RAG grounding requiring chatbot policy answers to cite current official policy; human review or escalation for financially consequential, policy-specific queries; clear internal ownership of chatbot content accuracy rather than treating the chatbot as autonomous/unaccountable.

**Sources**: Widely reported, including CBC News and multiple legal/industry analyses of the Civil Resolution Tribunal of British Columbia decision, *Moffatt v. Air Canada* (2024).
