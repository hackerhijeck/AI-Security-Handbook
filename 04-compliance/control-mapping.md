# Control Mapping Matrix (starter)

Use one control set to satisfy many frameworks. This table is a **starting point**, not an official crosswalk.

| Control | OWASP LLM | OWASP Agentic | NIST AI RMF | ISO 42001 theme | EU AI Act |
|---|---|---|---|---|---|
| AI inventory and classification | all | all | MAP | Resources / lifecycle | Art. 6, 49 |
| Threat modeling | LLM01-10 | ASI01-10 | MAP, MEASURE | Risk assessment (cl. 6) | Art. 9 |
| Prompt injection defenses | LLM01 | ASI01 | MANAGE | Operation (cl. 8) | Art. 15 |
| Data sanitization and DLP | LLM02 | ASI03 | MANAGE | Data for AI | Art. 10 |
| Supply chain vetting, AI-BOM | LLM03 | ASI04 | GOVERN | Third-party | Art. 15, 25 |
| Data provenance and integrity | LLM04, LLM08 | ASI06 | MAP, MEASURE | Data for AI | Art. 10 |
| Output validation | LLM05 | ASI05 | MANAGE | Operation | Art. 15 |
| Least privilege and approvals | LLM06 | ASI02, ASI03 | MANAGE | Use of AI systems | Art. 14 |
| Secrets management | LLM07 | ASI03 | MANAGE | Operation | Art. 15 |
| Grounding and evaluation | LLM09 | ASI09 | MEASURE | Lifecycle | Art. 13, 15 |
| Rate limits, budgets | LLM10 | ASI08 | MANAGE | Operation | Art. 15 |
| Logging and monitoring | all | ASI10 | MEASURE, MANAGE | Performance eval (cl. 9) | Art. 12 |
| Human oversight | LLM06 | ASI09 | GOVERN | Use of AI systems | Art. 14 |
| Incident response | all | ASI08 | MANAGE | Improvement (cl. 10) | Art. 73 |
| Red teaming / testing | all | all | MEASURE | Performance eval | Art. 9, 15 |
| Training and AI literacy | - | ASI09 | GOVERN | Support (cl. 7) | Art. 4 |

## How to use
1. List your controls in a register.
2. Tag each with framework references.
3. Collect one piece of evidence per control.
4. Reuse evidence across audits.
