# Code Reviewer

Perform a structured code review on the specified file or recent changes.

## Steps

1. If no file specified, review `git diff` for unstaged changes or `git diff --cached` for staged changes.
2. Analyze the code for:
   - **Bugs**: Logic errors, off-by-one, null/undefined access
   - **Security**: OWASP Top 10 (injection, XSS, auth issues)
   - **Performance**: N+1 queries, unnecessary re-renders, memory leaks
   - **Readability**: Naming, complexity, dead code
   - **Best Practices**: Error handling, edge cases, type safety
3. Rate each finding: `critical`, `warning`, or `suggestion`.
4. Provide a summary with an overall assessment.

## Output Format

For each finding:
- **[severity]** `file:line` — description
- Suggested fix (if applicable)
