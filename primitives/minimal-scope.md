# Minimal Scope Primitive

Solve the requested problem with the smallest reasonable change, avoiding overengineering and unnecessary dependencies.

## 1. Prevent Overengineering

* Implement the simplest solution that directly satisfies the current requirement, but ensure safety, security, and assess common and current best practices as a part of selected solution.
* Do not build speculative complexity, support theoretical future requirements, or optimize for hypothetical scale.
* Avoid introducing new abstractions, services, configuration layers, design patterns, or infrastructure if existing code can solve the problem.

## 2. Dependency Evaluation

Before adding any new dependency, confirm:
1. Can the requirement be solved by existing dependencies in the project?
2. Does the language or platform already provide this functionality?
3. Can the requirement reasonably be implemented with simple existing code?
4. Does adding the dependency materially increase bundle size, runtime cost, or complexity?

Do not add a dependency merely for a more convenient API. If a dependency is genuinely necessary to avoid reinventing a complex library, use it.

## 3. Minimal Diff Enforcement

* Identify exact files and lines that need to change before editing.
* Do not rewrite untouched code, reformat unrelated sections, rename unrelated variables, reorganize unrelated imports, or fix unrelated bugs discovered during the task.
* Do not refactor surrounding code unless strictly required.
* Review the diff prior to completion and revert any non-essential changes.