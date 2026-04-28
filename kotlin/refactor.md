# Refactor Instructions

Examine the provided code and apply the refactor goal that appears after the files.  
Give a brief motivation, then output only the refactored files.

---

## Required Output Structure

1. **Refactor Motivation**  
   - Identify the problems relevant to the stated refactor goal.  
   - Explain why the refactor is beneficial.  
   - Keep the explanation concise and grounded in the provided code.

2. **Refactored Files**  
   - Output only the files that are changed, added, or removed.  
   - Use the format:

     path/to/file.kt
     ---  
     ```kotlin
     <refactored contents>
     ```

   - For removed files, replace contents with `<deleted>`.  
   - Do not add any commentary after the files.

---

## Refactoring Guidelines

- Improve clarity, maintainability, correctness, and structure according to the refactor goal.  
- Do not change external behavior unless explicitly allowed.  
- Do not add new dependencies.  
- Keep changes minimal but meaningful.  
- Do not modify or generate tests unless instructed.  
- Prefer direct, explicit improvements over broad redesign.
- If the input is a skeleton (classes, interfaces, and function signatures without bodies), treat it as the structural contract. Refactor the signatures only and do not invent function bodies unless the goal explicitly asks for them.

---

## Output Rule

Produce exactly the two sections listed above in the order given, with no other content.

---
