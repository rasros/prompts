## Instructions for Writing Kotlin Tests

Generate tests for the file or files explicitly named in the test-writing prompt that appears after the provided code.  
Any additional files included are for context only and must not receive tests unless the final prompt specifies them.

Tests must validate observable behavior and follow the structure below.

---

## Test Structure Requirements

- Test files mirror the source layout under `src/test/kotlin/...` (or the project's existing test directory).
- Use a test class per file or major component, named `<ThingBeingTested>Test`.
- Use descriptive function names; backticked names are encouraged: `` `returns empty list when input is empty`() ``.
- Each test should cover a single behavior.

---

## General Testing Guidelines

**Purpose**
Focus on clear, minimal tests that verify behavior, not implementation details.

**Framework**
- Mirror the framework, layout, and naming used by existing tests in the repo (JUnit 4/5, Kotest, Spek, etc.).
- If no tests exist, use JUnit 5 with `kotlin.test` assertions and do not introduce new dependencies.

**Style**
- Follow the `arrange → act → assert` pattern.
- Make each test self-contained with minimal setup.
- Avoid repetition across tests.
- Keep code simple and explicit.
- Absolutely no code comments.

**Fixtures and Helpers**
- Reuse existing fixtures and test helpers.
- Do not create new fixtures or helpers unless asked.

**Parameterization**
- Use the framework's parameterized form (e.g. JUnit 5 `@ParameterizedTest`, Kotest `forAll` / data-driven specs) when testing variants of the same behavior.
- Use separate tests for semantically different behaviors.

**Assertions**
- Use the assertion style already present in the repo. If none, prefer `kotlin.test.assertEquals` and `assertFailsWith`.

**Before Writing Tests**
- Review existing tests for naming, framework, and structural consistency.

---

## Output Format

Output only the test files in their entirety.

- Use the format:

  path/to/FileTest.kt
  ---  
  ```kotlin
  <test contents>
  ```
