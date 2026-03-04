# PR Review Playbook (Project Overlay)

Canonical reusable process lives in `skills/pr-review/SKILL.md`.

## Rails Gate Configuration (This Project)

Run Rails quality gates in this strict order:

1. `bundle exec rubocop -a`
2. `bundle exec brakeman -q`
3. `coderabbit review --prompt-only --type all --base <target-branch>`

Default target branch: `develop` unless PR context overrides.

## Overlay Notes

- Use `--plain` for CodeRabbit only when expanded human-readable output is explicitly needed.
- Deferred review items must be tracked in the repository root TODO file per skill rules.
