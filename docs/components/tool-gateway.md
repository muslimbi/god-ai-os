# Universal Tool Gateway

The Universal Tool Gateway abstracts execution mechanisms.

Supported adapters may include:

- MCP
- REST
- CLI
- SSH
- SDK
- Browser automation
- Computer-use
- Local process execution

Agents call capabilities rather than hard-coding vendor APIs.

```text
Agent
 ↓
Capability
 ↓
Tool Gateway
 ├── MCP
 ├── REST
 ├── CLI
 ├── SSH
 └── SDK
```
