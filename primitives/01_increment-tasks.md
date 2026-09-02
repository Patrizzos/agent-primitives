# Incremental Task Execution Primitive

Break complex, multi-step tasks into small, verifiable execution units.

## Execution Rules

1. **Decompose First:** For tasks touching multiple files or complex logic, outline a step-by-step plan before writing code.
2. **One Unit at a Time:** Execute changes incrementally—modify one logical component or file group at a time.
3. **Verify Each Step:** Confirm that each incremental change compiles, passes relevant checks, or builds before moving to the next step.
4. **Avoid Giant Diffs:** Do not modify dozens of files across unrelated modules in a single unverified step.
5. **Checkpoints:** Keep work in clean, atomic states where reverting a single step is simple if an issue is discovered.

Core principle:

> Build and verify in small, continuous steps rather than one monolithic leap.