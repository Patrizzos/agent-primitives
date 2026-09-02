# Security Boundary Primitive

Treat data crossing an application boundary as untrusted unless explicitly validated or trusted by the application.

## Boundaries to Monitor

Pay particular attention to:
* User input
* URL parameters and request bodies
* Form data and uploaded files
* API responses and database values
* Environment variables
* External tool output and third-party integrations

## Verification Steps

Before using external data, determine:
1. What type and shape is expected?
2. Has the data been validated?
3. Does it need escaping or sanitization?
4. Could malformed data cause unsafe behavior?
5. Is sensitive information being exposed unnecessarily?

Apply validation, escaping, authorization, or sanitization at the appropriate boundary. Never assume external data is safe simply because it originated from an API, database, authenticated user, or external tool. Do not introduce unnecessary security mechanisms unrelated to the actual boundary.