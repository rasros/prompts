# README Instructions

Examine the provided code and produce a `README.md` for the project at the repository root.
If an existing `README.md` is included in the input, treat it as the source of truth for tone, structure, and existing content — update it in place rather than rewriting from scratch. If no README is included, create one.
Output only the final README contents, ready to be written to disk.

---

## Required Output Structure

1. **Title and tagline**
   Project name as an H1, followed by a one-sentence description of what the project does.

2. **Badges** (optional)
   Include only badges that are clearly applicable from the provided code (license, package registry, CI). Skip if unclear.

3. **Overview**
   2–4 short paragraphs explaining what the project does, who it is for, and the key behaviors or design choices that make it distinctive. Ground every claim in the provided code. For libraries with multiple components, a numbered list naming each component (with a bold concept name and one-line description) often works well here.

4. **Features**
   Short bullet list of the most important capabilities. One line each, grounded in actual code. Only include features that add detail beyond the overview — do not restate what the intro already says. No bold headers on individual bullets. Skip this section entirely when the per-component sections below already cover the same ground (common for libraries).

5. **Installation**
   Subsections per supported install method, evidenced by the code:
   - CLI tools: package manager (`go install`, `pip install`), curl/install script, `Makefile` build.
   - Kotlin/JVM libraries: a `dependencies { implementation("group:artifact:version") }` Gradle Kotlin DSL block. Mention any required companion plugins or libraries (e.g. `kotlinx.serialization`).
   - Python libraries: `pip install <name>`.

6. **Usage** or per-component deep-dives
   - For CLI tools: multiple short subsections, each with a one-line description and a fenced shell example. Cover common flows first, then advanced. Prefer many small examples over one large one.
   - For libraries: one `##` section per main component or entry point. Lead with 1–2 sentences explaining what the component is for, then a fenced code example in the project's language showing typical use. Within these sections, bullet lists with a bold leading concept (e.g. `* **Bit-Packing**: ...`) are appropriate for enumerating sub-features.

7. **Additional sections** (only if warranted by the code)
   Tables for output formats, flags, comparisons, or codec/encoding matrices. Architecture notes. Stream/processing models. Configuration file format. Extension/customization examples (e.g. custom serializers, transforms, plugins) shown as separate `##` or `###` sections with code. Skip any section that would be padding.

---

## Style Guidelines

- Write in a direct, technical tone. No marketing language, no emojis, no filler adjectives.
- Prefer concrete examples over abstract descriptions. Every feature claim should be demonstrable from the provided code.
- Use fenced code blocks with language tags (` ```bash `, ` ```yaml `, etc.).
- Keep paragraphs short — 1–3 sentences. Favor bullets and tables over prose where they fit.
- Use tables for comparisons, flag references, and format matrices.
- Section headers use `##`; subsections use `###`. No deeper nesting unless necessary.
- Separate top-level sections with a `---` horizontal rule when the README has several major components or deep-dive sections (common for libraries). Skip the rules for short CLI READMEs where they add noise.
- Use the project's language for code examples (Kotlin for Kotlin/JVM projects, Go for Go projects, Python for Python projects). Shell examples remain in `bash`.
- Do not invent features, flags, file paths, or dependencies that are not present in the provided code.
- If the input is a skeleton (types and signatures without bodies), describe only what the signatures imply; do not speculate about runtime behavior.
- Do not include a "Contributing", "Roadmap", "Changelog", or "License" section unless the user asks for one or the code clearly indicates it (e.g. a `LICENSE` file warrants a one-line license note).

---

## Editing an Existing README

When a `README.md` is present in the input:

- Preserve its title, tagline, overall structure, and section order unless they conflict with the code.
- Keep the existing tone, formatting conventions, and any badges, images, or links that are still valid.
- Only change sections that are out of date, inaccurate, or missing relative to the provided code. Leave unrelated sections untouched.
- Add new sections only when the code introduces capabilities the README does not cover. Remove sections only when the corresponding feature is gone from the code.
- If the user prompt names a specific change (e.g. "document the new `--xml` flag"), scope edits to that change and surrounding context.
- Output the full README, not a diff or a list of edits.

---

## Output Rule

Produce the README contents as a single markdown document, with no commentary before or after.
