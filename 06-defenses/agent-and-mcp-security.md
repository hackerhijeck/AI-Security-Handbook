# Agent and MCP Security

## Principle: Least Agency
Only the autonomy, tools and permissions required for the task.

## Identity and access
- Unique identity per agent; no shared credentials
- Short-lived, scoped tokens; OAuth on-behalf-of user
- Re-check authorization for each tool call

## Tools
- Minimal, purpose-built tools rather than general shells
- Validate arguments server-side; allow-lists
- Read-only by default; separate write tools with approval
- Pin tool versions; review tool descriptions (they are prompt content!)

## MCP (Model Context Protocol) specific risks
| Risk | Description | Mitigation |
|---|---|---|
| Malicious/compromised MCP server | Untrusted server supplies harmful tools | Allow-list servers, review code, sandbox |
| Tool poisoning | Hidden instructions in tool descriptions | Inspect descriptions, display to users, hash and pin |
| Rug pull | Tool behavior/description changes after approval | Version pinning, change alerts |
| Tool shadowing | One server's tools override or influence another's | Namespace tools, isolate servers |
| Over-broad token scope | Token grants more than needed | Least-privilege scopes |
| Confused deputy | Server acts with wrong user's authority | Per-user auth, token audience checks |
| Local server RCE | Locally run servers execute commands | Sandbox, run as low-privilege user |
| Data exfiltration | Tools send data to attacker endpoints | Egress controls, DLP |

## Sandboxing code execution
Containers/microVMs, no secrets, read-only mounts, no or allow-listed network, CPU/memory/time limits, ephemeral.

## Human-in-the-loop done right
- Show exact action and parameters
- Highlight risk (data leaving, irreversible)
- Avoid approval fatigue: gate only meaningful actions

## Memory
Validate writes, tag provenance, isolate per user, allow purge/rollback.

## Multi-agent
Authenticate agents to each other, validate messages, limit chain depth, add circuit breakers and a global kill switch.

## Observability
Trace goals, plans, tool calls, results, approvals. Immutable logs. Baseline normal behavior and alert on deviation.
