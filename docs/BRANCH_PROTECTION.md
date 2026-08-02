---
title: Branch Protection Rules
description: Guide to setting up and configuring branch protection rules for the AI Project Kit repository
---

# Branch Protection Rules

This guide documents the branch protection rules configured for the AI Project Kit repository to maintain code quality and ensure proper review workflows.

## Purpose

Branch protection rules enforce best practices by:
- Requiring code reviews before merging
- Running automated checks (tests, linting)
- Preventing force pushes to main branches
- Requiring status checks to pass
- Maintaining a clean, auditable commit history

## Main Branch Protection Rules

### Branch: `main`

#### 1. **Require a Pull Request Before Merging**
- ✅ Require approvals: **1 approval minimum**
- ✅ Dismiss stale pull request approvals when new commits are pushed
- ✅ Require review from Code Owners (if `CODEOWNERS` file exists)

**Why:** Ensures at least one other person reviews changes before they reach production.

#### 2. **Require Status Checks to Pass Before Merging**
- ✅ Require branches to be up to date before merging
- ✅ Required status checks:
  - `tests` - All unit and integration tests must pass
  - `lint` - Code style checks must pass
  - `build` - Project must build successfully

**Why:** Prevents broken or untested code from being merged.

#### 3. **Require Branches to Be Up to Date**
- ✅ Enabled

**Why:** Ensures the PR has been tested against the latest main branch code.

#### 4. **Require Code Review Before Merging**
- ✅ Require code owner approval
- ✅ Restrict who can approve (if Code Owners defined)

**Why:** Distributes knowledge and catches issues early.

#### 5. **Require Conversation Resolution Before Merging**
- ✅ Enabled

**Why:** Ensures all discussion threads are resolved, not just approved.

#### 6. **Require Signed Commits**
- ⚠️ Optional (Recommended for production-grade projects)

**Why:** Provides cryptographic proof of authorship and integrity.

#### 7. **Include Administrators**
- ✅ Enabled

**Why:** Ensures rules apply to everyone, including admins.

#### 8. **Restrict Who Can Push to Matching Branches**
- ✅ Enabled (Recommended for enhanced security)

**Why:** Only designated users/roles can push to main.

#### 9. **Allow Force Pushes**
- ❌ Disabled

**Why:** Prevents rewriting history, maintains audit trail.

#### 10. **Allow Deletions**
- ❌ Disabled

**Why:** Prevents accidental branch deletion.

---

## Implementation Steps

### Step 1: Navigate to Branch Protection Settings
1. Go to your repository on GitHub
2. Click **Settings** (gear icon)
3. In the left sidebar, click **Branches**
4. Under "Branch protection rules", click **Add rule**

### Step 2: Configure Rule for `main`
1. Enter branch name pattern: `main`
2. Check the following boxes:

   - [x] Require a pull request before merging
   - [x] Require approvals (set to 1)
   - [x] Dismiss stale pull request approvals when new commits are pushed
   - [x] Require status checks to pass before merging
   - [x] Require branches to be up to date before merging
   - [x] Require code owner reviews (if applicable)
   - [x] Require conversation resolution before merging
   - [x] Include administrators
   - [x] Restrict who can push to matching branches (optional)

3. Under "Status checks that must pass":
   - Add checks: `tests`, `lint`, `build` (once CI/CD is configured)

4. Click **Create** or **Save changes**

### Step 3: Configure GitHub Actions (CI/CD)
Create workflow files in `.github/workflows/` to run:
- Tests (`npm test`)
- Linting (`npm run lint`)
- Build (`npm run build`)

See `.github/workflows/` directory for workflow configurations.

---

## Recommended Additional Configuration

### CODEOWNERS File
Create `.github/CODEOWNERS` to specify who must review changes to specific files:

```
# Default reviewers for all files
* @maintainer-username

# Specific reviewers for critical areas
/src/core/ @core-team
/docs/ @docs-team
```

### Ruleset for Multiple Branches
Consider applying similar (but less strict) rules to:
- `develop` or `staging` branches
- `feature/*` branches (optional, for larger teams)

Example for `develop`:
- Require 1 approval (less strict than main)
- Skip signed commits requirement
- Allow limited force pushes for admins only

---

## Best Practices

### For Contributors
1. ✅ Keep PRs focused and reasonably sized
2. ✅ Write clear PR descriptions and commit messages
3. ✅ Run tests locally before pushing
4. ✅ Keep your branch up to date with main
5. ✅ Respond to review comments promptly

### For Reviewers
1. ✅ Review code thoroughly, not just approve
2. ✅ Test the changes locally if possible
3. ✅ Provide constructive feedback
4. ✅ Approve once satisfied with quality
5. ✅ Merge promptly after approval

### For Maintainers
1. ✅ Review branch protection settings quarterly
2. ✅ Keep status check integrations updated
3. ✅ Monitor and enforce code review standards
4. ✅ Update CODEOWNERS as team changes
5. ✅ Document any exceptions or special cases

---

## Troubleshooting

### "Commit does not have a signature" Error
- Ensure you have [configured Git signing](https://docs.github.com/en/authentication/managing-commit-signature-verification)
- Use `git commit -S` to sign commits

### "Branch is behind main" Error
- Click "Update branch" button in the PR
- Or run locally: `git fetch origin && git merge origin/main`

### PR Cannot Be Merged Despite Approvals
- Check all required status checks are passing (green ✅)
- Ensure all conversations are resolved
- Verify branch is up to date with main

### Cannot Push to Main
- Use a feature branch instead
- Submit a PR for review
- Ask a maintainer for direct push access if absolutely necessary

---

## References

- [GitHub Branch Protection Rules Documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)
- [CODEOWNERS File](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Commit Signature Verification](https://docs.github.com/en/authentication/managing-commit-signature-verification)

---

## Document Metadata

- **Last Updated:** 2026-08-02
- **Status:** Active
- **Owner:** Repository Maintainers
- **Related Documents:**
  - [CONTRIBUTING.md](../CONTRIBUTING.md)
  - [DEFINITION_OF_DONE.md](../DEFINITION_OF_DONE.md)
  - [Git Workflow](./git-workflow.md)
