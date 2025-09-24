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
- [Branching Strategy — GitFlow with Environments](#branching-strategy--gitflow-with-environments)
- [Branch Naming Standards](#branch-naming-standards)
- [Commit Message Format – Conventional Commits](#commit-message-format--conventional-commits)
- [Versioning – Semantic Versioning](#versioning--semantic-versioning)
- [Ruleset Configuration](#ruleset-configuration)

---

## Git and PR Standards

- All code changes must go through a **pull request (PR)**.
- At least **one approval** is required before merging.
- Direct pushes to protected branches (for example, `main`) are disabled.

Notes:

- Open a PR for feature work, bug fixes, and configuration changes that affect more than one person.
- Include a short description of the change, testing performed, and any rollout/rollback considerations in the PR body.

---

## Branching Strategy — GitFlow with Environments

We follow a simplified [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/) branching strategy aligned with our environments:

- `dev` → Default Branch/Active development (feature branches merge here)
- `test` → QA/Staging (validated before production)
- `prod` → Production-ready code (stable, release-approved)

**Feature branches** should be named by type and topic:

feat/locator-ui
fix/api-timeout

Merge flow:
- PR from feature branch → `dev`
- Promotion via PR from `dev` → `test`, and from `test` → `prod`
- Each merge should include clear changelogs and testing status

This helps us maintain stability across environments and simplify rollbacks if needed.

---

## Branch Naming Standards

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

---

### Ruleset Configuration

We maintain our branch protection policies using a version-controlled ruleset file:

**Ruleset File:** [`rulesets/one-ruleset-to-rule-them-all.json`](../rulesets/one-ruleset-to-rule-them-all.json)

This JSON file can be imported into GitHub via CLI or API to enforce consistent policies across repositories.

Note: This file is not auto-enforced — it serves as a reusable source of truth and must be explicitly applied.

For more information, see the official GitHub repository:
[github.com/github/ruleset-recipes](https://github.com/github/ruleset-recipes)

---

This document as well as our standards are a work in progress and will evolve over time
