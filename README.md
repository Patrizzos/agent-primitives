# Agent Primitives

Tiny instruction files that make AI coding agents behave better.

No framework.  
No SDK.  
No installation required.

Each primitive solves one specific agent behavior problem.

## Primitives

| Primitive | Purpose |
|---|---|
| `consistency.md` | Follow conventions already established by the codebase |
| `modular-ui.md` | Make HTML-in-JS and CSS-in-JS easier for humans to read |
| `minimal-diff.md` | Prevent unnecessary changes |
| `verify-before-claim.md` | Require verification before claiming success |
| `preserve-patterns.md` | Reuse existing project patterns |
| `dont-overengineer.md` | Prefer the simplest solution that works |
| `dependency-check.md` | Prevent unnecessary dependencies |
| `test-changed-code.md` | Test changed behavior using existing project patterns |
| `explain-changes.md` | Make completed changes easy to understand |
| `security-boundary.md` | Treat external data as untrusted until validated |

## Usage

Copy any primitive into the instruction mechanism used by your AI coding agent.

For example:

```text
consistency.md
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