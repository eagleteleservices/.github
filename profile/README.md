# Eagle Tele-Services – GitHub Profile

Welcome to the official GitHub organization for **Eagle Tele-Services**, a nationwide call center and technology partner supporting the commercial trucking and roadside assistance industry.

We use this space to manage and document our internal software tools, automation pipelines, and developer processes.

> Most of our repositories are private and support in-house operations.  
> This page outlines shared engineering practices for our team and collaborators.

For more about us, visit [https://eagleteleservices.biz](https://eagleteleservices.biz)  
Interested in working with us? Reach out at [https://eagleteleservices.biz/careers.html](https://eagleteleservices.biz/careers.html)

---

## Engineering Standards

This document captures the core engineering standards used across Eagle Tele-Services repositories. It covers Git/PR expectations, commit message formats, and versioning rules. Link this file from organization-level or repository-level READMEs to ensure these standards are easy to find.

## Table of contents

- [Git and PR Standards](#git-and-pr-standards)
- [Branch Naming Standards](#branch-naming-standards)
- [Commit Message Format – Conventional Commits](#commit-message-format--conventional-commits)
- [Versioning – Semantic Versioning](#versioning--semantic-versioning)

---

## Git and PR Standards

- All code changes must go through a **pull request (PR)**.
- At least **one approval** is required before merging.
- **Self-approval is allowed**, but a PR and review step are always required.
- Direct pushes to protected branches (for example, `main`) are disabled.

Notes:

- Open a PR for feature work, bug fixes, and configuration changes that affect more than one person.
- Include a short description of the change, testing performed, and any rollout/rollback considerations in the PR body.

---

# Branch Naming Standards

To maintain clarity and consistency across all repositories, please follow this naming convention when creating branches:

```
<type>/<short-description>
```

## Types

Use one of the following conventional prefixes:

- `feat` — A new feature
- `fix` — A bug fix
- `chore` — Non-production changes (e.g., cleanup, tooling)
- `docs` — Documentation-only changes
- `refactor` — Code change that neither fixes a bug nor adds a feature
- `test` — Adding or updating tests
- `ci` — Changes to CI/CD configuration or automation

## Format

- Use **lowercase**
- Separate words in the description using **hyphens**
- Be concise and descriptive

## Examples

```
feat/add-user-auth
fix/timeout-error
chore/remove-deprecated-scripts
docs/update-api-docs
refactor/optimize-query-handling
test/add-integration-tests
ci/update-github-actions
```

## Why It Matters

Consistent branch naming makes it easier to:

- Track work in progress
- Link branches to pull requests and issues
- Navigate repos with many contributors
- Improve automation workflows

> Adopted in alignment with our [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) and Git standards.

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
