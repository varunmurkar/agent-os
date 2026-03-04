# Testing Standards (Project Overlay)

Canonical reusable guidance lives in `skills/testing/references/tests-core.md`.

## Project-Specific Overlay

- Primary test stack in this project: RSpec for request/policy/service/unit tests.
- Minitest system tests are acceptable where full-stack coverage is needed.
- Apply tenant-context header/scoping tests only when this project uses multi-tenancy.
- If multi-tenancy is enabled in this project, current tenant naming may use `practice` terminology.
