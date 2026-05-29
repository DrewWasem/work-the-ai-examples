# Work the AI Examples — Working in this repo

This repo holds **code companions** to the Work the AI PDF guides. The rules below keep it a code-only resource that complements but never substitutes the paid PDFs.

> 🟢 **This repo is PUBLIC on GitHub at [github.com/DrewWasem/work-the-ai-examples](https://github.com/DrewWasem/work-the-ai-examples).** Every commit ships to the world. Review the diff before pushing.

## The hard rule

**Never include any prose, source, or strategy that lives in a PDF.** This repo is intentionally not a substitute for the paid product.

Before adding a file or folder, run this two-part check:

1. **Could a reader use this file as drop-in code without reading the PDF?** If yes, it likely belongs. If they'd need the PDF to make sense of it, it's pedagogy — don't include it.
2. **Is this file or its content shown verbatim in a PDF?** If yes, default to NO. Templates with `<blanks>` are the only safe exception: scaffolds with no filled-in content.

## Allowed

| Type | Example | Why it's safe |
|---|---|---|
| Template with `<blanks>` | `CLAUDE.md` starter, prompt skeleton structure | Scaffolding, not pedagogy |
| Config file | `.claude/settings.json` Stop hook | Utility, not prose |
| Runnable code | A FastAPI project demonstrating a pattern (code only) | Code, not explanation |
| README pointing to PDF | "Here's what this is; see PDF for why" | Brief signposting |
| LICENSE, `.gitignore` | Standard | Repo infrastructure |

## Forbidden

| Type | Example | Why it's blocked |
|---|---|---|
| PDF source markdown | `claude-code-primary-engineer.md` | The paid product itself |
| Rendered PDF / HTML | `.pdf`, `.html` of the guide | The paid product itself |
| Strategy doc | `product-strategy.md` | Internal business plan |
| Brand voice / lint rules | `brand.md`, `injections.md` from andrew-wasem | Internal IP |
| Prose explanations | "Why the test net matters: ..." | PDF pedagogy |
| Filled-in worked example | Orders-route 5-part spec exactly as in Ch1 / Ch4 | PDF content |
| Renderer | `render_book.py` | Production infrastructure |
| Outlines, drafts, notes | `outline.md`, scratch files | Pre-publication content |
| Founder story / case study | "I shipped two companies..." | PDF prose |

## When you add a new PDF's examples

1. Create `pdf-NN-slug/` (matching publication number, slug from PDF title).
2. Add a brief `README.md` in that folder: one sentence on what's here, one link to [work-the-ai.com](https://work-the-ai.com), bullet list of files with one line each.
3. Add only the allowed types from the table above.
4. Update the top-level `README.md`'s Contents table.

## README voice

READMEs in this repo follow the **andrew-wasem brand** voice (canonical source: `~/claude_projects/content_studio/brands/andrew-wasem/input/brand.md`).
- Plain language first; coder-specific terms second.
- 0 em-dashes (`—`) in body prose.
- 0 banned words (leverage, harness, robust, comprehensive, seamless, utilize, delve, etc.).
- No "simply / just / obviously" before verbs.

## Folder shape

```
work-the-ai-examples/
├── README.md           (intro, links, contents, allow / forbid)
├── CLAUDE.md           (this file)
├── LICENSE
├── .gitignore
└── pdf-NN-slug/
    ├── README.md
    └── <utility-folder>/<files>
```
