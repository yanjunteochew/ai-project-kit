# AI Project Kit

# PLAYBOOK

Version: 1.0

---

# Purpose

The Playbook defines the standard workflow for every contributor, whether human or AI.

Its purpose is to ensure that work is:

- Understood before implementation
- Planned before coding
- Built in small increments
- Tested before completion
- Documented as it evolves

This document describes **how work is performed**.

Engineering standards, commit conventions, and Definition of Done are documented separately.

---

# Core Principles

## 1. Understand Before Building

Never begin implementation immediately.

First understand:

- the project objective
- the current roadmap
- relevant architectural decisions
- existing implementation
- current sprint goal

If requirements are unclear, ask questions.

Do not make assumptions.

---

## 2. Documentation is the Source of Truth

Before making recommendations, read:

1. PROJECT_OVERVIEW.md
2. ROADMAP.md
3. DECISIONS.md
4. Relevant design documents
5. Existing implementation

Project documentation takes precedence over previous conversations.

---

## 3. Work in Small Increments

Large changes increase risk.

Break work into small, reviewable tasks that:

- solve one problem
- are independently testable
- can be reviewed easily
- can be reverted if necessary

Prefer steady progress over large feature drops.

---

## 4. Plan Before Implementing

Before writing code:

- explain the objective
- propose an implementation approach
- identify trade-offs
- discuss alternatives where appropriate
- obtain agreement for significant changes

Planning reduces unnecessary rework.

---

## 5. Implement Consistently

During implementation:

- follow existing project conventions
- minimise complexity
- prefer readable code
- avoid unnecessary dependencies
- avoid speculative features
- preserve backwards compatibility where practical

Consistency is more valuable than cleverness.

---

## 6. Validate Every Change

Every change should be validated before completion.

Validation may include:

- manual testing
- automated tests
- regression testing
- edge case verification
- peer review

If validation cannot be completed, explain why.

---

## 7. Keep Documentation Current

Documentation is part of the deliverable.

Whenever implementation changes:

- update relevant documentation
- update ROADMAP.md
- update DECISIONS.md when architectural decisions are made
- record assumptions if they affect future work

Documentation should always reflect reality.

---

## 8. Record Significant Decisions

When making long-term decisions:

- create an ADR
- describe the context
- explain the rationale
- document alternatives considered
- describe the consequences

Future contributors should understand *why* a decision was made.

---

## 9. Leave the Project Better Than You Found It

When completing work:

- remove temporary code
- remove debugging artefacts
- simplify where appropriate
- improve readability where practical
- avoid introducing technical debt

Every completed task should improve the project.

---

# Standard Workflow

Every task follows the same lifecycle.

```
Understand
    ↓
Plan
    ↓
Implement
    ↓
Validate
    ↓
Review
    ↓
Document
    ↓
Complete
```

Do not skip stages.

---

# AI Collaboration Guidelines

AI contributors should:

- explain recommendations
- recommend rather than dictate
- avoid hidden assumptions
- ask for clarification when uncertain
- optimise for maintainability
- preserve project consistency
- minimise unnecessary changes

AI should assist engineering, not replace engineering judgement.

---

# Continuous Improvement

At the completion of each milestone, ask:

- What worked well?
- What slowed progress?
- What should become standard practice?
- What should be improved next time?

Capture useful lessons so future projects benefit.

---

# Responsibilities

The Playbook defines **how work is performed**.

Refer to:

- AGENTS.md for responsibilities
- CONTRIBUTING.md for engineering standards
- DEFINITION_OF_DONE.md for completion criteria
- ROADMAP.md for current priorities
- DECISIONS.md for architectural history

---

# Guiding Principle

> Build the smallest valuable improvement, validate it, document it, and leave the project in a better state than before.