# Repository Settings Guide

This document describes the recommended GitHub repository settings for AI Project Kit projects.

## Overview

Proper repository configuration ensures consistency, security, and professional collaboration standards.

---

## Essential Settings

### General Settings

**Location:** Settings → General

- **Repository name** - Clear, descriptive name
- **Description** - Brief overview of the project
- **Visibility** - Public (for open source) or Private (for internal)
- **Default branch** - Set to `main` or `develop` based on your Git workflow

**Recommended:**
- ✅ Require status checks to pass before merging
- ✅ Require code reviews before merging
- ✅ Enforce branch protection rules

---

## Branch Protection

**Location:** Settings → Branches → Add rule

### Protect the `main` Branch

1. **Branch name pattern:** `main`

2. **Require pull request reviews before merging**
   - ✅ Require at least 1 approval
   - ✅ Dismiss stale pull request approvals

3. **Require status checks to pass before merging**
   - ✅ Require branches to be up to date before merging
   - Add CI/CD workflows as required status checks (if applicable)

4. **Additional protections**
   - ✅ Require signed commits (optional but recommended)
   - ✅ Restrict who can push to matching branches

### Optional: Protect the `develop` Branch

Similar settings to `main`, but may allow fewer approvals or different restrictions based on team size.

---

## Collaborators & Permissions

**Location:** Settings → Collaborators and teams

- **Admin** - Full repository access (typically maintainers only)
- **Maintain** - Can merge PRs, manage issues, but can't delete repo
- **Write** - Can push changes and merge PRs
- **Triage** - Can manage issues and PRs but can't push code
- **Read** - Can pull but can't push

**Recommendation:** Limit Admin access to project leads.

---

## Code Security

**Location:** Settings → Security & analysis

- ✅ Enable **Dependabot alerts** - Get notified of security vulnerabilities
- ✅ Enable **Dependabot security updates** - Auto-update vulnerable dependencies
- ✅ Enable **Secret scanning** - Detect exposed secrets
- ✅ Enable **Code scanning** - Detect code quality issues (if using GitHub Advanced Security)

---

## Actions & Automation

**Location:** Settings → Actions

- **Workflow permissions**
  - Limit to read-only for external contributors
  - Allow write access for organization members

---

## Issue & PR Templates

**Location:** Settings → General → "Set up templates"

- ✅ Enable issue templates (see `.github/ISSUE_TEMPLATE/`)
- ✅ Enable pull request template (see `.github/pull_request_template.md`)

---

## Discussion Settings (Optional)

**Location:** Settings → Options → Discussions

- Enable if you want community discussion forum
- Configure categories for different types of discussions

---

## Webhook & API

**Location:** Settings → Webhooks

- Configure webhooks for CI/CD, notifications, or integrations
- Examples:
  - Slack notifications for PR reviews
  - Discord alerts for failed deployments
  - Custom automation workflows

---

## Rules & Policies

**Location:** Settings → Rules

- Create ruleset for branch protection across organization (if applicable)
- Define commit message requirements
- Enforce status checks

---

## Quick Setup Checklist

After creating a new repository:

- [ ] Set repository description and topics
- [ ] Configure default branch to `main`
- [ ] Create branch protection rule for `main`
- [ ] Require at least 1 PR review before merge
- [ ] Enable Dependabot alerts and security updates
- [ ] Enable secret scanning
- [ ] Add collaborators with appropriate permissions
- [ ] Configure issue and PR templates
- [ ] Add topics/labels to repository
- [ ] Set up README with getting started instructions

---

## Template Repository Configuration

If this repository will be used as a template:

1. **Location:** Settings → General
2. **Enable** "Template repository" checkbox
3. Users can then use "Use this template" button to create new repos

---

## Automation & Integrations

Common GitHub integrations to consider:

- **Slack** - Notifications for PRs, issues, and deployments
- **Discord** - Similar to Slack, community-friendly
- **Codecov** - Coverage reporting
- **CodeQL** - Security scanning
- **Dependabot** - Dependency updates
- **Renovate** - Alternative to Dependabot

---

## References

- [GitHub Documentation - Repository Settings](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features)
- [GitHub Branch Protection](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches)
- [GitHub Security](https://docs.github.com/en/code-security)
