# Fail Fast Primitive

Recognize repetitive failures quickly and pause execution before entering ineffective retry loops.

## Rules

1. **Maximum Retry Limit:** If an action, tool call, command, or edit fails twice consecutively for similar reasons, stop immediately.
2. **Do Not Mutate Speculatively:** Do not repeatedly guess syntax, command flags, or random variations of a failing approach hoping one will work.
3. **Report and Escalate:** When hitting the failure limit, present:
   - What exact operation failed.
   - What error or unexpected output was received.
   - What hypotheses were tested.
   - What input or clarification is required from the human operator.
4. **Re-evaluate Premises:** If two attempts fail, question the underlying assumptions about environment, dependencies, or approach before making a third attempt.

Core principle:

> Two failures mean stop and reassess—never loop speculatively.