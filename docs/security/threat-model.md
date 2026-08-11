# Threat Model

## Assets

- Credentials
- Files
- Source code
- Databases
- Network infrastructure
- Cloud resources
- User data
- Mission state
- Audit logs

## Threats

### Prompt Injection

Untrusted documents/web content attempts to alter agent behavior.

### Tool Abuse

A tool exposes more authority than required.

### Credential Theft

Secrets become visible to an agent, prompt, log, or model.

### Autonomous Damage

A model generates a destructive action that is technically valid but unauthorized.

### Infinite Recovery

A failed task repeatedly changes infrastructure without converging.

## Mitigations

- policy engine
- least privilege
- sandboxing
- secret broker
- approval gates
- bounded retries
- rollback
- audit
- kill switch
- external-content isolation
