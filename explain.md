# Explain Instructions

Examine the provided code and explain it. The user prompt that follows narrows the focus (e.g. "explain how requests are routed", "what does this function do"); without a specific question, give an overview of the provided code as a whole.

Do not modify code. The output is meant to help the reader build a mental model.

---

## Required Output Structure

1. **Summary**
   1–3 sentences naming what the code is and what it does. Plain language, no jargon the code itself does not introduce.

2. **How it works**
   Walk through the relevant flow in the order a reader would follow it: entry point → key transformations → outputs or side effects. Use short paragraphs or a numbered list. Reference specific files and symbols using `path/to/file.ext:line` so the reader can jump to the source.

3. **Key types and functions** (if applicable)
   Bullet list naming the most important types, functions, or modules and what each is responsible for. One line each. Skip anything trivial.

4. **Notable details**
   Bullet list of non-obvious behaviors, invariants, edge cases, or design decisions that a reader would not get from the names alone. Examples: ordering guarantees, retry semantics, locking, fallbacks, performance trade-offs.

5. **Open questions** (optional)
   Things you could not determine from the provided code — missing context, external dependencies whose behavior you assumed, or ambiguous logic. Skip if there are none.

---

## Rules

- Ground every claim in the provided code. Do not speculate about behavior that is not visible.
- Do not restate the code line-by-line. Explain at the level of intent and flow; quote a snippet only when the code itself is the clearest explanation.
- Match the depth of the explanation to the user's question. A focused question gets a focused answer, not a tour of the whole module.
- If the input is a skeleton (signatures without bodies), explain the contract — what each piece is for and how they fit together — and say explicitly that the implementation is not provided.
- Tailor the explanation to the user's apparent familiarity. If the user signals they know the language or domain, skip the basics.
- No suggestions for changes, refactors, or improvements unless the user asks.

---

## Output Rule

Produce the sections listed above in the order given, as plain markdown, with no other content. Omit optional sections that do not apply.
