# AI Project Kit

# CONTRIBUTING

Version: 1.0

---

# Purpose

This document defines the engineering standards for contributing to this project.

These standards apply equally to human contributors and AI assistants.

The objective is to produce software that is:

- easy to understand
- easy to review
- easy to maintain
- easy to test
- easy to extend

---

# General Principles

Every contribution should:

- solve one logical problem
- minimise unnecessary changes
- preserve existing behaviour unless intentionally changed
- improve overall code quality
- leave the project in a better state

---

# Before Starting Work

Before making changes:

- Read PROJECT_OVERVIEW.md
- Review the current ROADMAP.md
- Check DECISIONS.md for relevant ADRs
- Understand the current implementation
- Clarify unclear requirements before coding

---

# Branching Strategy

Unless the project specifies otherwise:

- Main branch should always remain stable.
- Work should be completed on feature or fix branches.
- Merge only after review and validation.

Example branch names:

```
feature/email-sync

feature/oauth-login

fix/message-parser

fix/cache-expiry

docs/playbook-update

refactor/mail-storage
```

---

# Commit Guidelines

Each commit should represent **one logical change**.

Good commits are:

- small
- focused
- reviewable
- reversible

Avoid combining unrelated work.

---

## Commit Message Format

Use Conventional Commits where practical.

Examples:

```
feat(email): add IMAP retry support

fix(parser): handle empty attachments

docs(playbook): clarify workflow

refactor(storage): simplify mailbox cache

test(sync): add regression test for duplicate emails

chore(ci): update GitHub workflow
```

---

# Feature Development

When implementing a feature:

1. Understand the requirement.
2. Plan the implementation.
3. Implement incrementally.
4. Validate behaviour.
5. Update documentation.
6. Update ROADMAP.md.

Avoid implementing speculative functionality.

---

# Bug Fix Workflow

When fixing defects:

1. Reproduce the bug.
2. Identify the root cause.
3. Fix the underlying problem.
4. Verify the fix.
5. Add or update regression tests where practical.
6. Ensure no existing behaviour is broken.
7. Document behavioural changes if required.

Avoid patching symptoms without understanding the cause.

---

# Refactoring

Refactoring should:

- improve readability
- reduce complexity
- simplify maintenance

Refactoring should **not** introduce behavioural changes.

Separate refactoring from feature work whenever practical.

---

# Testing Expectations

Every contribution should include appropriate validation.

Validation may include:

- manual testing
- automated tests
- integration tests
- regression tests
- edge case verification

Testing should be proportional to the size and risk of the change.

---

# Documentation

Documentation is part of every contribution.

Update documentation whenever:

- behaviour changes
- architecture changes
- workflows change
- setup instructions change

Documentation should always reflect the current implementation.

---

# Pull Request Guidelines

A pull request should:

- have a clear objective
- remain focused on one topic
- explain significant design decisions
- describe testing performed
- identify known limitations

Large pull requests should be avoided.

---

# AI Contributor Guidelines

AI contributors should:

- explain reasoning
- ask questions when requirements are unclear
- avoid making assumptions
- prefer existing project conventions
- recommend improvements without unnecessary redesign
- keep implementations incremental
- update documentation alongside code

---

# Code Review Checklist

Before requesting review, verify:

- code is understandable
- unnecessary complexity has been removed
- naming is consistent
- validation has been completed
- documentation has been updated
- roadmap reflects current progress

---

# Guiding Principle

> Every contribution should make the project easier to understand, easier to maintain, and easier for the next contributor to continue.