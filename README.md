# Claude Plugins Marketplace

A curated collection of Claude Code plugins for productivity, development, and automation.

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| **Git Smart Commit** | Generates conventional commit messages from staged changes | 1.2.0 |
| **Code Reviewer** | Structured code reviews with severity ratings and OWASP checks | 0.9.0 |
| **Test Generator** | Generates unit tests with edge case coverage | 1.0.0 |
| **Doc Generator** | Generates JSDoc, docstrings, and type annotations | 0.5.0 |
| **Dependency Auditor** | Scans for vulnerable, outdated, or unused dependencies | 1.1.0 |

## Installation

```bash
/plugin marketplace add https://github.com/blankdean/claude-plugins
```

Then install individual plugins:

```bash
/plugin install git-smart-commit
/plugin install code-reviewer
/plugin install test-generator
/plugin install doc-generator
/plugin install dep-auditor
```
