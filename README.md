# Work the AI — Examples

Code companions for the **Work the AI** PDF guides. Drop-in templates, hook configurations, and runnable samples that go alongside each PDF.

**Get the PDFs:** [work-the-ai.com](https://work-the-ai.com)
**Author:** Andrew Wasem ([@DrewWasem](https://github.com/DrewWasem))

The PDFs teach the *why* and the *how*. This repo is the *what*: the files you can clone, fork, and run.

## Contents

| Folder | Companion PDF | What's inside |
|---|---|---|
| [`pdf-01-claude-code/`](./pdf-01-claude-code/) | Claude Code as Your Primary Engineer ($27) | Starter `CLAUDE.md`, 5-part prompt skeleton, auto-commit hook |

More folders land here as each PDF in the line ships.

## What goes in this repo

Drop-in utility code that complements a PDF without teaching it:

- **Templates with `<blanks>`** for the reader to fill in (the starter `CLAUDE.md`, the 5-part prompt skeleton structure).
- **Hook configurations** the PDF mentions but doesn't print verbatim (the auto-commit Stop hook JSON).
- **Runnable code samples** that demonstrate a pattern from the PDF in code form, without re-explaining the pattern in prose.
- **READMEs** that briefly say what each file is and point to [work-the-ai.com](https://work-the-ai.com) for the *why*.

## What does NOT go here

Anything that gives away the paid product:

- ❌ PDF source markdown, outlines, or drafts.
- ❌ Rendered `.pdf` or `.html` of any guide.
- ❌ Prose explanations of patterns, principles, or lessons from the PDF.
- ❌ Filled-in worked examples that mirror the PDF's running examples (e.g., the orders-route 5-part spec exactly as in Ch1 / Ch4).
- ❌ The product strategy doc, bundle architecture, pricing, or revenue projections.
- ❌ Brand voice files, lint rules, or any internal andrew-wasem source.
- ❌ The renderer (`render_book.py`) or other production infrastructure.
- ❌ Founder story or case study prose.

If unsure: **default to NOT including it.** The bar: "Could a reader use this as drop-in code without ever reading the PDF?" If yes, include. If it needs PDF context to make sense, it's pedagogy — leave it out.

See [`CLAUDE.md`](./CLAUDE.md) for the full working contract.

## License

MIT. Fork it, use it, ship something.
