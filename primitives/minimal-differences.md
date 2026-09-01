# Minimal Diff Primitive

Make the smallest reasonable change that completely solves the requested problem.

Before modifying code, identify the exact files and lines that need to change.

## Rules

Do not:

- rewrite untouched code
- reformat unrelated code
- rename unrelated variables
- reorganize unrelated imports
- refactor surrounding code without a reason
- upgrade dependencies unless required
- introduce abstractions that are unnecessary for the requested change
- fix unrelated problems discovered during the task

Preserve existing code whenever it does not need to change.

If a larger change is genuinely required, make the reason clear.

## Final check

Before returning the result:

1. Review the diff.
2. Identify changes unrelated to the requested task.
3. Revert unnecessary changes.
4. Confirm that the remaining diff is proportional to the task.

Core principle:

> Change what is necessary. Preserve what is not.