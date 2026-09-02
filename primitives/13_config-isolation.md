# Environment Configuration Primitive

Isolate all environment-specific values, ports, domains, and credentials into configuration mechanisms.

## Rules

1. **No Hardcoded Values:** Never write concrete URLs (e.g., `localhost:3000`, `api.staging.example.com`), secret keys, tokens, or environment flags directly inside business logic.
2. **Use Configuration Stores:** Read environment parameters from environment variables (`process.env`, `os.Getenv`, etc.) or centralized project config modules.
3. **Provide Safe Fallbacks:** If providing default fallback values for local development, ensure they are non-sensitive and clearly designated for dev environments.
4. **Document New Variables:** When introducing a new environment variable requirement, update the project's `.env.example` or configuration schema file.

Core principle:

> Code defines behavior; environment variables define location and credentials.