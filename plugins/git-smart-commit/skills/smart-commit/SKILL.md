---
name: smart-commit
description: This skill should be used when the user asks to "smart commit", "generate commit message", "conventional commit", "commit my changes", or wants help writing a well-formatted git commit message from staged changes.
version: 1.0.0
---

# Smart Commit

Analyze currently staged git changes and generate a conventional commit message.

## Instructions

1. Run `git diff --cached --stat` to see what files are staged. If nothing is staged, inform the user and stop.
2. Run `git diff --cached` to see the full diff.
3. Run `git log --oneline -5` to see recent commit style for consistency.
4. Determine the commit type from the changes:
   - `feat` — new feature
   - `fix` — bug fix
   - `refactor` — code restructuring without behavior change
   - `docs` — documentation only
   - `test` — adding or updating tests
   - `chore` — maintenance tasks, dependency updates
   - `style` — formatting, whitespace, semicolons
   - `perf` — performance improvement
   - `ci` — CI/CD configuration
   - `build` — build system or external dependencies
5. Detect the scope from file paths (e.g., `auth`, `api`, `ui`, `config`).
6. Write a concise subject line in imperative mood, under 72 characters.
7. If the change is non-trivial, add a body explaining **why** the change was made, not just what changed.
8. Present the commit message to the user for approval before committing.

## Output Format

```
<type>(<scope>): <subject>

<body>
```

## Rules

- Never commit without user approval.
- If multiple unrelated changes are staged, suggest splitting into separate commits.
- Match the tone and style of existing commit history when possible.
