# Example Mission

## User Request

> Deploy a web application, verify it, and provide a report.

## Plan

1. Inspect environment
2. Check prerequisites
3. Retrieve source
4. Install dependencies
5. Run tests
6. Build deployment artifact
7. Deploy
8. Health-check
9. Verify
10. Report

## Failure

If health-check fails:

```text
health-check failed
 ↓
collect logs
 ↓
diagnose
 ↓
attempt bounded recovery
 ↓
verify again
```

If recovery fails, pause and escalate rather than looping indefinitely.
