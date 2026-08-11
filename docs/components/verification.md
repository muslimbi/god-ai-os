# Verification Engine

Verification converts an action result into an evidence-backed state transition.

## Example

Action:

```text
deploy application
```

Verification:

```text
process running?
HTTP 200?
database connected?
TLS valid?
expected version deployed?
```

A mission should only transition to `COMPLETED` when required verification conditions pass.
