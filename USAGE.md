# Using Agent Primitives

Agent primitives are standalone behavioral instructions.

A primitive can be used in several ways depending on the AI coding
environment.

## 1. Persistent instructions

Add the primitive's contents to the instruction file used by your agent.

Examples:

- AGENTS.md
- CLAUDE.md
- project rules
- system instructions

Best for behavior you want applied consistently.

## 2. Skills

Use the primitive as the body of a skill when your agent supports
skill-based instructions.

Best for behaviors that should be available as reusable capabilities.

## 3. Hooks

Wrap the primitive in the appropriate hook mechanism for your agent.

A hook can invoke the primitive at a specific lifecycle event, such as
before an action, after an action, or before the agent finishes.

Best for behaviors that should be enforced or automatically checked.

## Combining primitives

Primitives are intentionally composable.

For example:

consistency
+ minimal-diff
+ verify-before-claim

creates a lightweight development policy without requiring a framework,
package, or additional runtime dependency.

## Choosing a primitive

Use the smallest number of primitives necessary.

Do not combine primitives simply because they exist.

Each primitive should solve one identifiable behavioral problem.

## Important

The `.md` file is the behavioral specification.

It is not itself a universal hook implementation.

Different agents may require different mechanisms to inject or enforce
the instruction.

The primitive remains portable because its behavior is independent of
that mechanism.