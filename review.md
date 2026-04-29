# Review Instructions

Examine the provided code and produce a focused code review. The input is typically a diff, a branch's worth of changes, or a set of files staged for review. Any user prompt that follows narrows the scope (e.g. "focus on the auth changes"); otherwise review everything provided.

Do not modify code. The review is meant to be read and acted on by the author.

---

## Required Output Structure

1. **Summary**
   1–2 sentences describing what the change does and your overall assessment (ship / needs work / blocked).

2. **Findings**
   A flat list of findings, each tagged with a severity. Use these tags:
   - `[bug]` — incorrect behavior, crash, data loss, race condition, security issue.
   - `[risk]` — likely-but-not-certain problem; edge cases, unclear invariants, fragile assumptions.
   - `[nit]` — style, naming, minor clarity. Optional to address.
   - `[question]` — something you cannot determine from the provided code; the author should clarify.

   Format each finding as:

   ```
   [severity] path/to/file.ext:line — short title
   <1–3 sentence explanation, grounded in the code. Quote the specific line or snippet if it helps.>
   <Suggested fix in one sentence, if obvious.>
   ```

   Order: all `[bug]` first, then `[risk]`, then `[question]`, then `[nit]`. Within a tag, order by file.

3. **Out of scope** (optional)
   Bullet list of issues you noticed that are real but unrelated to this change. Keep short.

---

## Rules

- Ground every finding in a specific file and line. No vague "consider improving error handling" comments.
- Do not restate what the code does. Focus on what is wrong, risky, or unclear.
- Do not flag style issues that the project's linter or formatter would catch.
- If the change looks fine, say so plainly in the summary and produce a short or empty findings list. Do not invent issues to fill space.
- If the input is a diff, review only the changed lines plus enough surrounding context to judge them. Do not review unrelated existing code.
- If the input is a skeleton (signatures without bodies), review the contract — names, types, signatures, error shape — not hypothetical implementations.
- No commentary on commit messages, branch names, or PR formatting unless asked.

---

## Output Rule

Produce exactly the sections listed above in the order given, as plain markdown, with no other content.
