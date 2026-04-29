My personal prompts. Feel free to use them.

I use them with https://github.com/rasros/lx, which has a `-P` flag for picking a prompt by path or name from a library directory. Point `LX_PROMPTS_DIR` at a clone of this repo and `lx -P go/refactor src/` will prepend the matching prompt to your bundled context.

The language directories (go, kotlin, python) hold prompts that produce code edits and follow that language's conventions: comments, plan, refactor, test. The root-level prompts are language-agnostic and produce analysis or documentation rather than code: review, explain, and readme.

Each prompt is a single self-contained markdown file with the rules baked in, so they work the same whether you pipe them into a CLI, paste them into a chat, or load them through some other tool.
