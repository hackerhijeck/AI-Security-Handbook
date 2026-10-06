# OWASP AI Security Map

OWASP's **GenAI Security Project** hosts several related resources. Know which one to use.

| Resource | Use it for |
|---|---|
| **OWASP Top 10 for LLM Applications (2025)** | Awareness list of top risks in LLM apps. Start here. |
| **OWASP Top 10 for Agentic Applications (2026)** | Risks of autonomous agents (ASI01 to ASI10), published Dec 2025. |
| **OWASP Machine Learning Security Top 10** | Classic ML risks (poisoning, inversion, theft). |
| **OWASP AI Exchange** | Deep, living guidance on AI threats and controls; maps to standards. |
| **OWASP AI Security & Privacy Guide** | Practical guidance for secure and privacy-preserving AI. |
| **OWASP LLM/GenAI Red Teaming Guide** | Method for testing GenAI systems. |
| **OWASP MCP Top 10** | Risks specific to Model Context Protocol servers/clients. |
| **OWASP AIVSS** | Work toward scoring AI vulnerabilities (check current status). |

Tip: the Top 10 lists are **awareness documents**, not complete standards. Pair them with NIST AI RMF (risk process), ISO/IEC 42001 (management system) and MITRE ATLAS (attack techniques).

## Mapping LLM Top 10 to Agentic Top 10 (rough)
| LLM Top 10 (2025) | Closest agentic risk |
|---|---|
| LLM01 Prompt Injection | ASI01 Agent Goal Hijack |
| LLM06 Excessive Agency | ASI02 Tool Misuse, ASI03 Identity & Privilege Abuse |
| LLM03 Supply Chain | ASI04 Agentic Supply Chain |
| LLM05 Improper Output Handling | ASI05 Unexpected Code Execution |
| LLM04 Data & Model Poisoning, LLM08 Vector/Embedding | ASI06 Memory & Context Poisoning |
| (new in agentic) | ASI07 Insecure Inter-Agent Comms, ASI08 Cascading Failures |
| LLM09 Misinformation | ASI09 Human-Agent Trust Exploitation |
| (new in agentic) | ASI10 Rogue Agents |
