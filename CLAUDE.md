# CLAUDE.md

## Branch Naming Convention

When working on a GitHub issue or opening a new pull request, always create a
dedicated branch instead of committing to the default branch. Name the branch
after the functionality being implemented, using the following rules:

- Use a short, descriptive, kebab-case name that reflects the feature, fix, or
  task at hand (e.g., `add-user-authentication`, `fix-markdown-parsing`).
- Prefix the branch name with a type that matches the work:
  - `feature/` for new functionality
  - `fix/` for bug fixes
  - `chore/` for maintenance, tooling, or refactoring
  - `docs/` for documentation changes
- When the work originates from an issue, include the issue number after the
  prefix (e.g., `feature/42-add-user-authentication`).
- Keep names lowercase, hyphen-separated, and free of spaces or special
  characters.

Always create and switch to this branch before making any changes, and open the
pull request from that branch.
