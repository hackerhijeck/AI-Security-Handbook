# AI Incident Response Playbook

## Incident types
Prompt-injection exploitation, data leakage via model, poisoned data/model discovered, agent took unauthorized action, model theft, harmful output event, cost/DoS abuse, vendor model compromise.

## Phases
1. **Detect**: alerts, user reports, anomaly monitoring.
2. **Triage**: severity, scope, affected data and users, legal triggers.
3. **Contain**: disable tool/agent, revoke tokens, switch to safe mode, block attacker, pause ingestion, roll back model/prompt/memory.
4. **Eradicate**: remove poisoned data, patch prompts/controls, rotate secrets, fix vulnerable tools.
5. **Recover**: staged re-enable with extra monitoring.
6. **Notify**: regulators and affected parties as required (e.g., GDPR 72h; EU AI Act serious incident reporting for high-risk; India CERT-In 6h for specified incidents; DPDP breach notification). Confirm timelines with legal.
7. **Learn**: post-incident review, update tests/controls/risk register.

## Evidence to preserve
Prompts, retrieved context, tool-call traces, model/prompt versions, logs, timeline.

## Roles
Incident commander, security analyst, AI/ML engineer, legal/privacy, communications, business owner.

## Kill-switch checklist
- [ ] Can disable agent tools within minutes
- [ ] Can revoke agent credentials centrally
- [ ] Can purge memory/vector entries
- [ ] Can roll back to previous model/prompt version
