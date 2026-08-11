# Contributing to GOD AI OS

Thank you for contributing.

## Development Principles

1. Prefer modular components.
2. Keep the core model-provider agnostic.
3. Never bypass the policy layer for convenience.
4. Every new capability should define verification.
5. Every connector should define authentication and permission requirements.
6. Avoid vendor-specific logic in the core.
7. Add tests for failure cases, not only happy paths.
8. Document security implications.

## Adding a Capability

A capability should define name, version, description, inputs, outputs, required permissions, risk level, execution adapter, verification adapter, and tests.

## Pull Requests

A PR should explain what changed, why it is needed, security impact, backward compatibility, tests added, and documentation updated.

## Commit Style

```text
feat: add capability registry
fix: prevent mission retry loop
docs: update execution architecture
security: restrict credential scope
test: add verification failure cases
```

## Code Review

Reviewers should pay special attention to privilege escalation, prompt injection, secret exposure, unsafe shell execution, missing verification, unbounded retries, missing audit events, and destructive defaults.
