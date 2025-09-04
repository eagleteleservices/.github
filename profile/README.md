# Eagle Tele-Services – Engineering Standards

## Git & PR Standards

- All code changes must go through a **pull request**.
- At least **one approval** is required before merging.
- **Self-approval is allowed**, but a PR and review step are always required.
- Direct pushes to protected branches (e.g., `main`) are disabled.

---

## Commit Message Format – Conventional Commits

We follow the [Conventional Commits](https://www.conventionalcommits.org/) standard.

Example formats:
```

feat: add API support for X
fix: correct error when user inputs Y
chore: clean up unused code

```
Common prefixes:
# Eagle Tele-Services — Engineering Standards

This document captures the core engineering standards used across Eagle Tele-Services repositories. It covers Git/PR expectations, commit message formats, and versioning rules. Link this file from organization or repository READMEs to make the rules easy to find.

## Table of contents

- [Git & PR Standards](#git--pr-standards)
- [Commit message format — Conventional Commits](#commit-message-format---conventional-commits)
- [Versioning — Semantic Versioning](#versioning---semantic-versioning)

---

## Git & PR Standards

- All code changes must go through a **pull request (PR)**.
- At least **one approval** is required before merging.
- **Self-approval is allowed**, but a PR and review step are always required.
- Direct pushes to protected branches (for example, `main`) are disabled.

Notes:

- Open a PR for feature work, bug fixes, and configuration changes that affect more than one person.
- Include a short description of the change, testing performed, and any rollout/rollback considerations in the PR body.

---

## Commit message format — Conventional Commits

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification for structured, machine-readable commit messages.

Example messages:

```text
feat: add API support for X
fix: correct error when user inputs Y
chore: clean up unused code
```

Common types (prefixes):

- `feat`: a new feature
- `fix`: a bug fix
- `chore`: tooling, cleanup, or config changes
- `docs`: documentation-only changes
- `refactor`: code changes that neither fix a bug nor add a feature
- `test`: adding or updating tests
- `ci`: changes to CI/CD configuration

Tips:

- Keep the short description (after the prefix) under 72 characters where possible.
- Use the body to explain *why* the change was made and any migration notes.

---

## Versioning — Semantic Versioning

We use [Semantic Versioning](https://semver.org/).

```text
MAJOR.MINOR.PATCH
```

Increment rules:

- MAJOR version when you make incompatible API changes.
- MINOR version when you add functionality in a backward-compatible manner.
- PATCH version when you make backward-compatible bug fixes.

When releasing, include a short changelog entry that explains the user-facing impact.

---

If you'd like, I can also:

- add a CONTRIBUTING section with a PR template link,
- add GitHub Actions workflow examples for commit linting and release tagging,
- or convert this to an `README.md` at the org level and add a small badge summary.


