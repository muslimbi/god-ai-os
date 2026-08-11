# Capability Registry

The Capability Registry is the contract layer between agents and tools.

## Example

```yaml
name: filesystem.create_file
version: 1.0.0
risk: low

inputs:
  path:
    type: string
  content:
    type: string

permissions:
  - filesystem.write

verification:
  - file_exists
  - checksum_matches
```

The registry should support discovery, versioning, policy evaluation, and verification metadata.
