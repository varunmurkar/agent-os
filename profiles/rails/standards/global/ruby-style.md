# Ruby & Rails Style Guide

Condensed conventions—use RuboCop plus existing code as the final authority.

## Core Principles
- Embrace duck typing; check behavior, not classes.
- Prefer Rails conventions and Hotwire idioms before custom frameworks.
- Keep each change surgical: update only what the task requires.

## Models
- One class per file with sections ordered: associations → scopes → validations → callbacks → public methods → private helpers.
- Use scopes for repeatable queries and keep callbacks minimal.
- Push heavy domain logic into service objects/concerns; keep models readable.

## Controllers
- Keep controllers skinny: authentication/authorization + orchestration only.
- When the project is multi-tenant, scope by tenant context (for example `current_tenant` or project-specific equivalent).
- Use `before_action` for setup, strong parameters for input, and let services handle complex work.
- Prefer Turbo/Stimulus for async behavior rather than custom JS endpoints.

## Views & Helpers
- Favor partials/components for repeated markup; keep data prep in helpers/presenters.
- Avoid inline JavaScript; wire interactivity via Stimulus controllers.
- Use ERB sparingly for logic; anything complex belongs in helpers.

## Services & Jobs
- Single responsibility with explicit initializer arguments and a `call` method.
- Return clear results or raise typed errors; no hidden reliance on controller state.
- Keep them framework-light to simplify testing.

## Methods & Complexity
- Keep methods under ~10 lines; extract to helpers or services when branching grows.
- Limit cyclomatic complexity (<6); guard clause early exits instead of nested conditionals.
- Keep lines ≤100 chars and favor named predicates over comments.

## Comments & Documentation
- Code should explain the “what”; comments are for the “why” (business context, tradeoffs).
- Use `# TODO:` only with an owner/issue link and clean them up quickly.
- Update or remove comments when behavior changes; never leave stale explanations.
