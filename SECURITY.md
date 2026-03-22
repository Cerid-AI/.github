# Security Policy

## Supported Versions

| Repository | Supported |
|-----------|-----------|
| cerid-ai (latest main) | ✅ |
| cerid-trading-agent (latest main) | ✅ |
| cerid-boardroom (latest main) | ✅ |

Older pinned versions are not actively patched. Always run from `main`.

---

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report security issues privately:

1. Go to the affected repository on GitHub.
2. Click **Security** → **Report a vulnerability** (GitHub private advisory).
3. Include: affected component, reproduction steps, potential impact, and any suggested fix.

We will acknowledge receipt within **48 hours** and aim to provide a fix or mitigation within **14 days** depending on severity.

---

## Scope

### In scope
- Authentication bypasses or privilege escalation in the MCP server or API
- Remote code execution via file ingestion or agent workflows
- Data exfiltration from the knowledge base or secrets store
- Dependency vulnerabilities in direct dependencies

### Out of scope
- Issues in third-party services (OpenRouter, Hyperliquid, Polymarket)
- Vulnerabilities requiring physical access to the host machine
- Social engineering attacks

---

## Secrets & Encryption

Cerid AI uses `age` encryption for secrets at rest (`.env.age`). Age keys are stored outside the repo at `~/.config/cerid/age-key.txt`. If you discover a committed secret or key material, report it immediately via the private advisory process above.

---

## Dependency Security

Dependabot is enabled across all repos with weekly grouped updates. Lock files with hashes (`requirements.lock`, `package-lock.json`) are used to ensure reproducible builds. CodeQL analysis runs on every push.
