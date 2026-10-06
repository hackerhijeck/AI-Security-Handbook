# OWASP Machine Learning Security Top 10

Covers classic ML (not only LLMs). Naming may differ slightly between versions; verify on the official site.

| ID | Risk | Summary | Key defenses |
|---|---|---|---|
| ML01 | Input Manipulation | Adversarial examples fool the model at inference | Adversarial training, input preprocessing, robustness testing |
| ML02 | Data Poisoning | Training data tampered with | Data validation, provenance, access control |
| ML03 | Model Inversion | Reconstruct training inputs from outputs | Limit output detail, differential privacy, rate limits |
| ML04 | Membership Inference | Determine whether a record was in training data | Regularization, differential privacy, reduce overfitting |
| ML05 | Model Theft | Clone/steal a model | API throttling, watermarking, access control, encryption of weights |
| ML06 | AI Supply Chain Attacks | Malicious models, datasets, libraries | Verify sources, hashes, SBOM/AI-BOM, safe formats |
| ML07 | Transfer Learning Attack | Malicious pre-trained base carries backdoors | Vet base models, fine-tune carefully, test for backdoors |
| ML08 | Model Skewing | Feedback loops shift model behavior | Feedback validation, monitoring, retraining controls |
| ML09 | Output Integrity Attack | Model outputs altered between model and consumer | Integrity checks, signing, secure channels |
| ML10 | Model Poisoning | Direct tampering with model weights/params | Access control, integrity monitoring, signed artifacts |

## Study tip
Know one real-world style example for each (spam filter evasion, face-recognition adversarial patches, API-based model cloning, etc.).
