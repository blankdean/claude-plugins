# Dependency Auditor

Scan project dependencies for security vulnerabilities, outdated packages, and unused imports.

## Steps

1. Detect the package manager (npm, yarn, pnpm, pip, cargo, go mod).
2. Run the appropriate audit command:
   - `npm audit` / `yarn audit` / `pnpm audit`
   - `pip-audit` or `safety check`
   - `cargo audit`
3. Check for outdated packages using the relevant command.
4. Scan source files to identify dependencies that are installed but never imported.
5. Present findings grouped by severity.

## Output Format

### Vulnerabilities
| Package | Severity | Description | Fix |
|---------|----------|-------------|-----|

### Outdated
| Package | Current | Latest | Breaking? |
|---------|---------|--------|-----------|

### Unused
- List of installed but unused packages
