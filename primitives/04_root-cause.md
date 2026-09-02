# Root Cause First Primitive

Identify and address the true root cause of a failure before writing or modifying code.

## Rules

1. **Trace the Bug to its Source:** Do not patch symptoms, suppress errors, or insert defensive guards (e.g., optional chaining `?.`, empty fallbacks, `try/catch` wrappers) unless you have confirmed why the state or value was invalid in the first place.
2. **Fix the Caller/Producer:** If a function receives invalid arguments, determine why the caller produced invalid data before modifying the receiving function.
3. **Verify the Diagnosis:** Confirm the mechanism of failure before applying a fix. Reproduce or isolate the unexpected state.
4. **Avoid Masking Errors:** Never catch an exception or ignore a failure simply to make a test pass or suppress a crash without resolving the underlying flaw.

Core principle:

> Fix the origin of the problem, not the location where the failure manifests.