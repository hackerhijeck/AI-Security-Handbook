# AI Risk Register Template

| ID | System | Risk description | Category | OWASP ref | Likelihood (1-5) | Impact (1-5) | Score | Existing controls | Treatment | Owner | Due | Residual | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | Support chatbot | Indirect prompt injection via KB leads to data leak | Security | LLM01, LLM02 | 4 | 4 | 16 | Output DLP | Mitigate: per-user retrieval ACL, injection tests | Security lead | 2026-12-31 | 8 | Open |
| R-002 | HR screening model | Biased ranking of candidates | Fairness/Legal | n/a | 3 | 5 | 15 | Manual review | Mitigate: bias testing, human oversight | AI owner | 2027-03-31 | 6 | Open |
| R-003 | Coding agent | Malicious dependency suggestion | Supply chain | LLM03, ASI04 | 3 | 4 | 12 | Dependency scanner | Mitigate: allow-list, approval | Eng lead | 2026-11-30 | 6 | Open |

Score = Likelihood x Impact. Bands: 1-4 Low, 5-9 Medium, 10-16 High, 17-25 Critical.
