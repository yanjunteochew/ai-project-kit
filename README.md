# AI Project Kit

A comprehensive toolkit for building AI-powered applications with best practices for architecture, testing, and deployment.

## Features

- **Modular Architecture**: Well-organized project structure for scalability
- **Best Practices**: Linting, testing, and documentation standards
- **AI Integration**: Ready for LLM APIs and AI service integrations
- **Development Ready**: Pre-configured for rapid prototyping

## Quick Start

### Prerequisites

- Node.js 18+ (recommended; CI uses Node 18)
- npm (bundled with Node.js)

### Installation

```bash
git clone https://github.com/yanjunteochew/ai-project-kit.git
cd ai-project-kit
npm install
```

Note: Running `npm install` will create a package-lock.json. Commit the lockfile to ensure deterministic installs and to allow CI to use `npm ci`.

### Run locally

The repository includes a minimal Node.js starter scaffold (src/index.js) and a sample Jest test.

Run the project locally:

```bash
npm start
```

Run tests and coverage:

```bash
npm test
npm run test:coverage
```

Run linter:

```bash
npm run lint
```

### CI

This repository includes a GitHub Actions workflow (.github/workflows/ci.yml) that runs on pushes and PRs to `main`. The workflow:

- checks out the code
- sets up Node 18
- runs `npm ci` (requires package-lock.json)
- runs the linter (currently non-blocking)
- runs the test suite

If you want lint failures to block CI, update the workflow to fail on lint (remove `|| true` in the lint step).

## Project Structure

```
ai-project-kit/
├── src/              # Source code
├── tests/            # Test files
├── docs/             # Documentation
├── .github/          # GitHub templates & workflows
├── package.json      # Project metadata and dependencies
└── README.md         # This file
```

## Documentation

- [Architecture](./docs/architecture.md) - System design and components
- [Contributing](./CONTRIBUTING.md) - Guidelines for contributions

## Next recommended steps

- Commit the generated package-lock.json (run `npm install` locally and commit the lockfile).
- Add environment example: `.env.example` if your project needs runtime configuration.
- Add a `scripts/setup.sh` or `scripts/setup.js` to document local dev setup steps (DBs, env vars, etc.).
- Expand the test suite and add CI checks for coverage if desired.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## Getting Help

For issues and questions, please open an issue on GitHub.
