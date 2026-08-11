# Project Governance

## Project Philosophy

GOD AI OS is intended to be an open-source, community-driven architecture.

## Maintainers

Maintainers are responsible for architecture decisions, security response, release management, compatibility policy, and project direction.

## Architecture Decisions

Significant design decisions should be recorded as ADRs under `docs/adr/`.

## Security

Security-related changes require additional review. No contributor should weaken authorization, sandboxing, auditability, or emergency-stop mechanisms without a documented architectural reason.

## Compatibility

Public APIs and capability schemas should use semantic versioning where practical.

## Decision Rule

When choosing between more autonomy, more safety, and more complexity, the default should be:

> Preserve safety and observability first; increase autonomy through explicit, testable capabilities.
