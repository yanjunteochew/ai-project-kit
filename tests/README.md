# Test Suite

This directory contains all test files for the project.

## Purpose

Tests validate:
- Functionality works as intended
- Edge cases are handled
- Regressions are caught
- Code quality is maintained

## Test Organization

Tests should mirror the source structure:
```
tests/
├── unit/        - Unit tests for individual functions/modules
├── integration/ - Integration tests between components
└── e2e/         - End-to-end tests
```

## Running Tests

```bash
npm test              # Run all tests
npm run test:watch    # Run tests in watch mode
npm run test:coverage # Run with coverage report
```

## Test Standards

- Each test file should have a corresponding source file
- Tests should follow Arrange-Act-Assert pattern
- Test names should describe behavior clearly
- Keep tests focused and isolated

## Coverage

Aim for:
- Unit test coverage: >80%
- Integration test coverage: Critical paths
- E2E test coverage: Happy path and key workflows
