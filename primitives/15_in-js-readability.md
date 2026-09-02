# Modular UI Primitive

When generating HTML-in-JS or CSS-in-JS, prioritize human readability and modularity over minimizing lines of code.

## HTML-in-JS

* Do not place large HTML templates inside a single monolithic function or template literal.
* Break meaningful UI sections into named variables or functions (e.g., `header`, `content`, `footer`).

## CSS-in-JS

* Group styles by logical responsibility (e.g., `layoutStyles`, `headerStyles`, `buttonStyles`) rather than placing an entire stylesheet into one string.

## Component Boundaries & Logic

* Group HTML and CSS according to recognizable UI responsibilities using descriptive names (`card`, `cardStyles`, `modal`, `modalStyles`).
* Avoid generic names like `html1`, `template2`, or `stuff`.
* Separate application and business logic from UI template strings. Prepare data and mappings before assembling the layout.
* Preserve existing technology; do not introduce external preprocessors or frameworks solely for modularity.