# Feature Implementation Prompt

Name: Feature Implementation

Intent / When to use
- Use when you need a concise implementation plan and a minimal code sketch for a small feature that is reviewable and easy to test.

Inputs (required)
- {{FEATURE_DESCRIPTION}} — short description of the feature
- {{CONSTRAINTS}} — constraints (language, frameworks, compatibility)
- {{PROJECT_STYLE_NOTES}} — any style or architectural notes
- Optionally: small file context or existing code snippets

Prompt
You are a senior software engineer. Given the feature description, constraints, and project style notes, provide:
1) Acceptance Criteria (2–6 items)
2) Implementation Plan: list of files to add/change with short rationale
3) Minimal code sketch or patch (diff or code block) sufficient to demonstrate the approach
4) Suggested unit tests (names + short assertions)
5) Estimated risks & rollout notes

Recommended settings
- System message: You are a helpful senior engineer who writes small, testable code changes and clear plans.
- Model: any capable LLM; reduce temperature for deterministic output (0–0.3).

Example input
FEATURE_DESCRIPTION: "Add a health-check endpoint /health returning 200 and JSON {\"status\":\"ok\"}."
CONSTRAINTS: "Keep changes small, follow existing style, add unit test."
PROJECT_STYLE_NOTES: "HTTP handlers live in src/handlers, tests in tests/unit."

Expected response format
- Acceptance Criteria (numbered)
- Implementation Plan (file list)
- Patch (diff)
- Tests (pseudo-code)
- Risk notes

Notes / Safety checks
- Keep implementation language-agnostic in the catalog; include language-specific examples in example files where helpful.
