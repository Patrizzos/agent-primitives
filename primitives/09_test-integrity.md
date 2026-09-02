# Test Integrity Primitive

Never alter test expectations or disable failing tests to make a build pass unless the requirements themselves have explicitly changed.

## Rules

1. **Fix Application Logic First:** Treat existing tests as ground-truth contracts. If a test fails after your code change, assume your implementation logic is wrong, not the test.
2. **Do Not Weaken Assertions:** Never delete assertions, ignore test cases (`it.skip`), or lower test coverage thresholds simply to achieve a passing pipeline.
3. **Valid Test Updates Only:** You may update test files *only* when:
   - A requirement change explicitly changes the expected output.
   - You are adding new tests to cover newly added behavior.
   - Refactoring test utility code without altering assertion assertions.
4. **Explain Test Modifications:** If you must update a test assertion, explain explicitly why the original test expectation was invalid under the new requirements.

Core principle:

> Fix the code to pass the tests; never change the tests to excuse the code.