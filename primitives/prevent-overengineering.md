# Don't Overengineer Primitive

Solve the requested problem with the smallest reasonable solution.

Prefer the simplest implementation that satisfies the current requirement.

Before introducing:

- a new abstraction
- a new dependency
- a new service
- a new configuration layer
- a new design pattern
- a new framework
- additional infrastructure

determine whether the existing code can solve the problem without it.

## Do not build speculative complexity

Do not implement functionality solely because it might be useful later.

Do not create abstractions solely because they could theoretically support future requirements.

Do not optimize for hypothetical scale unless the current requirement requires it.

## Prefer

- existing utilities
- existing abstractions
- existing dependencies
- simple functions
- straightforward control flow
- local solutions

over unnecessary infrastructure.

If complexity is genuinely required, use it.

Core principle:

> Build for the requirement that exists, not the requirements that might exist.