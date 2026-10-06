# AI Risk Management

## 1. What is AI risk?
**Risk = Likelihood x Impact**, applied to harms across: security, privacy, safety, fairness/bias, reliability, legal/compliance, reputation, and financial loss.

## 2. Types of AI risk
| Category | Examples |
|---|---|
| Security | Prompt injection, poisoning, model theft |
| Privacy | PII leakage, unlawful training data, inference attacks |
| Safety | Harmful advice, physical-world failures |
| Fairness | Discriminatory hiring or credit decisions |
| Reliability | Hallucinations, drift, outages |
| Legal/Compliance | EU AI Act breach, IP/copyright issues |
| Third-party | Vendor model change, data retention by provider |
| Societal/Ethical | Misinformation, deepfakes, over-reliance |

## 3. Risk management lifecycle
1. **Establish context**: business goals, stakeholders, risk appetite.
2. **Inventory**: list all AI systems (including shadow AI).
3. **Identify risks**: threat modeling, impact assessment.
4. **Analyze/score**: likelihood and impact.
5. **Evaluate**: compare to risk appetite.
6. **Treat**: mitigate, transfer, avoid, accept.
7. **Monitor and review**: metrics, incidents, drift, audits.
8. **Communicate**: dashboards, reports to leadership.

## 4. Simple 5x5 scoring
| Score | Likelihood | Impact |
|---|---|---|
| 1 | Rare | Negligible |
| 2 | Unlikely | Minor |
| 3 | Possible | Moderate |
| 4 | Likely | Major |
| 5 | Almost certain | Severe |

Rating: 1-4 Low, 5-9 Medium, 10-16 High, 17-25 Critical.

## 5. Risk treatment options
- **Mitigate**: add controls (guardrails, approvals, monitoring).
- **Avoid**: do not deploy the use case.
- **Transfer**: contract terms, insurance (does not remove accountability).
- **Accept**: documented, approved by risk owner.

## 6. NIST AI Risk Management Framework (AI RMF 1.0)
Voluntary framework from NIST (Jan 2023). Four functions:

| Function | Purpose | Example activities |
|---|---|---|
| **GOVERN** | Culture, policies, accountability | AI policy, roles, risk appetite, third-party rules |
| **MAP** | Understand context and risks | Use-case scoping, stakeholders, impact assessment |
| **MEASURE** | Analyze and track risk | Testing, metrics, bias/robustness evaluation |
| **MANAGE** | Prioritize and act | Treatment plans, incident response, decommissioning |

**Trustworthy AI characteristics (NIST):** valid and reliable; safe; secure and resilient; accountable and transparent; explainable and interpretable; privacy-enhanced; fair with harmful bias managed.

**Related NIST documents:**
- **NIST AI 600-1**: Generative AI Profile (July 2024), lists GenAI-specific risks and suggested actions.
- **NIST AI 100-2**: Adversarial Machine Learning taxonomy and terminology.
- **NIST SP 800-218A**: secure software development practices for generative AI.

## 7. AI governance structure
| Body/Role | Responsibility |
|---|---|
| Board / executives | Risk appetite, accountability |
| AI governance committee | Policy, approvals for high-risk use cases |
| AI risk owner (per system) | Owns risk decisions |
| Security | Controls, testing, monitoring |
| Legal/privacy | Regulatory and data protection |
| Engineering/data science | Implement controls, documentation |
| Internal audit | Independent assurance |

## 8. Core AI policies to have
- Acceptable use of AI (employees, including GenAI tools)
- AI risk assessment and approval procedure
- Data governance for AI (sources, consent, retention)
- Third-party/vendor AI policy
- Model lifecycle policy (development, validation, change, retirement)
- Incident response for AI
- Transparency and human oversight policy

## 9. Shadow AI
Employees using unapproved AI tools can leak data. Controls: approved tool list, DLP, browser/CASB monitoring, training, easy sanctioned alternatives.

## 10. Key metrics (KRIs/KPIs)
- % AI systems inventoried and risk-assessed
- Number of AI security incidents / near misses
- Red-team findings open vs closed, time to remediate
- Guardrail block rate, false positive rate
- % high-risk systems with human oversight documented
- Model drift and accuracy over time
- Vendor assessments completed
