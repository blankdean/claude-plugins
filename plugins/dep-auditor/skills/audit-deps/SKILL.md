---
name: audit-deps
description: This skill should be used when the user asks to "audit dependencies", "check vulnerabilities", "outdated packages", "security scan", "check deps", or wants to analyze project dependencies for issues.
version: 1.0.0
---

# Dependency Auditor

Scan project dependencies for security vulnerabilities, outdated packages, and unused imports.

## Instructions

1. Use the `auditor` agent to perform the audit by spawning it with the Agent tool (subagent_type: "general-purpose").
2. The audit should:
   - Detect the package manager (npm, yarn, pnpm, pip, cargo, go mod)
   - Run the appropriate audit command for vulnerabilities
   - Check for outdated packages
   - Scan source files to identify installed-but-unused dependencies
3. Present findings in the structured format below.

## Output Format

### Vulnerabilities
| Package | Severity | Description | Fix |
|---------|----------|-------------|-----|

### Outdated
| Package | Current | Latest | Breaking? |
|---------|---------|--------|-----------|

### Unused
- List of installed but never-imported packages

### Summary
- Total vulnerabilities by severity
- Number of outdated packages
- Recommended priority actions
