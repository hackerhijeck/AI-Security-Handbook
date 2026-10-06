# Data and Model Security

## Training data
- Provenance and licensing records
- Access control and encryption
- Integrity checks (hashes), versioning
- Poisoning detection: outlier detection, label audits, holdout canaries
- Remove or mask PII; document legal basis

## Model artifacts
- Store in secured registry with signing and access logs
- Verify hash/signature before load
- Prefer **safetensors** over pickle; never load untrusted pickle files
- Scan models for malicious code and backdoors
- Separate dev, staging, production

## AI-BOM (AI Bill of Materials)
Track: models (name, version, source, license), datasets, libraries, prompts, tools, vendors. Formats such as CycloneDX ML-BOM or SPDX AI profile can help.

## Model theft and extraction
Rate limits, anomaly detection on queries, watermarking, restrict logits/probabilities, authenticate API clients, legal terms.

## Privacy-enhancing techniques
Differential privacy, federated learning, secure enclaves/confidential computing, synthetic data (validate quality and leakage).

## Fine-tuning safety
Review fine-tuning data; test safety after fine-tuning (safety can regress); restrict who can fine-tune.

## Infrastructure
GPU cluster isolation, secrets management, network segmentation, patching of inference servers, container hardening, cost monitoring.

## Model lifecycle
Develop -> validate -> approve -> deploy -> monitor -> retrain/update -> retire. Document each gate; keep rollback ability.
