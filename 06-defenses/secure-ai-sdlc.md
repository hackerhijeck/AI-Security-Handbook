# Secure AI Development Lifecycle

| Phase | Security activities |
|---|---|
| Plan | Use-case risk screening, regulatory classification, threat model |
| Data | Provenance, consent, quality, poisoning checks |
| Build | Secure coding, dependency scanning, secrets scanning, prompt review |
| Evaluate | Accuracy, robustness, bias, safety, security red team |
| Deploy | Hardened infra, authN/Z, rate limits, guardrails, approvals |
| Operate | Monitoring, drift, abuse detection, incident response |
| Retire | Data deletion, key revocation, documentation retention |

## CI/CD gates for AI
- Static analysis and dependency/model scanning
- Automated prompt-injection and jailbreak regression suite
- Evaluation thresholds (quality, safety, bias) must pass
- Prompt and config changes require review
- Signed artifacts and provenance (SLSA-style)
- Staged rollout with canary and rollback

## Documentation to produce
Model/system card, data sheet, threat model, risk assessment, test reports, user instructions, change log.
