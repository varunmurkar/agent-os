# Error Handling Standards (Project Overlay)

Canonical reusable guidance lives in `skills/engineering-core/references/error-handling-core.md`.

## Project-Specific Overlay

- This project may enforce a canonical API error envelope and tracing headers on API responses.
- Keep status-code mapping and response schema consistent with existing API contracts in the repository.
- Apply tenant-specific error isolation only when this project is operating in multi-tenant mode.
