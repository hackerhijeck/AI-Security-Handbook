# AI Compliance Landscape (Overview)

AI compliance is a mix of **laws**, **standards**, and **frameworks**.

| Type | Examples | Binding? |
|---|---|---|
| Law/regulation | EU AI Act, GDPR, India DPDP Act 2023, sector rules (health, finance), state laws in US | Yes |
| Management standard | ISO/IEC 42001 | Voluntary, certifiable |
| Risk framework | NIST AI RMF, ISO/IEC 23894 | Voluntary |
| Security guidance | OWASP, MITRE ATLAS, Google SAIF, CSA AI Controls Matrix | Voluntary |
| Security baseline | ISO/IEC 27001, SOC 2 | Often contractually required |

## Compliance workflow
1. Build an **AI inventory** (system, purpose, data, model, vendor, users, geography).
2. Determine **applicable laws** per system and location.
3. **Classify risk** (e.g., EU AI Act tier).
4. Determine your **role** (provider, deployer, importer, distributor).
5. **Map controls** (see `control-mapping.md`).
6. **Document** (technical documentation, DPIAs, risk assessments).
7. **Test and monitor.**
8. **Audit and improve.**

## Evidence auditors usually ask for
- AI policy and governance charter
- AI inventory and risk classification
- Risk assessments and treatment plans
- Data lineage, consent/legal basis, DPIAs
- Test and evaluation reports (security, bias, robustness)
- Human oversight procedures
- Incident logs and post-incident reviews
- Vendor due diligence records
- Training records (AI literacy)
