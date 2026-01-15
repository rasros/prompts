# Go Comment Cleanup Guidelines

Clean up comments in Go code according to the following rules:

## Remove
- Temporary or historical comments describing past changes  
  (e.g. "Added this line", "This now works", "Fixed bug here")
- Obvious or redundant comments that restate the code  
  (e.g. `// return the data`, `// increment i`)
- Excessive comments in test code; keep only those that clarify intent,
  edge cases, or non-obvious setup

## Keep
- All `TODO` comments
- Comments on exported (public) functions, methods, types, constants,
  and variables that are part of an externally used package
- Comments that explain **why** something is done, not **what** the code
  already makes clear
- Documentation comments that follow Go conventions  
  (e.g. `// Name ...`) suitable for `godoc`

## General Guidance
- Prefer clear naming over comments
- Comments should add context, constraints, or rationale that is not
  immediately obvious from the code
- Do not introduce new comments unless they add meaningful value

Apply these rules consistently across the codebase.

