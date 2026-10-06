# Privacy and Data Protection for AI

## GDPR (EU/UK) key points for AI
- **Lawful basis** for training and use of personal data (consent, legitimate interest, etc.)
- **Purpose limitation** and **data minimization**
- **Transparency**: tell people how AI uses their data
- **Rights**: access, rectification, erasure, objection (hard for trained models; plan for it)
- **Article 22**: restrictions on solely automated decisions with significant effects
- **DPIA** (Data Protection Impact Assessment) for high-risk processing
- **Security of processing** (Art. 32) and breach notification within 72 hours
- International transfers (SCCs, adequacy)

## India: Digital Personal Data Protection Act, 2023 (DPDP)
- Applies to digital personal data processing in India (and some outside processing offering services to people in India)
- Consent-based with limited legitimate uses; notice requirements
- Data fiduciary duties: security safeguards, breach notification, retention limits
- Rights for data principals: access, correction, erasure, grievance redressal
- Special rules for children's data
- Significant Data Fiduciaries have extra duties (e.g., DPIA, audit, DPO)
- Rules are being phased in; **check current commencement dates and rules** on MeitY / official sources.
- India also has CERT-In directions (incident reporting within 6 hours) and sector rules (RBI, SEBI, IRDAI).

## Other regimes to be aware of
- US: no single federal AI law; state laws (e.g., Colorado AI Act, California rules), FTC enforcement, sector rules (HIPAA, GLBA)
- China: generative AI measures, algorithm registration
- Many countries: national AI strategies and sandbox programs

## Privacy risks specific to AI
- Training on personal data without a basis
- Memorization and regurgitation
- Prompts containing PII sent to third-party providers
- Inference of sensitive attributes
- Logs and chat histories retaining personal data
- Embeddings containing personal data

## Privacy controls
- Data inventory and classification
- Anonymization/pseudonymization (know limits)
- PII redaction before prompts and indexing
- Retention and deletion policies for prompts, logs, vector stores
- Vendor DPAs, zero-retention options, region controls
- Differential privacy, federated learning (where appropriate)
- Privacy by design reviews
