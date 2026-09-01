# Preserve Patterns Primitive

When extending existing functionality, first determine how the repository already solves the same type of problem.

Prefer extending an existing pattern over introducing a parallel pattern.

## Before adding a new mechanism

Look for existing approaches to:

- state management
- error handling
- API requests
- authentication
- validation
- data fetching
- persistence
- logging
- configuration
- component structure
- testing

If an established mechanism already exists, use it unless there is a concrete reason not to.

## Avoid parallel systems

Do not unnecessarily introduce:

- another API client
- another state-management approach
- another validation strategy
- another error-handling pattern
- another configuration mechanism
- another component convention
- another utility for an existing operation

## Exceptions

A new pattern may be appropriate when:

- the existing pattern cannot satisfy the requirement
- the existing pattern is explicitly being replaced
- the new context genuinely requires different behavior

When introducing a new pattern, make the reason explicit.

Core principle:

> One problem should not accumulate multiple solutions without a reason.