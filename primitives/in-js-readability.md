# Modular UI Primitive

When generating HTML-in-JS or CSS-in-JS, prioritize human readability and modularity over minimizing lines of code.

## HTML-in-JS

Do not place a large HTML template inside a single function or template literal.

Break meaningful UI sections into named pieces.

Prefer:

```js
const header = `
  <header class="site-header">
    <h1>${title}</h1>
    <nav>${navigation}</nav>
  </header>
`;

const content = `
  <main class="site-content">
    ${body}
  </main>
`;

const page = `
  ${header}
  ${content}
`;
```

over a single giant template.

## CSS-in-JS

Do not place an entire stylesheet into one monolithic string.

Group styles by logical responsibility.

Prefer:

```js
const layoutStyles = `
  .layout {
    display: grid;
    min-height: 100vh;
  }
`;

const headerStyles = `
  .site-header {
    padding: 1rem;
  }
`;

const buttonStyles = `
  .button {
    cursor: pointer;
    padding: 0.5rem 1rem;
  }
`;

const styles = `
  ${layoutStyles}
  ${headerStyles}
  ${buttonStyles}
`;
```

## Component boundaries

Group HTML and CSS according to recognizable UI responsibilities.

Examples:

- header
- navigation
- hero
- card
- modal
- form
- footer

Use descriptive names such as:

- `card`
- `cardStyles`
- `modal`
- `modalStyles`

Avoid names such as:

- `html1`
- `template2`
- `styles3`
- `stuff`

## Keep logic separate

Do not put substantial application or business logic inside HTML or CSS template strings.

Prefer:

```js
const items = getItems();

const cards = items.map(renderCard).join("");

const page = renderPage({ cards });
```

over embedding complex loops, conditionals, and business logic throughout a giant HTML string.

## Preserve the existing technology

Do not introduce a framework, component library, preprocessor, or dependency solely to make the UI more modular.

Improve organization within the existing architecture.

## Final check

Before returning code, ask:

- Can a human quickly identify each UI section?
- Are large templates broken into logical pieces?
- Are styles grouped by responsibility?
- Is application logic separated from presentation?
- Can one UI component be modified without navigating a giant string?

If not, refactor before returning the code.

Core principle:

> HTML, CSS, and UI logic should be modular enough that a human can understand and modify the interface without mentally parsing a giant JavaScript file.