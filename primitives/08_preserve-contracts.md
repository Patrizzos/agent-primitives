# Preserve API Contracts Primitive

Maintain backwards compatibility and public interfaces when modifying underlying implementation details.

## Rules

1. **Treat Contracts as Immutable:** Do not alter public function signatures, exported interface types, API route paths, request/response payload schemas, or database column definitions unless explicitly requested.
2. **Isolate Internal Refactoring:** Internal performance improvements or structural cleanups must not leak changes into public interfaces.
3. **Add, Do Not Modify:** If new data or behavior is required for an interface, add optional fields or secondary parameters rather than changing existing required parameters.
4. **Deprecate Before Removing:** If a contract change is strictly necessary, signal deprecation clearly and support the existing contract alongside the new one where possible.

Core principle:

> Refactor implementation details freely, but protect public interfaces.