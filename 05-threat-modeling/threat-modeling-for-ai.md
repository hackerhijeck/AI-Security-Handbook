# Threat Modeling for AI Systems

## Steps
1. **Scope**: what is the system, who uses it, what data and tools?
2. **Diagram**: data flow diagram (DFD) with trust boundaries.
3. **Identify threats**: STRIDE, OWASP lists, MITRE ATLAS.
4. **Rate**: likelihood x impact.
5. **Mitigate**: map controls.
6. **Validate**: test; revisit after changes.

## Key trust boundaries in AI apps
- User <-> application
- Application <-> model provider
- Model <-> retrieved content (untrusted)
- Model <-> tools / APIs / other agents
- Training pipeline <-> data sources
- Model output <-> downstream systems and humans

## STRIDE applied to AI
| STRIDE | AI example | Control |
|---|---|---|
| Spoofing | Fake agent or tool identity; impersonating user in prompts | Strong authN, signed messages |
| Tampering | Data/model poisoning, prompt tampering | Integrity checks, provenance |
| Repudiation | No logs of agent actions | Immutable tracing |
| Information disclosure | Training data leak, prompt leak, cross-tenant RAG | Access control, DLP |
| Denial of service | Token flooding, expensive prompts | Quotas, limits |
| Elevation of privilege | Agent uses admin tool via injection | Least privilege, approvals |

## MAESTRO / agentic layers (CSA)
Consider threats by layer: foundation model, data operations, agent frameworks, deployment infrastructure, evaluation/observability, security/compliance, agent ecosystem.

## Example: customer-support RAG chatbot
- Assets: customer data, internal KB, brand reputation
- Entry points: chat input, uploaded files, KB ingestion
- Top threats: indirect injection via KB doc, cross-customer leakage, hallucinated refund policy, cost abuse
- Controls: per-user retrieval ACL, output filter for PII, approved-policy grounding, rate limits, human escalation

## Example: coding agent with shell tool
- Threats: injected README instructs agent to exfiltrate secrets; malicious dependency suggestion; destructive commands
- Controls: sandbox, no secrets in env, egress allow-list, approval for risky commands, dependency allow-list
