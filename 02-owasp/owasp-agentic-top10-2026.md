# OWASP Top 10 for Agentic Applications (2026)

Published by the OWASP GenAI Security Project in December 2025 (IDs ASI01 to ASI10). It targets **autonomous agents**: systems that plan, hold memory, call tools and act with delegated authority.

Two guiding ideas:
- **Least agency**: give agents only the minimum autonomy required for a bounded task.
- **Strong observability**: you must see what agents plan, decide and do.

> Names below follow the published list; confirm wording on the official OWASP site.

---
## ASI01: Agent Goal Hijack
Attacker content (prompt injection, poisoned documents, emails, calendar invites) redirects the agent's objectives.
**Example:** a calendar invite instructs the agent to exfiltrate files.
**Mitigate:** treat all natural-language input as untrusted; lock goals/system prompt; validate intent before actions; human approval for goal changes; monitor behavior drift.

## ASI02: Tool Misuse and Exploitation
Agent uses legitimate tools in unsafe ways (over-broad parameters, destructive commands, chained tool abuse).
**Mitigate:** narrow tool scopes; argument validation and allow-lists; policy enforcement layer; sandboxing; rate limits; dry-run modes.

## ASI03: Identity and Privilege Abuse
Agents inherit or share credentials; confused-deputy problems; privilege escalation across agents or tools.
**Mitigate:** distinct identity per agent; short-lived, scoped tokens; user-delegated (on-behalf-of) auth; no shared admin keys; re-authorize per action; audit trails.

## ASI04: Agentic Supply Chain Vulnerabilities
Compromised tools, plugins, MCP servers, prompts, models, or other agents loaded at runtime.
**Mitigate:** vetted registries; signed and pinned components; allow-lists; sandbox third-party tools; AI-BOM; monitor for tool description changes ("rug pull").

## ASI05: Unexpected Code Execution (RCE)
Agent-generated or agent-triggered code runs outside intended boundaries (code interpreters, shell tools, CI).
**Mitigate:** isolated sandboxes (containers/microVMs), no network or limited egress, read-only filesystems, resource limits, approval for execution, static checks.

## ASI06: Memory and Context Poisoning
Persistent memory, vector stores, or shared context are corrupted so future behavior is skewed.
**Mitigate:** validate what is written to memory; provenance tags; per-user/tenant isolation; expiry and review; ability to roll back or purge memory.

## ASI07: Insecure Inter-Agent Communication
Agent-to-agent messages are spoofed, replayed, or tampered with; weak authentication between agents.
**Mitigate:** mutual authentication, signed/encrypted messages, schemas, trust boundaries between agents, message validation, rate limiting.

## ASI08: Cascading Failures
One fault or compromise propagates across chained agents and systems, amplifying impact.
**Mitigate:** circuit breakers, blast-radius limits, isolation domains, timeouts, step/budget caps, kill switch, staged rollouts, resilience testing.

## ASI09: Human-Agent Trust Exploitation
Humans over-trust confident agents; attackers use agents to socially engineer approvals.
**Mitigate:** clear explanations of proposed actions; show sources and uncertainty; meaningful (not rubber-stamp) approvals; train users; avoid anthropomorphic over-reassurance.

## ASI10: Rogue Agents
Agents deviate from intended behavior, collude, or pursue misaligned or deceptive objectives after governance fails.
**Mitigate:** behavioral baselines and anomaly detection; immutable logs; kill switches; periodic attestation; independent monitoring agents; strict scoping.

---
## Agentic threat-modeling steps
1. List agent goals, tools, data, memory, and other agents.
2. Draw trust boundaries and identities.
3. For each ASI item, ask: can it happen here? what is the blast radius?
4. Add controls: least agency, approvals, sandboxing, observability.
5. Test with red-team scenarios (injected docs, malicious tool, poisoned memory).

## Agent security baseline checklist
- [ ] Each agent has its own identity and scoped, short-lived credentials
- [ ] Tool allow-list; arguments validated outside the model
- [ ] High-impact actions need human approval
- [ ] Code execution sandboxed with restricted egress
- [ ] Memory writes validated, attributable, purgeable
- [ ] Inter-agent messages authenticated
- [ ] Budgets: max steps, tokens, spend, time
- [ ] Full tracing of plans, tool calls, outputs
- [ ] Kill switch tested
