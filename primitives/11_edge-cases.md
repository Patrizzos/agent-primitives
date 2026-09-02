# Edge Case Hardening Primitive

Explicitly identify and handle boundary conditions and unexpected states before completing any task.

## Check Boundary Conditions

Before finalizing logic, verify behavior against:
1. **Empty States:** Empty arrays, empty strings, zero values, missing properties, uninitialized objects.
2. **Absence of Value:** `null`, `undefined`, missing keys, unassigned parameters.
3. **Limits & Extremes:** Max integer values, long text strings, concurrency, boundary index values.
4. **Failures & Timeouts:** Network timeouts, unreachable services, rate limits, non-JSON responses.
5. **Format Variations:** Unexpected casing, whitespace padding, unicode characters, trailing slashes.

## Implementation Standard

- Handle edge conditions explicitly at execution boundaries.
- Provide sensible defaults or early returns rather than allowing runtime errors.
- Include focused tests for identified edge cases.

Core principle:

> Code is only complete when boundary conditions and error states are handled.