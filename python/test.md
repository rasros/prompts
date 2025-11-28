## Instructions for Writing Python Tests (pytest)

You are generating **pytest-style tests** for the files listed below.  
Follow these rules **strictly** for all produced tests.

### General Testing Guidelines

**Purpose**  
Write clear, minimal, behavior-focused Python tests. Tests must validate observable behavior, not internal implementation details.

**Style**
- Use the `arrange → act → assert` structure.
- One behavior per test; avoid multi-purpose tests.
- Each test must be self-sufficient with minimal setup.
- No repetition across tests.
- Prefer simple, explicit code over abstraction.

**Structure**
- Test files must be named `test_*.py`.
- Use a test class for each file or major component: `Test<ThingBeingTested>`.
- Use descriptive test method names: `test_<method>_<scenario>_<expected>()`.
- We do **not** separate unit/integration tests; all tests follow the same style.
- Do not use mocks, temporary files, or external resources unless explicitly instructed.

**Fixtures**
- **Never create new fixtures. Use only existing fixtures in `tests/fixtures`.**
- Prefer local inline setup when only needed once.
- Import fixtures explicitly and only when required.

**Parametrization**
- Use `@pytest.mark.parametrize` only for multiple input/output variants of the *same* behavior.
- Use separate tests when semantics differ.

**Assertions**
- Use plain `assert` with clear, direct expectations.
- Assert behavior, not implementation details.
- Use `pytest.raises` for exception cases.

**Before Implementing**
- Review similar existing tests for structure, naming, and patterns.

---


