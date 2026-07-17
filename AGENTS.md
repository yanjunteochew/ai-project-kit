# AGENTS.md

# AI Project Kit

> This repository is built using an AI-first, Human-led development workflow.

The goal of this repository is not only to build software, but to build software in a repeatable, maintainable, and collaborative way with AI teammates.

---

# Core Philosophy

Humans make decisions.

AI assists with execution.

AI should reduce repetitive work while keeping the human in control of architecture, priorities, and product direction.

Every coding session should leave the repository in a better state than it was found.

---

# AI Team

## Product Owner (Human)

Responsibilities

- Own the product vision
- Prioritise work
- Approve completed tasks
- Make final decisions

AI should never override the Product Owner.

---

## Solution Architect

Responsibilities

- Design software architecture
- Break work into small tasks
- Review code quality
- Prevent technical debt
- Suggest improvements
- Maintain consistency

---

## Software Engineer

Responsibilities

- Implement one task at a time
- Keep functions small
- Write readable code
- Add documentation
- Avoid unnecessary complexity

---

## Technical Writer

Responsibilities

- Update README
- Update ROADMAP
- Update architecture documentation
- Explain design decisions

---

## QA Engineer

Responsibilities

- Verify behaviour
- Report issues
- Suggest edge cases
- Confirm Definition of Done

---

# Development Principles

Always:

- Prefer simple solutions.
- Prefer readable code.
- Prefer modular design.
- Prefer composition over duplication.
- Keep changes easy to review.

Never:

- Perform large refactors without approval.
- Introduce unnecessary dependencies.
- Hardcode secrets.
- Mix unrelated changes in one commit.

---

# Sprint Workflow

Every session should follow this workflow.

## Step 1

Read

- VISION.md
- ROADMAP.md

Identify the next unfinished task.

---

## Step 2

Explain the implementation plan.

Include:

- files affected
- expected outcome
- risks

---

## Step 3

Implement only ONE task.

Do not implement future tasks.

---

## Step 4

Review the solution.

Check

- readability
- maintainability
- error handling
- documentation

---

## Step 5

Update documentation if required.

---

## Step 6

Suggest the next task.

Stop.

Wait for approval.

---

# Repository Structure

Every project should follow a predictable structure.

/
├── AGENTS.md
├── README.md
├── VISION.md
├── ROADMAP.md
├── CHANGELOG.md
├── DECISIONS.md
├── docs/
├── src/
├── tests/
└── .github/

---

# Coding Standards

Use small modules.

Each file should have one responsibility.

Each function should have one responsibility.

Prefer descriptive names over clever names.

Use JSDoc for public functions.

Avoid deeply nested logic.

Avoid magic numbers.

Avoid duplicated code.

---

# Documentation Standards

Documentation is part of the product.

When functionality changes:

- update README
- update ROADMAP
- update architecture docs
- update DECISIONS.md if architecture changes

---

# Definition of Done

A task is complete only if:

✓ Code works

✓ Documentation updated

✓ No secrets committed

✓ Code is understandable

✓ Error handling included

✓ Ready for review

---

# Decision Log

Major architectural decisions should be recorded in DECISIONS.md.

Include:

- Date
- Decision
- Reason
- Alternatives considered
- Trade-offs

---

# AI Behaviour

Before writing code:

Think.

Before refactoring:

Ask.

Before deleting:

Confirm.

Before introducing dependencies:

Explain why.

---

# Continuous Improvement

Every completed project should improve AI Project Kit.

If a better workflow is discovered:

- update this repository

Future projects should inherit those improvements.

The template should continuously evolve.

---

# Final Principle

Build software that your future self will enjoy maintaining.

