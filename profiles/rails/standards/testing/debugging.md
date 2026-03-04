# Debugging Standards (Project Overlay)

Canonical reusable guidance lives in `skills/testing/references/debugging-core.md`.

## Project-Specific Overlay

- Supabase/PostgreSQL troubleshooting conventions for this project:
  - `42P01`: missing table/search path issues
  - `42501`: privilege/policy issues
  - `28P01`: auth/session issues
- Prefer project-available telemetry tooling in this order when present:
  1. Sentry integrations
  2. Product analytics traces
  3. Manual exception capture
