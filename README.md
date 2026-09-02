# Agent Primitives

16 tiny instruction files that make AI coding agents behave better.

No framework.  
No SDK.  
No installation required.

Each primitive solves one specific agent behavior problem.

## Primitive Index

### Workflow & Scope
| Primitive | Purpose |
|---|---|
| `01_incremental-tasks.md` | Break complex, multi-step tasks into small, verifiable execution units. |
| `02_minimal-scope.md` | Prevent unnecessary changes, avoid overengineering, and check dependencies. |
| `03_fail-fast.md` | Recognize repetitive failures quickly and pause execution before entering retry loops. |

### Quality & Safety
| Primitive | Purpose |
|---|---|
| `04_root-cause.md` | Identify and address the true root cause of a failure before writing or modifying code. |
| `05_confirm-destruction.md` | Never execute an irreversible or destructive operation without explicit authorization. |
| `06_enforce-security.md` | Treat data crossing application boundaries as untrusted until validated. |

### Code Integrity
| Primitive | Purpose |
|---|---|
| `07_codebase-alignment.md` | Follow conventions established by the codebase and preserve existing architectural patterns. |
| `08_preserve-contracts.md` | Maintain backwards compatibility and public interfaces when modifying underlying implementations. |
| `09_test-integrity.md` | Never alter test expectations or disable failing tests to make a build pass. |
| `10_read-before-write.md` | Always inspect the current on-disk state of a file immediately before modifying it. |

### Robustness
| Primitive | Purpose |
|---|---|
| `11_edge-cases.md` | Explicitly identify and handle boundary conditions and unexpected states. |
| `12_silent-failures.md` | Never catch, suppress, or ignore errors without explicit logging or handling. |
| `13_config-isolation.md` | Isolate all environment-specific values, ports, domains, and credentials into configuration. |
| `14_database-efficiency.md` | Avoid performance anti-patterns and optimize data access when interacting with database stores. |

### UI & Formatting
| Primitive | Purpose |
|---|---|
| `15_in-js-readability.md` | Make HTML-in-JS and CSS-in-JS easier for humans to read. |
| `16_verification-and-reporting.md` | Require verification before claiming success, test changed behavior, and format change explanations. |

## Usage

Copy any primitive into the instruction mechanism used by your AI coding agent.

For example:

```text
verification-and-reporting.md
```

or combine several:

```text
consistency.md
minimal-diff.md
verify-before-claim.md
```

Primitives are intentionally standalone and composable.

## Philosophy

Each primitive should:

- solve one problem
- be understandable by a human
- work without dependencies
- avoid prescribing architecture
- avoid unnecessary complexity
- be useful when copied into an agent's instructions

The goal is not to create another agent framework.

The goal is to create a collection of tiny behavioral constraints that make agents easier to work with.

## Contributing

Good primitives are:

**Small + specific + measurable + composable.**

If a primitive needs a large explanation to describe what it does, it probably needs to be simplified.