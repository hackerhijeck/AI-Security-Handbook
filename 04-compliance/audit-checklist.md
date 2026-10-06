# AI Compliance and Security Audit Checklist

## Governance
- [ ] AI policy approved and communicated
- [ ] Roles: AI owner, risk owner, DPO, security lead named
- [ ] AI governance committee meets regularly
- [ ] AI literacy training delivered

## Inventory and classification
- [ ] All AI systems (incl. third-party and shadow AI) listed
- [ ] Risk tier assigned (e.g., EU AI Act)
- [ ] Data sources and legal basis recorded
- [ ] Provider/deployer role identified

## Risk and impact
- [ ] Risk assessment per system
- [ ] DPIA / AI impact assessment completed where needed
- [ ] Residual risk accepted by risk owner

## Security
- [ ] Threat model done (OWASP LLM, Agentic, ATLAS)
- [ ] Access control and secrets management
- [ ] Prompt injection and output handling tests passed
- [ ] RAG access control verified
- [ ] Model and dataset integrity controls
- [ ] Supply chain inventory (AI-BOM)
- [ ] Logging and monitoring active

## Data and privacy
- [ ] Data minimization and retention rules
- [ ] PII handling for prompts/logs/embeddings
- [ ] Vendor DPAs and data residency

## Oversight and transparency
- [ ] Human oversight defined and effective
- [ ] Users informed they interact with AI where required
- [ ] AI-generated content labeled where required

## Operations
- [ ] Incident response playbook for AI
- [ ] Change management for models/prompts
- [ ] Monitoring for drift and misuse
- [ ] Decommissioning process

## Third parties
- [ ] Vendor security and AI due diligence
- [ ] Contract clauses (data use, training, incident notice, audit rights)
