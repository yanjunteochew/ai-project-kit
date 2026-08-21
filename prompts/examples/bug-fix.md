# Bug Fix Prompt

Name: Bug Fix

Intent / When to use
- Use when diagnosing a failing test, runtime error, or bug report and designing a minimal, test-covered fix.

Inputs (required)
- {{ERROR_LOG}} or failing test output
- {{RELATED_FILES}} (relevant code snippets)
- {{REPRO_STEPS}} (how to reproduce)

Prompt
You are a debugger. Given the failing test log, error stack, and relevant code files, do the following:
1) Provide a plausible root-cause explanation (1–3 bullets)
2) Propose a minimal fix (code patch or one-line change)
3) Provide or modify unit test(s) that reproduce and validate the fix
4) Mention any risks, side-effects, and migration steps

Recommended settings
- System message: You are a careful engineer who prefers minimal, well-tested fixes.
- Model: low temperature (0–0.2)

Example input
ERROR_LOG: "TypeError: x.map is not a function"
RELATED_FILES: snippet showing x may be null or a non-array
REPRO_STEPS: "Run tests: npm test ./tests/unit/transform.test.js"

Expected response format
- Root cause bullets
- Patch (diff)
- Unit test (name + assertions)
- Risk notes

Notes / Safety checks
- Prefer the smallest safe change that fixes the immediate issue and adds a regression test.
