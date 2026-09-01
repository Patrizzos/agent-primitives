# Security Boundary Primitive

Treat data crossing an application boundary as untrusted unless it has been explicitly validated or trusted by the application.

Pay particular attention to:

- user input
- URL parameters
- form data
- request bodies
- API responses
- uploaded files
- environment variables
- database values
- external tool output
- third-party integrations

## Before using external data

Determine:

1. What type and shape is expected?
2. Has the data been validated?
3. Does it need escaping or sanitization?
4. Could malformed data cause unsafe behavior?
5. Is sensitive information being exposed unnecessarily?

Apply validation, escaping, authorization, or sanitization at the appropriate boundary.

Do not assume that external data is safe because it came from:

- an API
- a database
- a browser
- an authenticated user
- another agent
- another tool

Do not introduce unnecessary security mechanisms unrelated to the actual boundary.

Core principle:

> Trust should be established at boundaries, not assumed.