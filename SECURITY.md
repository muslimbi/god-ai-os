# Security Model

Security is a core architectural requirement, not an optional feature.

## Threat Model

Potential threats include prompt injection, malicious tools, compromised connectors, credential theft, excessive agent permissions, destructive autonomous actions, data exfiltration, tool-chain attacks, model hallucination, infinite execution loops, and supply-chain compromise.

## Security Principles

### Least Privilege

Agents receive only the capabilities required for a mission.

### Capability-Based Authorization

Access is granted to capabilities, not unrestricted shell authority.

### Human Approval

High-risk actions require explicit approval.

### Secret Isolation

Secrets must never be placed directly into prompts.

### Sandboxing

Generated or untrusted code should execute in an isolated environment.

### Auditability

Every consequential action must be auditable.

### Bounded Autonomy

Every mission has limits for runtime, token usage, cost, tool calls, CPU, memory, and network access.

## Risk Classes

### Low

Examples: read files, search documentation, create temporary files.

### Medium

Examples: install packages, start containers, modify development environments.

### High

Examples: modify production firewall, deploy production services, change routing, rotate credentials.

### Critical

Examples: delete production database, financial transaction, irreversible destructive operation.

Critical actions require explicit human authorization.

## Kill Switch

The emergency stop must exist outside the LLM control path.

```text
KILL SWITCH
   ├── stop agents
   ├── stop workflows
   ├── revoke capabilities
   └── block new executions
```

## Prompt Injection Defense

External content must be treated as untrusted data. The system must distinguish system policy, user intent, agent plan, tool data, and external content. Tool output must not automatically gain authority to modify policy or permissions.

## Credential Flow

```text
Agent
 ↓
Capability
 ↓
Credential Broker
 ↓
Secret Store
 ↓
External Service
```

Agents should receive scoped, short-lived credentials where possible.

## Security Reporting

Security vulnerabilities should be reported privately to the project maintainers until a coordinated disclosure decision is made.
