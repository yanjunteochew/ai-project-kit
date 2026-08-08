# AI Project Kit

A stack-agnostic project kit that documents best practices, workflows, and governance for AI-assisted development. This repository provides process, templates, and guidance — teams add their preferred starter code and tooling for the stack they choose.

## What this kit provides

- Governance and collaboration documents (VISION, PLAYBOOK, AGENTS, CONTRIBUTING, DEFINITION OF DONE, DECISIONS)
- Issue and PR templates to standardise triage & contributions
- Guidance for CI/CD, testing, and release workflows (docs and READMEs)
- Directory conventions and examples for where to add starter code and tests

## How to use this kit

1. Clone the repository:

```bash
git clone https://github.com/yanjunteochew/ai-project-kit.git
cd ai-project-kit
```

2. Choose the technology stack appropriate for your project (Node, Python, Go, Rust, etc.).
3. Add the starter artifacts for that stack in the recommended locations (see "Project structure").
4. Update ROADMAP.md and DECISIONS.md to reflect your chosen stack and any architecture decisions.
5. Implement CI workflows and lockfiles as required by your package manager and team policies.

Note: This kit intentionally does not include opinionated, language-specific starter artifacts (for example: package.json, src/index.js, or lockfiles). That allows teams to adopt the kit for any stack without needing to remove or refactor an included starter.

## Features

- Modular architecture for processes and docs
- Best-practice guidance for collaboration, reviews, and testing
- AI-first playbook and contributor guidance
- Development-ready conventions that are intentionally stack-agnostic

## Project structure (example)

```
ai-project-kit/
├── AGENTS.md            # AI/human collaboration guidance
├── README.md            # This file
├── VISION.md            # Project vision
├── ROADMAP.md           # Roadmap and sprint tasks
├── DECISIONS.md         # Architecture Decision Records (ADRs)
├── docs/                # Documentation and optional starter guides
├── .github/             # Templates & workflows (workflows may be examples)
├── tests/               # Test guidance and optional tests for example starters
├── scripts/             # Utility scripts (optional)
└── <optional-starters>/ # e.g. starters/nodejs, starters/python (add as needed)
```

The `<optional-starters>/` area is intentionally optional. Add starter projects for the stacks your team needs (and document them under docs/starter-guides.md if helpful).

## Documentation

- See CONTRIBUTING.md for contribution guidelines
- See PLAYBOOK.md and AGENTS.md for development workflow and responsibilities
- See DEFINITION_OF_DONE.md for completion criteria

## Next recommended steps when creating a new project from this kit

- Add starter artifacts appropriate to your chosen stack (e.g., package.json & package-lock.json for Node; pyproject.toml & poetry.lock for Python). Commit the lockfile recommended by your package manager.
- Create CI workflow files in .github/workflows that reflect your chosen toolchain.
- Add an `.env.example` if runtime configuration is required.
- Add scripts/setup.sh or scripts/setup.md to document local dev setup steps (databases, env vars, etc.).
- Optionally add example starter folders under `starters/` and document them in `docs/starter-guides.md`.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## Getting Help

For issues and questions, please open an issue on GitHub.
