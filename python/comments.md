# Python Comment Cleanup Instructions

Examine the provided code and clean up comments and docstrings according to the following rules:

## Remove
- Temporary or historical comments describing past changes  
  (e.g. "Added this line", "This now works", "Fixed bug here")
- Obvious or redundant comments that restate the code  
  (e.g. `# return the data`, `# increment i`)
- Empty or placeholder docstrings that add no information beyond the name and signature
- Excessive comments in test code; keep only those that clarify intent,
  edge cases, or non-obvious setup

## Keep
- All `# TODO` and `# FIXME` comments
- Docstrings on public modules, classes, and functions that are part of an
  externally used package
- Comments that explain **why** something is done, not **what** the code
  already makes clear
- Rationale next to non-obvious type hints, default values, or invariants

## General Guidance
- Prefer clear naming and type hints over comments
- Comments should add context, constraints, or rationale that is not
  immediately obvious from the code
- Do not introduce new comments unless they add meaningful value

## Output Format
Output only changed files in their entirety. Do not output files that have not changed.

- Use the format:

 path/to/file.py
 ---  
 ```python
 <refactored contents>
 ```
