# ROADMAP.md

**Project:** AI Project Kit  
**Document:** Roadmap  
**Version:** 1.0.0  
**Status:** Complete  
**Owner:** Product Owner  
**Last Updated:** 2026-08-23

---

# Purpose

This roadmap is the single source of truth for project progress.

At the beginning of every development session:

1. Read VISION.md.
2. Read AGENTS.md.
3. Read this roadmap.
4. Identify the Current Task.
5. Complete only that task unless instructed otherwise.

---

Note: This AI Project Kit is intentionally stack-agnostic. It provides governance, workflows, and templates for collaboration — not opinionated language-specific starter code. Teams should add starter artifacts appropriate for their chosen tech stack when they use this kit as a template.

---

# Project Status

## ✅ AI Project Kit v1.0.0 – Complete

The AI Project Kit is now feature-complete. All core objectives have been achieved:

- ✅ **Governance & Documentation** — Comprehensive project standards and decision-making framework
- ✅ **Development Standards** — Git workflows, commit conventions, and code style guidelines
- ✅ **AI Collaboration Framework** — Agents, playbooks, and prompt library for AI-assisted development
- ✅ **Repository Structure** — Clear organization with proper templates and conventions

### Why No Starter Templates?

Sprint 4 (Starter Templates) has been **intentionally skipped** because:

1. **Stack-agnostic philosophy** — The kit's value is in its *processes and standards*, not in language-specific starter code.
2. **Contradicts core principle** — Providing Node.js/Python starters violates the intentional decision to remain stack-agnostic.
3. **Teams customize anyway** — Teams using this kit will replace starters with their own tech choices.
4. **Maintenance burden** — Multiple starter examples create ongoing maintenance without clear value.
5. **Clear guidance exists** — The README and CONTRIBUTING.md already guide teams to add their own starter artifacts.

The kit provides everything needed for teams to build their own starters using the established governance and standards.

---

# Future Enhancements

Ideas for potential future versions (demand-driven, not planned):

- AI memory integration
- Multi-agent workflows
- Automated sprint planning
- Documentation generator
- Repository health checks
- Release automation
- CI/CD pipeline templates
- Language-specific starter examples (if requested by users)

Future features will be added only when there is clear user demand and they align with the stack-agnostic philosophy.

---

# Completed Sprints

## Sprint 3 – AI Prompt Library ✅

### Outcome

Successfully created a reusable prompt library for common development tasks.

### What Went Well

- Prompt catalog created and documented (prompts/CATALOG.md)
- Five essential example prompts provided for common tasks:
  - Feature implementation prompt
  - Code review prompt
  - Bug fix prompt
  - Refactoring prompt
  - Architecture review prompt
- Clear contributing guidelines established for future prompt expansions
- Minimal, focused approach aligned with stack-agnostic philosophy

### Lessons Learned

- Optional expansions don't require upfront issue creation; they can be added incrementally based on actual demand
- Bare-minimum prompt library provides immediate value without over-engineering
- Contributing guidelines provide sufficient process for future contributors to add new prompts

### Improvements to AI Project Kit

- Teams now have reusable prompts for common AI-assisted development tasks
- Clear structure for extending the prompt library in the future
- Established best practices for prompt documentation and versioning

### Repository Version

v0.2.0

---

## Sprint 2 – Development Standards ✅

### Outcome

Successfully documented key development standards for template users.

### What Went Well

- Created clear Git workflow documentation with branching strategy
- Established Conventional Commits standard for clean commit history
- Documented code style guidelines with language-specific examples
- Focused on bare-minimum essentials rather than comprehensive documentation

### Lessons Learned

- Bare-minimum approach delivers value faster
- Focus on most impactful standards first (git workflow, commits, style)
- Template users appreciate practical, actionable guidelines

### Improvements to AI Project Kit

- Teams now have clear development standards to follow
- Git workflow and commit conventions prevent common mistakes
- Code style guidelines promote consistency across projects

### Repository Version

v0.2.0

---

## Sprint 1 – GitHub Configuration ✅

### Outcome

Set up GitHub templates and repository governance to support professional collaboration.

### What Went Well

- Issue templates created and committed (.github/ISSUE_TEMPLATE/)
- Pull request template created (.github/pull_request_template.md)
- GitHub labels defined and documented
- Repository settings guide written
- Branch protection rules documented and recommended settings described
- ROADMAP.md and README.md updated to reflect stack-agnostic intent

### Lessons Learned

- Consistent templates reduce triage friction for contributors
- Explicit repository settings guidance helps maintainers configure new projects faster
- Keeping the kit stack-agnostic avoids forcing a specific technology choice

### Improvements to AI Project Kit

- Improved onboarding for contributors via issue/PR templates
- Clearer repository governance and settings guidance
- Foundation laid for optional starter examples in future sprints

### Repository Version

v0.2.0

---

## Sprint 0 – Foundation ✅

### Outcome

Successfully established core documentation and repository structure for AI Project Kit.

### What Went Well

- Created comprehensive project governance documents (VISION, AGENTS, PLAYBOOK, etc.)
- Established clear Definition of Done standards
- Built bare-minimum template structure with proper organization
- Documented project roadmap and decision-making process

### Lessons Learned

- Bare-minimum templates are sufficient for most use cases
- Clear documentation upfront saves time later
- Project governance documents are as important as code

### Improvements to AI Project Kit

- Added project structure clarity
- Established foundation for future sprints
- Created reusable template for AI-powered projects

### Repository Version

v0.2.0

---

# Sprint Review Template

When a sprint is completed, record:

## Sprint X – <Title>

### Outcome

...

### What Went Well

...

### Lessons Learned

...

### Improvements to AI Project Kit

...

### Repository Version

vX.X.X
