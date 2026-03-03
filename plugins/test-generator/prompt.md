# Test Generator

Generate unit tests for the specified function, class, or file.

## Steps

1. Read the target source file.
2. Identify exported functions/classes and their signatures.
3. Detect the project's test framework (jest, pytest, vitest, mocha, etc.).
4. Generate tests covering:
   - Happy path with typical inputs
   - Edge cases (empty input, boundary values, null/undefined)
   - Error cases (invalid input, thrown exceptions)
   - Mocking of external dependencies
5. Write the test file following the project's existing test conventions.

## Conventions

- Place tests adjacent to source or in the project's test directory.
- Follow the existing naming pattern (e.g., `*.test.ts`, `test_*.py`).
- Use `describe`/`it` or equivalent grouping from the detected framework.
