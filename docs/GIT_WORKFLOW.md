# Git Workflow

This document describes the Git workflow and branching strategy used in AI Project Kit projects.

## Overview

We follow a simplified Git Flow model adapted for small teams and solo developers.

---

## Branch Strategy

### Main Branches

- **`main`** - Production-ready code. Always stable and deployable.
  - Protected branch - requires pull request reviews
  - Tagged with version numbers (v0.1.0, v0.2.0, etc.)

- **`develop`** - Development integration branch. Contains latest features and fixes.
  - Base branch for feature and bugfix branches

### Supporting Branches

- **`feature/*`** - New features
  - Branch from: `develop`
  - Merge back into: `develop`
  - Naming: `feature/user-authentication`, `feature/api-integration`

- **`bugfix/*`** - Bug fixes for develop
  - Branch from: `develop`
  - Merge back into: `develop`
  - Naming: `bugfix/login-error`, `bugfix/memory-leak`

- **`hotfix/*`** - Critical production fixes
  - Branch from: `main`
  - Merge back into: `main` and `develop`
  - Naming: `hotfix/security-patch`, `hotfix/critical-bug`

- **`release/*`** - Release preparation
  - Branch from: `develop`
  - Merge back into: `main` and `develop`
  - Naming: `release/v0.2.0`

---

## Workflow

### Starting a Feature

```bash
# Update develop branch
git checkout develop
git pull origin develop

# Create feature branch
git checkout -b feature/my-feature

# Work and commit regularly
git add .
git commit -m "feat: describe your changes"
```

### Submitting a Pull Request

1. Push your branch to remote:
   ```bash
   git push origin feature/my-feature
   ```

2. Open a Pull Request on GitHub:
   - Target: `develop` (for features/bugfixes) or `main` (for hotfixes)
   - Fill in PR template
   - Reference related issues: "Closes #42"

3. Wait for reviews and address feedback

4. Merge via GitHub (use "Squash and merge" for features)

### Merging to Main

Only release branches or hotfixes merge to `main`.

```bash
# Create release branch
git checkout -b release/v0.2.0 develop
# Update version numbers, create release notes
git commit -m "chore: bump version to v0.2.0"
git push origin release/v0.2.0

# Create PR to main, get approval, merge
# Then merge release back to develop
```

---

## Rules

- ✅ Always create a branch for work - never commit directly to `main` or `develop`
- ✅ Use descriptive branch names
- ✅ Keep branches focused on one feature/fix
- ✅ Delete branches after merging
- ✅ Keep commit history clean with meaningful messages

---

## Typical Flow

```
main (v0.1.0)
  │
  ├─→ develop
        │
        ├─→ feature/user-auth
        │     ├─ commit
        │     └─ (PR) merge back to develop
        │
        ├─→ bugfix/login-error
        │     └─ (PR) merge back to develop
        │
        └─→ release/v0.2.0
              ├─ (PR) merge to main → tag v0.2.0
              └─ merge back to develop
```

---

## Quick Reference

| Task | Command |
|------|---------|
| Start feature | `git checkout -b feature/name develop` |
| Update branch | `git pull origin branch-name` |
| Push changes | `git push origin branch-name` |
| View branches | `git branch -a` |
| Delete local branch | `git branch -d branch-name` |
| Delete remote branch | `git push origin --delete branch-name` |

---

## Questions?

See CONTRIBUTING.md for more guidelines, or open an issue for workflow questions.
