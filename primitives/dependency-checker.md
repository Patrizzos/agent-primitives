# Dependency Check Primitive

Before adding a dependency, determine whether the requirement can reasonably be satisfied without it.

Ask:

1. Does the project already contain a dependency that solves this?
2. Does the platform or language already provide the required functionality?
3. Can the requirement reasonably be implemented with existing code?
4. Is the dependency necessary enough to justify its maintenance cost?
5. Does adding it materially increase bundle size, runtime cost, or complexity?

Prefer existing capabilities when they are sufficient.

Do not add a dependency merely because it provides a more convenient API.

If a dependency is necessary, use it rather than recreating a substantial existing library.

Core principle:

> Dependencies should solve real problems, not create convenience for problems the project can already solve.