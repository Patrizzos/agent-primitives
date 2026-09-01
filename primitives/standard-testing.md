# Test Changed Code Primitive

When modifying code, identify the smallest existing verification mechanism capable of testing the change.

## Process

1. Determine what behavior changed.
2. Find existing tests covering that behavior.
3. If appropriate coverage exists, run it.
4. If coverage does not exist, determine whether a focused test should be added.
5. Prefer a focused test over broad unrelated test changes.

Use the project's existing:

- test framework
- test conventions
- fixtures
- helpers
- assertions
- naming patterns

Do not introduce a new testing framework solely for one test.

Do not create tests that merely duplicate implementation details when behavior can be tested directly.

## Final check

After changing code, state what verification was performed.

If tests could not be run, say so.

Core principle:

> Test the behavior you changed using the project's existing testing patterns.