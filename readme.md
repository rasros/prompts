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
   2–4 short paragraphs explaining what the project does, who it is for, and the key behaviors or design choices that make it distinctive. Ground every claim in the provided code.

4. **Quick links**
   A single line of inline links to the main sections below (e.g. `[Installation](#installation) • [Usage](#usage) • [Configuration](#configuration)`).

5. **Features**
   Bullet list of concrete capabilities. One line each, grounded in actual code.

6. **Installation**
   Subsections per supported install method (package manager, build from source, script). Include only methods that are evidenced by the code (e.g. `go.mod`, `setup.py`, `install.sh`, `Makefile`).

7. **Usage**
   Multiple short subsections, each with a one-line description and a fenced shell or code example. Cover the common flows first, then the more advanced ones. Prefer many small examples over one large one.

8. **Configuration** (if applicable)
   Show the config file location and a minimal example with the most important keys. Only include if the code supports configuration.

9. **Additional sections** (only if warranted by the code)
   Tables for output formats, flags, or comparisons. Architecture notes. Stream/processing models. Skip any section that would be padding.

---

## Style Guidelines

- Write in a direct, technical tone. No marketing language, no emojis, no filler adjectives.
- Prefer concrete examples over abstract descriptions. Every feature claim should be demonstrable from the provided code.
- Use fenced code blocks with language tags (` ```bash `, ` ```yaml `, etc.).
- Keep paragraphs short — 1–3 sentences. Favor bullets and tables over prose where they fit.
- Use tables for comparisons, flag references, and format matrices.
- Section headers use `##`; subsections use `###`. No deeper nesting unless necessary.
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
