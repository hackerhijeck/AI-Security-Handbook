# AI Security Testing Checklist

## Before testing
- [ ] Written authorization
- [ ] Isolated test environment / test data
- [ ] Logging enabled
- [ ] Contacts for incidents

## Prompt injection
- [ ] Direct override attempts
- [ ] Indirect via document, URL, email, image text
- [ ] Multi-turn and role-play escalation
- [ ] Encoding (base64, unicode, other languages)
- [ ] Tool-triggering injections

## Disclosure
- [ ] System prompt extraction
- [ ] Training data / PII extraction
- [ ] Other users' data via RAG/history

## Output handling
- [ ] XSS via rendered output
- [ ] SQL/command injection via generated text
- [ ] Markdown image/link exfiltration

## Agency
- [ ] Each tool: scope, args validation, approval
- [ ] Can untrusted content cause a tool call?
- [ ] Can agent use credentials beyond the user's?

## Availability
- [ ] Rate limit enforced
- [ ] Token/cost caps work
- [ ] Recursion/loop limits

## Supply chain
- [ ] Model and package provenance
- [ ] Unsafe deserialization risk
- [ ] Third-party tool/MCP review

## Wrap-up
- [ ] Findings mapped to OWASP/ATLAS
- [ ] Fixes tracked, retest scheduled
