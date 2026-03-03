---
name: generate-docs
description: This skill should be used when the user asks to "generate docs", "add documentation", "add docstrings", "add jsdoc", "document this code", "add comments", or wants documentation annotations added to their code.
version: 1.0.0
---

# Documentation Generator

Generate documentation annotations for undocumented code.

## Instructions

1. Read the target file.
2. Identify undocumented functions, classes, methods, and type definitions.
3. Detect the language and select the appropriate doc format:
   - **JavaScript/TypeScript**: JSDoc (`/** */`)
   - **Python**: Google-style docstrings (`"""..."""`)
   - **Go**: Godoc comments (`// FunctionName ...`)
   - **Rust**: Doc comments (`/// ...`)
   - **Java/Kotlin**: Javadoc (`/** */`)
   - **C/C++**: Doxygen (`/** */`) or `///`
   - **Ruby**: YARD (`# @param`, `# @return`)
4. Generate concise documentation including:
   - Brief one-line description
   - Parameter descriptions with types (if not already typed)
   - Return value description
   - Thrown exceptions or errors (if applicable)
   - Usage example for complex or non-obvious APIs
5. Apply the documentation using the Edit tool.

## Rules

- Do not document trivially obvious code (simple getters/setters, constructors that just assign fields).
- Match the existing documentation style in the project.
- Keep descriptions concise — prefer one clear sentence over a paragraph.
- Document the **why** when the **what** isn't obvious from the signature.
- Do not add `@type` annotations to TypeScript code that already has type annotations.
- Preserve existing documentation — only add to undocumented items.
