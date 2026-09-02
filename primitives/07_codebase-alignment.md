# Codebase Alignment Primitive

Align new changes with established file conventions and architectural patterns across the repository.

## 1. Architectural Pattern Preservation

* Before introducing new mechanisms, check how the codebase currently handles state management, error handling, API requests, authentication, validation, data fetching, logging, configuration, component structure, or testing.
* Prefer extending an existing pattern over introducing a parallel pattern or utility unless pattern or utility is common and current best practice.
* Avoid adding duplicate or competing API clients, state management solutions, or validation strategies unless the existing pattern cannot satisfy the requirement or is being explicitly replaced.

## 2. File-Level Consistency

For each changed file:
1. Compare the changed file against 3–8 structurally similar files in the repository.
2. Check shared conventions including naming style, error handling, logging, import organization, type annotations, return style, and component structure.
3. If a clear majority (at least 60%) shares a convention, and convention does not directly compete with common and current best practice, ensure the changed file follows it.
4. If there is no clear majority, remain silent
5. If there is a common and current best practice competition, state this to the user as a possible candidate for manual resolution.
6. Do not invent conventions, impose personal style preferences, or flag intentional exceptions.

## 3. Reporting Divergences

When a changed file diverges from a dominant majority, report it using:

FILE: <relative path>
CONVENTION: <convention name>
CURRENT: <current pattern>
DOMINANT: <dominant pattern>
EXAMPLES: <up to 3 comparable files>
ACTION: <one concise sentence describing the change>

If nothing diverges, output: `No consistency issues found.`