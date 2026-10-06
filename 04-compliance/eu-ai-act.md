# EU AI Act (Regulation (EU) 2024/1689)

The world's first comprehensive AI law. Risk-based. Applies to providers and deployers placing AI on the EU market or whose output is used in the EU (extra-territorial).

> **Timeline has been amended.** The Digital Omnibus on AI postponed high-risk obligations. Reports state the amending regulation entered into force in July 2026. Verify exact dates on the European Commission site before relying on them.

## Risk tiers
| Tier | Treatment | Examples |
|---|---|---|
| **Unacceptable** | Prohibited (Art. 5) | Social scoring, manipulative AI exploiting vulnerabilities, untargeted facial-image scraping, certain emotion recognition at work/school |
| **High-risk** | Strict obligations | Hiring/HR, education, credit scoring, critical infrastructure, law enforcement, migration, medical device AI |
| **Limited risk (transparency)** | Disclosure duties (Art. 50) | Chatbots, deepfakes, AI-generated content labeling |
| **Minimal risk** | No specific obligations | Spam filters, game AI |
| **GPAI models** | Separate regime (Arts. 51-56) | Foundation models; extra duties if "systemic risk" |

## Key dates (as reported after the Omnibus, verify)
| Date | What |
|---|---|
| 1 Aug 2024 | Act entered into force |
| 2 Feb 2025 | Prohibitions and AI literacy obligations apply |
| 2 Aug 2025 | GPAI obligations and governance rules apply |
| 2 Aug 2026 | Article 50 transparency obligations (some grace/delay for certain watermarking, check) |
| 2 Dec 2027 | High-risk obligations for stand-alone (Annex III) systems (postponed from Aug 2026) |
| 2 Aug 2028 | High-risk obligations for product-embedded (Annex I) systems (postponed from Aug 2027) |

## High-risk provider obligations (summary)
- Risk management system (Art. 9)
- Data and data governance (Art. 10)
- Technical documentation (Art. 11)
- Record-keeping / logging (Art. 12)
- Transparency and instructions for use (Art. 13)
- Human oversight (Art. 14)
- **Accuracy, robustness and cybersecurity (Art. 15)** (the main security article)
- Quality management system (Art. 17)
- Conformity assessment, CE marking, EU database registration
- Post-market monitoring and serious incident reporting

## Deployer obligations (summary)
Use per instructions, assign human oversight, monitor, keep logs, inform affected people, and perform a **Fundamental Rights Impact Assessment** where required (Art. 27).

## GPAI model providers
Technical documentation, information for downstream providers, copyright policy, training-data summary; for systemic-risk models: evaluations, adversarial testing, incident reporting, cybersecurity protection.

## Penalties (maximum, up to)
- Prohibited practices: EUR 35M or 7% of global turnover
- Other obligations: EUR 15M or 3%
- Incorrect info to authorities: EUR 7.5M or 1%

## Security link
Article 15 requires resilience against attacks such as **data poisoning, model poisoning, adversarial examples, model evasion, confidentiality attacks**. Use OWASP and ATLAS to evidence this.

## Practical steps
1. Inventory AI systems; check for prohibited practices now.
2. Classify each (is it Annex III?).
3. Identify your role.
4. Gap-assess against Arts. 9-15 and 17.
5. Start documentation and logging early.
6. Build AI literacy training.
