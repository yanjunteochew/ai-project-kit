# AI Project Kit

A comprehensive toolkit for building AI-powered applications with best practices for architecture, testing, and deployment.

This AI Project Kit is intentionally stack-agnostic: it provides governance, workflows, and templates for collaboration, and does not include opinionated, language-specific starter code. Teams should add starter artifacts appropriate to their chosen stack.

## Features

- Modular Architecture: Well-organized project structure for scalability
- Best Practices: Linting, testing, and documentation standards
- AI Integration: Ready for LLM APIs and AI service integrations
- Development Ready: Conventions and guidance to help you onboard quickly

## Quick Start (stack-agnostic)

1. Clone the repository:

```bash
git clone https://github.com/yanjunteochew/ai-project-kit.git
cd ai-project-kit
```

2. Choose the technology stack appropriate for your project (Node, Python, Go, Rust, etc.).
3. Add the starter artifacts and CI configuration required for your chosen stack.
4. Update ROADMAP.md and DECISIONS.md to reflect your chosen stack and architecture decisions.

## Project Structure

```
ai-project-kit/
├── AGENTS.md            # AI/human collaboration guidance
├── README.md            # This file
├── VISION.md            # Project vision
├── ROADMAP.md           # Roadmap and sprint tasks
├── DECISIONS.md         # Architecture Decision Records (ADRs)
├── docs/                # Documentation and optional starter guides
├── .github/             # Templates & workflows
├── tests/               # Test guidance and optional tests for example starters
└── scripts/             # Utility scripts (optional)
```

## Documentation

- See CONTRIBUTING.md for contribution guidelines
- See PLAYBOOK.md and AGENTS.md for development workflow and responsibilities
- See DEFINITION_OF_DONE.md for completion criteria

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## Getting Help

For issues and questions, please open an issue on GitHub.
