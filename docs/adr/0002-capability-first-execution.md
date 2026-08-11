# ADR 0002: Capability-First Execution

## Status

Accepted

## Decision

Agents will reason over capability contracts instead of vendor-specific tools.

## Rationale

This allows the same high-level task to use different implementations.

Example:

```text
network.configure_vlan
   ├── MikroTik adapter
   ├── Cisco adapter
   ├── SSH adapter
   └── REST adapter
```

This reduces coupling and improves portability.
