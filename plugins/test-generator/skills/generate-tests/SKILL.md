---
name: generate-tests
description: This skill should be used when the user asks to "generate tests", "write tests", "add unit tests", "create test file", "test this function", or wants automated test generation for their code.
version: 1.0.0
---

# Test Generator

Generate unit tests for the specified function, class, or file.

## Instructions

1. Read the target source file.
2. Identify exported functions, classes, and their signatures.
3. Detect the project's test framework by checking:
   - `package.json` for jest, vitest, mocha
   - `pytest.ini`, `setup.cfg`, `pyproject.toml` for pytest
   - `Cargo.toml` for Rust tests
   - Existing test files for patterns
4. Check for existing test files and conventions:
   - Naming pattern (e.g., `*.test.ts`, `test_*.py`, `*_test.go`)
   - Test directory structure (co-located vs. separate `__tests__/` or `tests/`)
   - Import style and assertion patterns
5. Generate tests covering:
   - **Happy path**: Typical inputs producing expected outputs
   - **Edge cases**: Empty input, boundary values, null/undefined, zero, empty strings
   - **Error cases**: Invalid input, thrown exceptions, rejected promises
   - **Mocking**: External dependencies, API calls, file system operations
6. Write the test file following the project's existing conventions.

## Rules

- Match the existing test style in the project. If no tests exist, use the most common convention for the language.
- Use `describe`/`it` or equivalent grouping from the detected framework.
- Include meaningful test names that describe the expected behavior.
- Keep tests independent — no shared mutable state between tests.
- Add setup/teardown only when necessary.
