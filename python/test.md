## Instructions for Writing Python Tests (pytest)

Generate pytest-style tests for the file or files explicitly named in the test-writing prompt that appears after the provided code.  
Any additional files included are for context only and must not receive tests unless the final prompt specifies them.

Tests must validate observable behavior and follow the structure below.

---

## Test Structure Requirements

- Test files must be named `test_*.py`.
- Use a test class for each file or major component: `Test<ThingBeingTested>`.
- Use descriptive method names: `test_<method>_<scenario>_<expected>()`.
- Each test should cover a single behavior.

---

## General Testing Guidelines

**Purpose**
Focus on clear, minimal tests that verify behavior, not implementation details.

**Style**
- Follow the `arrange → act → assert` pattern.
- Make each test self-contained with minimal setup.
- Avoid repetition across tests.
- Keep code simple and explicit.
- Absolutely no code comments.

**Fixtures**
- Do not create new fixtures.
- Use only fixtures from `tests/fixtures`, importing them only when needed.

**Parametrization**
- Use `@pytest.mark.parametrize` when testing multiple input/output variants of the same behavior.
- Use separate tests for semantically different behaviors.

**Assertions**
- Use plain `assert` with direct expectations.
- Use `pytest.raises` for exception cases.

**Before Writing Tests**
- Review existing tests for naming and structural consistency.

---


