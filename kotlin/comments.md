# Kotlin Comment Cleanup Instructions

Examine the provided code and clean up comments according to the following rules:

## Remove
- Temporary or historical comments describing past changes  
  (e.g. "Added this line", "This now works", "Fixed bug here")
- Obvious or redundant comments that restate the code  
  (e.g. `// return the data`, `// increment i`)
- Empty KDoc blocks that add no information beyond the name and signature
- Excessive comments in test code; keep only those that clarify intent,
  edge cases, or non-obvious setup

## Keep
- All `// TODO` and `// FIXME` comments
- KDoc (`/** ... */`) on public and `internal` classes, objects, top-level
  functions, and properties that are part of an externally used module
- Comments that explain **why** something is done, not **what** the code
  already makes clear
- Documentation comments that follow KDoc conventions and are useful to
  consumers of the API

## General Guidance
- Prefer clear naming and types over comments
- Comments should add context, constraints, or rationale that is not
  immediately obvious from the code
- Do not introduce new comments unless they add meaningful value

## Output Format
Output only changed files in their entirety. Do not output files that have not changed.

Use this format for each changed file:

path/to/File.kt
---
```kotlin
<refactored contents>
```
