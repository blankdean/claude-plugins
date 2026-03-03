# Claude Plugins Marketplace

A curated collection of Claude Code plugins for productivity, development, and automation.

## Available Plugins

| Plugin | Description | Skill Triggers |
|--------|-------------|----------------|
| **git-smart-commit** | Generates conventional commit messages from staged changes | "smart commit", "generate commit message", "conventional commit" |
| **code-reviewer** | Structured code reviews with severity ratings and OWASP checks | "review code", "code review", "check for bugs" |
| **test-generator** | Generates unit tests with edge case coverage | "generate tests", "write tests", "add unit tests" |
| **doc-generator** | Generates JSDoc, docstrings, and type annotations | "generate docs", "add documentation", "add docstrings", "add jsdoc" |
| **dep-auditor** | Scans for vulnerable, outdated, or unused dependencies | "audit dependencies", "check vulnerabilities", "outdated packages" |

## Installation

Add this marketplace:

```bash
/plugin marketplace add blankdean/claude-plugins
```

Then install individual plugins:

```
/plugin install git-smart-commit@blankdean-claude-plugins
/plugin install code-reviewer@blankdean-claude-plugins
/plugin install test-generator@blankdean-claude-plugins
/plugin install doc-generator@blankdean-claude-plugins
/plugin install dep-auditor@blankdean-claude-plugins
```

## Structure

Each plugin follows the standard Claude Code plugin format:

```
plugins/{plugin-name}/
├── .claude-plugin/
│   └── plugin.json       # Plugin metadata
├── skills/
│   └── {skill-name}/
│       └── SKILL.md      # Skill definition with YAML frontmatter
├── agents/               # (optional) Agent definitions
│   └── {agent-name}.md
└── README.md
```

## License

MIT
