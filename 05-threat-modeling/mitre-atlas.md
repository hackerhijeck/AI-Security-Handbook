# MITRE ATLAS

**ATLAS** (Adversarial Threat Landscape for AI Systems) is a knowledge base of adversary **tactics and techniques** against AI systems, modeled on MITRE ATT&CK, with case studies from real incidents.

## Tactics (high level, verify current list on atlas.mitre.org)
Reconnaissance, Resource Development, Initial Access, AI Model Access, Execution, Persistence, Privilege Escalation, Defense Evasion, Credential Access, Discovery, Collection, AI Attack Staging, Command and Control, Exfiltration, Impact.

## Example technique families
- Prompt injection (direct/indirect)
- LLM jailbreak
- Poison training data
- Backdoor ML model
- Craft adversarial data
- Exfiltration via AI inference API
- Model extraction
- Evade ML model
- Publish poisoned datasets/models

## How to use ATLAS
1. Take your threat model.
2. For each attack path, find the matching ATLAS technique ID.
3. Check listed mitigations and case studies.
4. Build detections and test cases per technique.
5. Report findings using ATLAS IDs for shared language.

## Related frameworks
- **MITRE ATT&CK**: traditional adversary behavior (use for infrastructure).
- **NIST AI 100-2**: adversarial ML taxonomy.
- **Google SAIF**: Secure AI Framework (six core elements).
- **CSA AI Controls Matrix / MAESTRO**.
