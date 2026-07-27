# GitHub Labels

This document defines the standard labels used in AI Project Kit projects for organizing and categorizing issues and pull requests.

## Using Labels

Labels help organize issues and PRs by:
- **Type** - What kind of work (bug, feature, documentation, etc.)
- **Priority** - How urgent or important (critical, high, medium, low)
- **Status** - Current state (in progress, blocked, needs review, etc.)
- **Area** - What part of the project is affected

---

## Label Categories

### Type Labels

| Label | Color | Description |
|-------|-------|-------------|
| `bug` | `#d73a49` (red) | Something isn't working |
| `enhancement` | `#a2eeef` (cyan) | New feature or request |
| `documentation` | `#0075ca` (blue) | Documentation improvements |
| `refactor` | `#fbca04` (yellow) | Code refactoring or cleanup |
| `chore` | `#ffd700` (gold) | Maintenance, dependencies, tooling |
| `test` | `#cc317c` (purple) | Testing related |

### Priority Labels

| Label | Color | Description |
|-------|-------|-------------|
| `critical` | `#d73a49` (red) | Must be fixed immediately |
| `high` | `#ff7b72` (orange-red) | Important, should be prioritized |
| `medium` | `#ffd700` (yellow) | Standard priority |
| `low` | `#85e89d` (green) | Nice to have, can wait |

### Status Labels

| Label | Color | Description |
|-------|-------|-------------|
| `in progress` | `#0075ca` (blue) | Currently being worked on |
| `blocked` | `#d73a49` (red) | Cannot proceed, waiting for something |
| `needs review` | `#fbca04` (yellow) | Ready for review, waiting for feedback |
| `help wanted` | `#008672` (teal) | Seeking community help |
| `good first issue` | `#7057ff` (purple) | Good for newcomers |

### Area Labels

Create these based on your project structure:

| Label | Color | Description |
|-------|-------|-------------|
| `area: api` | `#cccccc` (gray) | API-related |
| `area: ui` | `#cccccc` (gray) | User interface |
| `area: database` | `#cccccc` (gray) | Database-related |
| `area: docs` | `#cccccc` (gray) | Documentation |

---

## How to Create Labels in GitHub

1. Go to your repository
2. Click **Settings** → **Labels**
3. Click **New label**
4. Enter label name, description, and color
5. Click **Create label**

Or use the [GitHub CLI](https://cli.github.com/):

```bash
gh label create bug --description "Something isn't working" --color "d73a49"
gh label create enhancement --description "New feature or request" --color "a2eeef"
gh label create documentation --description "Documentation improvements" --color "0075ca"
```

---

## Label Usage Guidelines

### For Issues

- **Always add one type label** (bug, enhancement, documentation, etc.)
- **Add priority label** if appropriate
- **Add status label** if applicable
- **Add area label** to indicate which part of the project

Example: Issue labeled with `bug`, `high`, and `area: api`

### For Pull Requests

- **Add type label** to match the type of changes
- **Add status label** (needs review, blocked, etc.)
- **Add area label** if relevant

### Best Practices

- Use labels consistently across all projects
- Don't over-label (3-4 labels per issue is usually enough)
- Clean up labels regularly to avoid duplication
- Review and adjust labels based on team feedback

---

## Customization

Teams can customize these labels based on their needs:
- Add project-specific area labels
- Adjust colors to match team preferences
- Create additional priority or status labels as needed

Document any customizations in your project's `DECISIONS.md`.
