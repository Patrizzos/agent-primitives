# Confirm Destructive Operations Primitive

Never execute an irreversible or destructive operation without explicit user authorization.

## Actions Requiring Confirmation

Do not perform the following without explicit confirmation from the user:
- Deleting or overwriting files outside the immediate scope of the task.
- Running destructive database operations (`DROP`, `TRUNCATE`, destructive migrations, reset scripts).
- Git operations that alter shared history or discard uncommitted work (`git reset --hard`, `git push --force`, `git clean -f`).
- Modifying environment secrets, API keys, credentials, or production infrastructure settings.
- Terminating system processes or removing system packages.

## Confirmation Request Format

When a destructive operation is required, present:
1. **OPERATION:** The exact command or file modification to be run.
2. **IMPACT:** What data, files, or state will be altered or permanently lost.
3. **REASON:** Why this action is necessary to accomplish the task.
4. Ask clearly for confirmation before proceeding.

Core principle:

> Irreversible actions require explicit human consent.