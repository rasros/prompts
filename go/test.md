## Instructions for Writing Go Tests

Generate tests for the file or files explicitly named in the test-writing prompt that appears after the provided code.  
Any additional files included are for context only and must not receive tests unless the final prompt specifies them.

Tests must validate observable behavior and follow the structure below.

---

## Test Structure Requirements

- Test files live next to the code under test and are named `<file>_test.go`.
- One top-level test function per behavior: `TestThing_Scenario_Expected`.
- Use table-driven subtests (`t.Run`) when testing variants of the same behavior.
- Each test should cover a single behavior.

---

## General Testing Guidelines

**Purpose**
Focus on clear, minimal tests that verify behavior, not implementation details.

**Framework**
- Mirror the framework, layout, and naming used by existing tests in the repo.
- If no tests exist, use the standard `testing` package — do not introduce new dependencies.

**Style**
- Follow the `arrange → act → assert` pattern.
- Make each test self-contained with minimal setup.
- Avoid repetition across tests; pull shared setup into helpers only when it clearly reduces noise.
- Keep code simple and explicit.
- Absolutely no code comments.

**Helpers and Fixtures**
- Reuse existing test helpers and fixtures.
- Do not create new helpers or fixtures unless asked.

**Assertions**
- Use plain `if got != want { t.Errorf(...) }` style unless the repo already uses an assertion library.
- Use `t.Fatal` only when continuing the test would be meaningless.

**Before Writing Tests**
- Review existing tests for naming and structural consistency.

---

## Output Format

Output only the test files in their entirety.

- Use the format:

  path/to/file_test.go
  ---  
  ```go
  <test contents>
  ```
