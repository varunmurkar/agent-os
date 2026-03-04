# Backend Models Standards (Project Overlay)

Canonical reusable guidance lives in `skills/backend/references/models-core.md`.

## Project-Specific Overlay

- Rails/ActiveRecord conventions apply for this codebase.
- For Postgres schema/table design, load `skills/supabase-postgres-best-practices/SKILL.md` and the relevant `schema-*`/`security-*` references as required design checks.
- If (and only if) this project is configured for multi-tenancy, map tenant partitioning to project terminology (`practice_id`, `current_practice`, and related helpers).
- For single-tenant projects, do not add tenant partition-key overhead.
