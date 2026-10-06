# AI Security Fundamentals

## 1. Key terms
- **AI**: systems performing tasks that normally need human intelligence.
- **ML**: models that learn patterns from data.
- **LLM**: large language model (text in, text out) predicting next tokens.
- **RAG**: Retrieval-Augmented Generation, where an LLM answers using retrieved documents.
- **Agent**: an LLM-based system that plans, remembers, calls tools and acts autonomously.
- **MCP**: Model Context Protocol, a standard for connecting models/agents to tools and data.
- **Embedding / vector DB**: numeric representation of text used for semantic search.

## 2. Why AI security is different
| Traditional software | AI systems |
|---|---|
| Deterministic logic | Probabilistic outputs |
| Clear code/data separation | Instructions and data share one channel (natural language) |
| Input validation is well understood | Inputs can be ambiguous, adversarial, multimodal |
| Bugs are reproducible | Failures can be intermittent |
| Fixed attack surface | Surface includes data, models, prompts, tools, memory, other agents |

**Core problem:** an LLM cannot reliably distinguish trusted instructions from untrusted content. Prompt injection therefore cannot be fully "patched"; it must be contained through architecture.

## 3. The AI attack surface
```
Training data -> Training pipeline -> Model artifact -> Serving/API
                                                         |
User input -> Prompt assembly (system prompt + context) -> Model -> Output -> Downstream systems
                         ^                                  |
          RAG / vector DB / files / web                     +-> Tools / plugins / MCP / other agents
```
Attackable points: data collection, labeling, training code, model files, dependencies, prompts, retrieval stores, memory, tools, credentials, output consumers, and humans who trust outputs.

## 4. CIA triad for AI
- **Confidentiality**: training-data leakage, system prompt leakage, cross-user data leakage, model theft.
- **Integrity**: poisoning, prompt injection, output manipulation, model tampering, hallucinations treated as truth.
- **Availability**: resource exhaustion, "denial of wallet", model DoS, dependency outages.
- Add: **Safety**, **Fairness**, **Transparency/Accountability**, **Privacy**.

## 5. Categories of AI attacks
1. **Evasion** (inference-time): adversarial inputs, jailbreaks, prompt injection.
2. **Poisoning** (training-time): corrupt data or fine-tuning to implant backdoors or bias.
3. **Privacy attacks**: model inversion, membership inference, training-data extraction.
4. **Model theft / extraction**: cloning via API queries or stealing weights.
5. **Supply chain**: malicious models, packages, datasets, plugins.
6. **Abuse of agency**: tools used to take harmful actions.
7. **Misuse**: using AI to generate malware, phishing, deepfakes, disinformation.

## 6. Security principles to carry everywhere
- Treat **all model input and output as untrusted**.
- **Least privilege** and **least agency** for tools.
- **Defense in depth**: no single guardrail is enough.
- **Human-in-the-loop** for high-impact actions.
- **Log what you need** for forensics (with privacy care).
- **Assume breach**: design so a hijacked model causes limited damage.
- **Secure by design**: threat model before building.

## 7. Shared responsibility
| Role | Typical duties |
|---|---|
| Model provider | Base model safety, API security, documentation |
| Deployer / app owner | Prompting, RAG, tools, access control, monitoring |
| Data owner | Data quality, consent, classification |
| Security team | Threat modeling, testing, detection and response |
| GRC / legal | Policy, risk, regulatory mapping, audits |
| End user | Responsible use, verification of outputs |

## 8. Self-check questions
1. Why can't prompt injection be fully eliminated by filtering?
2. Which components of a RAG app handle untrusted data?
3. What is the difference between evasion and poisoning?
4. Why does adding tools increase risk more than adding a bigger model?
