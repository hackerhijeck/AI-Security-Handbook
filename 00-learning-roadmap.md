# Learning Roadmap: AI Security, Risk & Compliance

## Who this is for
Security engineers, developers, GRC/compliance staff, students, and anyone moving into AI security.

## Prerequisites (light)
- Basic security concepts: CIA triad, authentication, authorization, encryption
- Basic web/API knowledge
- Optional: Python basics, how REST APIs work

## 8-week plan

| Week | Focus | Read | Hands-on |
|---|---|---|---|
| 1 | Foundations | `01-fundamentals/*` | Explain the AI attack surface in your own diagram |
| 2 | OWASP LLM Top 10 | `02-owasp/owasp-llm-top10-2025.md` | Try prompt injection on a local/test LLM app |
| 3 | OWASP Agentic + ML | `02-owasp/owasp-agentic-top10-2026.md`, `owasp-ml-top10.md` | Threat-model a simple tool-calling agent |
| 4 | Threat modeling | `05-threat-modeling/*` | Map your agent to MITRE ATLAS techniques |
| 5 | Defenses | `06-defenses/*` | Add input/output validation and least-privilege tools to a demo app |
| 6 | Risk management | `03-risk-management/*` | Fill the AI risk register template |
| 7 | Compliance | `04-compliance/*` | Classify 3 AI use cases under the EU AI Act |
| 8 | Red teaming + capstone | `07-red-teaming/*` | Write a mini AI security assessment report |

## Capstone project
Pick one AI system (chatbot, RAG assistant, or agent). Produce:
1. AI system inventory entry
2. Data flow diagram and threat model
3. OWASP mapping (LLM + Agentic)
4. Risk register (min. 10 risks, scored)
5. Compliance mapping (EU AI Act tier, ISO 42001 controls, NIST AI RMF functions)
6. Test results and remediation plan

## Suggested certifications / courses (verify current availability)
- ISO/IEC 42001 Lead Implementer / Auditor courses
- IAPP AIGP (AI Governance Professional)
- Security vendor AI red-teaming courses; OWASP community training
- Cloud provider AI security learning paths
