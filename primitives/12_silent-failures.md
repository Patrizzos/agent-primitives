# Explicit Error Handling Primitive

Never catch, suppress, or ignore errors without explicit logging or handling.

## Rules

1. **No Swallowing Errors:** Never write empty `catch` blocks (`catch (e) {}`), empty `.catch()` handlers, or suppress error returns.
2. **Contextual Error Logs:** Always log caught exceptions with actionable context (e.g., file name, operation attempted, relevant IDs) before rethrowing or gracefully degrading.
3. **Fail Explicitly on Invariants:** If an operational invariant fails, raise a clear, typed error rather than returning `null` or `false` silently.
4. **Preserve Stack Traces:** When rewrapping errors in custom domain exceptions, preserve the original cause/stack trace.

Core principle:

> An error handled silently is a future bug hidden from engineers.