# Commit Message Conventions

This document describes the commit message format used in AI Project Kit projects.

## Overview

We follow the **Conventional Commits** specification for clear, semantic commit messages that are easy to parse and understand.

---

## Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type

Required. Must be one of:

- **feat** - A new feature
- **fix** - A bug fix
- **docs** - Documentation only changes
- **style** - Changes that don't affect code meaning (formatting, missing semicolons, etc.)
- **refactor** - Code change that neither fixes a bug nor adds a feature
- **perf** - Code change that improves performance
- **test** - Adding or updating tests
- **chore** - Changes to build process, dependencies, or tooling
- **ci** - Changes to CI/CD configuration

### Scope

Optional. Specify what part of the codebase is affected:

```
feat(api): add user authentication
fix(database): resolve connection timeout
docs(readme): update installation steps
```

### Subject

Required. Rules:

- Use imperative mood ("add" not "added" or "adds")
- Don't capitalize first letter
- No period (.) at the end
- Limit to 50 characters
- Be specific and descriptive

### Body

Optional. Use for detailed explanation:

- Explain **what** and **why**, not how
- Wrap at 72 characters
- Separate from subject with a blank line

Example:
```
feat(auth): implement JWT authentication

Add JWT token generation and validation for API endpoints.
This improves security by replacing session-based auth.

Tokens expire after 24 hours and include user role information.
```

### Footer

Optional. Reference issues and breaking changes:

```
Closes #42
Fixes #123
Breaking-Change: API response format changed
```

---

## Examples

### Good Commits

```
feat(api): add user registration endpoint

fix(login): resolve password validation bug

docs: update contributing guidelines

style: format code with prettier

test(auth): add unit tests for token validation

chore(deps): upgrade axios to 1.0.0
```

### Bad Commits

```
updated stuff
fixed bug
WIP: working on feature
Added new function
TODO: finish this later
```

---

## Benefits

- ✅ Clear history that's easy to scan
- ✅ Automated changelog generation possible
- ✅ Better code review context
- ✅ Easier debugging with git blame/bisect
- ✅ Professional and consistent codebase

---

## Quick Reference

| What You Did | Type | Example |
|---|---|---|
| New feature | feat | `feat(api): add payment endpoint` |
| Bug fix | fix | `fix(ui): resolve button overflow` |
| Documentation | docs | `docs: add API reference` |
| Code formatting | style | `style: format with prettier` |
| Refactoring | refactor | `refactor: simplify user service` |
| Performance | perf | `perf: optimize image loading` |
| Tests | test | `test: add auth tests` |
| Dependencies | chore | `chore(deps): update react` |

---

## Tips

- Commit often with small, logical changes
- Write commit message in present tense
- One change per commit when possible
- Use scope to provide context
- Reference issues in footer: "Closes #42"

---

## More Information

See [Conventional Commits](https://www.conventionalcommits.org/) for full specification.
