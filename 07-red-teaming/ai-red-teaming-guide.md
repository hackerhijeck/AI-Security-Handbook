# AI Red Teaming Guide (Defensive Testing)

Only test systems you own or have written permission to test.

## Goals
Find security, safety and misuse weaknesses before attackers do.

## Process
1. **Scope and rules of engagement**: systems, data, allowed techniques, stop conditions.
2. **Recon**: models, tools, data sources, guardrails, users.
3. **Threat-led test plan**: map to OWASP LLM/Agentic and ATLAS.
4. **Execute** manual + automated tests.
5. **Triage and score**: severity by impact and exploitability.
6. **Report and remediate**: reproducible steps, fix guidance.
7. **Retest** and add regression tests.

## Test areas
| Area | Example tests |
|---|---|
| Prompt injection | Direct, indirect (docs, web, email, images), multi-turn, encoded/obfuscated |
| Data leakage | System prompt extraction, PII elicitation, cross-tenant retrieval |
| Output handling | Payload generation that reaches browsers, DBs, shells |
| Agency | Unauthorized tool use, privilege escalation, approval bypass |
| RAG | Poisoned doc effects, ACL bypass |
| Supply chain | Model/package provenance, tool description review |
| Availability/cost | Long prompts, loops, parallel flood |
| Safety/misuse | Harmful content policies, jailbreak resilience |
| Bias/fairness | Differential outcomes across groups |

## Tools to explore (open source, verify maintenance status)
- **garak** (NVIDIA): LLM vulnerability scanner
- **PyRIT** (Microsoft): risk identification toolkit
- **promptfoo**: eval and red-team test harness
- **Adversarial Robustness Toolbox (ART)**: classical ML attacks/defenses
- **CleverHans / Foolbox**: adversarial example libraries
- **Counterfit**, **DeepTeam**, **Giskard**, **LLM Guard**, **Inspect (UK AISI)**

## Metrics
Attack success rate, number of bypassed controls, time to detect, time to remediate, coverage of OWASP items.

## Report template
- Executive summary
- Scope and method
- Findings (ID, title, severity, OWASP/ATLAS mapping, steps, evidence, impact, fix)
- Positive observations
- Remediation roadmap
- Appendix: test prompts, tooling

## Safe practice lab ideas
- Gandalf-style prompt injection games (Lakera), prompt-injection CTFs
- Deliberately vulnerable LLM apps (search GitHub for "vulnerable LLM app" labs, run in isolated environment)
- Build a small RAG app and attack it yourself
