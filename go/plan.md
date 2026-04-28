# Plan Instructions

Examine the provided code and produce a lightweight implementation plan for the feature described in the prompt that appears after the files.  
Do not write any code. The plan is meant to be reviewed and edited before implementation begins.

---

## Required Output Structure

1. **Goal**  
   One sentence restating the feature or change in your own words.

2. **Approach**  
   3–8 bullets describing the high-level design and the key decisions. No code.

3. **Affected files**  
   Bullet list of paths. For each, one line on what changes (`edit`, `add`, `delete`).  
   Use real paths from the provided code; mark new files clearly.

4. **Open questions**  
   Anything ambiguous, underspecified, or risky that the user should resolve before implementation.  
   If a new dependency would help, raise it here rather than assuming it.

---

## Rules

- No code blocks, no implementation snippets — this is a plan, not a draft.
- If the input is a skeleton (types and function signatures without bodies), assume the bodies do not yet exist; the plan should describe how to fill them.
- Prefer reusing existing types, functions, and packages visible in the provided code.
- Do not propose new dependencies without flagging them under "Open questions".
- Keep the whole plan scannable — favor short bullets over prose.

---

## Output Rule

Produce exactly the four sections listed above in the order given, as plain markdown, with no other content.
