---
name: review
description: This skill should be used when the user asks to "review code", "code review", "check for bugs", "review my changes", "review this file", or wants a structured analysis of code quality, security, and correctness.
version: 1.0.0
---

# Code Review

Perform a structured code review on specified files or recent changes.

## Instructions

1. Determine what to review:
   - If the user specifies a file or directory, review that.
   - Otherwise, review `git diff` for unstaged changes or `git diff --cached` for staged changes.
2. Use the `code-reviewer` agent to perform the review by spawning it with the Agent tool (subagent_type: "general-purpose").
3. The review should analyze code for:
   - **Bugs**: Logic errors, off-by-one, null/undefined access, race conditions
   - **Security**: OWASP Top 10 (injection, XSS, authentication issues, sensitive data exposure)
   - **Performance**: N+1 queries, unnecessary re-renders, memory leaks, algorithmic complexity
   - **Readability**: Naming, complexity, dead code, unclear intent
   - **Best Practices**: Error handling, edge cases, type safety, DRY violations
4. Rate each finding with a confidence score (high/medium/low).
5. Provide a summary with an overall assessment.

## Output Format

For each finding:
- **[severity]** `file:line` — description (confidence: high/medium/low)
- Suggested fix (if applicable)

Severity levels: `critical`, `warning`, `suggestion`

## Summary Section

End with:
- Overall assessment (approve / request changes / needs discussion)
- Count of findings by severity
- Top priority items to address
