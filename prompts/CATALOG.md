# Prompt Catalog

Purpose
- A curated catalog of reusable prompts for common development tasks. Each prompt entry includes intent, required inputs, the prompt text (with placeholders), recommended model/settings, an example input, and the expected response format.

How to use
1. Pick the prompt entry that matches your task.
2. Replace placeholders ({{...}}) with concrete repo/context values.
3. Provide the prompt to your preferred model using the suggested system message and settings.
4. Review the model output, run tests, and update the prompt entry if needed.

Prompt entry template
- Name
- Intent / When to use
- Inputs (required)
- Prompt (with placeholders)
- Recommended settings (system msg, model, temperature)
- Example input
- Expected response format
- Notes / Safety checks

Included prompt types
- Feature implementation (prompts/examples/feature-implementation.md)
- Code review (prompts/examples/code-review.md)
- Bug fix (prompts/examples/bug-fix.md)
- Refactoring (prompts/examples/refactor.md)
- Architecture review (prompts/examples/architecture-review.md)

Contributing
- Add new prompts under prompts/examples/.
- Follow the Prompt entry template.
- Include at least one example input and expected output format.
- Open an issue for large or opinionated prompts before adding them.
- Use label: area:prompts for prompt-related issues/PRs.

Backlog & roadmap
- See ROADMAP.md — Sprint 3 (AI Prompt Library). Link this catalog from ROADMAP.md once added.

License & attribution
- Prompts in this repo are licensed under the repository MIT license. If a prompt is derived from external sources, add attribution.
