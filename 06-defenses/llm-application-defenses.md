# Defending LLM Applications

## Layered architecture
```
User -> [Input controls] -> [Prompt builder] -> LLM -> [Output controls] -> [Policy/Action gate] -> Tools/Users
              |                   |                          |                       |
          authN, rate limit   separate trusted/untrusted   schema, DLP        authZ outside model, human approval
```

## 1. Input controls
- Authenticate users; apply per-user quotas.
- Length and format limits.
- Detect injection patterns with classifiers (helpful, bypassable).
- Scan uploads (malware, hidden text, metadata).
- Normalize encodings/unicode; handle multimodal inputs (text in images).

## 2. Prompt design
- Clear role and boundaries; instruct to treat retrieved content as data.
- Delimit untrusted content, and label its source.
- **No secrets** in prompts.
- Version-control prompts; review changes like code.

## 3. Output controls
- Validate against strict JSON/schemas.
- Encode outputs for destination (HTML escape, parameterized SQL).
- PII/secret scanning (DLP) before display.
- Block or flag harmful categories.
- Cite sources; show uncertainty.

## 4. Action controls (most important)
- Authorization enforced by deterministic code, not the model.
- Per-tool allow-lists and argument validation.
- Human-in-the-loop for irreversible/high-impact actions (payments, deletes, external emails).
- Use user's own delegated permissions.
- Rate limit and budget actions.

## 5. Guardrail tools (examples; evaluate for your needs)
NVIDIA NeMo Guardrails, Llama Guard / Prompt Guard (Meta), Guardrails AI, LLM Guard, cloud-provider content filters (Azure AI Content Safety, Bedrock Guardrails, Google model armor-style services). No tool is complete; combine with architecture controls.

## 6. Design patterns that reduce injection impact
- **Dual-LLM / quarantined LLM**: an unprivileged model handles untrusted text and cannot call tools.
- **Plan-then-execute**: fix the plan before reading untrusted data.
- **Capability-limited tools**: read-only by default.
- **Data/instruction separation** via structured interfaces.
- **Rule of Two (guidance idea)**: avoid combining untrusted input, access to sensitive data, and ability to take external actions in one agent session without human approval.

## 7. Monitoring and logging
- Log prompts, retrieved chunks, tool calls, outputs (mind privacy and retention).
- Alert on: anomalous token use, repeated refusals, injection signatures, tool-call spikes.
- Trace IDs across agent steps.

## 8. Incident readiness
See `08-templates/ai-incident-response-playbook.md`.
