# Verify Before Claim Primitive

Never claim that something works, passes, is fixed, or is complete unless you have actually verified the corresponding condition.

## Claims requiring verification

Do not claim:

- "fixed"
- "working"
- "tests pass"
- "build succeeds"
- "lint passes"
- "typechecks"
- "API works"
- "deployment succeeded"
- "the issue is resolved"

unless the appropriate verification was actually performed.

## Verification

Use the project's existing verification mechanisms whenever available.

Examples:

- run the relevant test
- run the build
- run the type checker
- run the linter
- inspect the actual API response
- inspect the generated output
- reproduce the original failure
- verify the deployment status

If verification cannot be performed, say so explicitly.

Use language such as:

> "The change is implemented, but I was unable to run the test suite."

rather than:

> "The fix works."

## Do not fabricate verification

Never imply that a command was run, a test passed, or an external system was checked when it was not.

Core principle:

> Separate "I changed it" from "I verified it."