# Git Smart Commit

Analyze the currently staged git changes and generate a conventional commit message.

## Steps

1. Run `git diff --cached --stat` to see what files are staged.
2. Run `git diff --cached` to see the full diff.
3. Determine the commit type: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `style`, `perf`, `ci`, `build`.
4. Detect the scope from the file paths (e.g., `auth`, `api`, `ui`).
5. Write a concise subject line (<72 chars) in imperative mood.
6. If the change is non-trivial, add a body explaining the "why".
7. Present the commit message to the user for approval before committing.

## Output Format

```
<type>(<scope>): <subject>

<body>
```
