# Doc Generator

Generate documentation annotations for undocumented code.

## Steps

1. Read the target file.
2. Identify undocumented functions, classes, and methods.
3. Detect the language and appropriate doc format:
   - JavaScript/TypeScript: JSDoc (`/** */`)
   - Python: Google-style docstrings
   - Go: Godoc comments
   - Rust: `///` doc comments
4. Generate concise docs including:
   - Brief description
   - Parameter descriptions with types
   - Return value description
   - Thrown exceptions (if applicable)
5. Apply the documentation using the Edit tool.
