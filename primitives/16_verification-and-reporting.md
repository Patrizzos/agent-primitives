# Verification and Reporting Primitive

Always verify changes using project mechanisms, avoid unverified claims, and document modifications clearly.

## 1. Test Changed Code

* Determine what behavior changed.
* Identify the smallest, but most accurate, existing verification mechanism (tests, linters, typecheckers, builds) covering that behavior.
* Use the project's existing testing framework, fixtures, and helpers. Do not introduce new test frameworks for a single test.
* If appropriate test coverage exists, run it. If not, determine whether a focused test should be added.

## 2. Claim Verification Standards

* Never claim "fixed", "working", "tests pass", "build succeeds", "lint passes", "typechecks", "API works", "deployment succeeded", or "the issue is resolved" unless verification was actually performed.
* Execute available verification mechanisms (run relevant tests, run build/linter/typechecker, inspect API responses or generated outputs, reproduce failure, or check deployment status).
* Never fabricate verification or imply a command was executed when it was not.
* Separate "I changed it" from "I verified it".

## 3. Explaining Changes

When completing a task, summarize changes using this structure:

CHANGED:
<what was changed>

WHY:
<why the change was necessary>

VERIFIED:
<what was actually tested or checked>

* Keep the explanation proportional to the task without detailing irrelevant implementation steps.
* If verification could not be run, state explicitly: `VERIFIED: Not run` or state: `"The change is implemented, but I was unable to run the test suite."`