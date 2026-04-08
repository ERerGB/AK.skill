# Irreducible Core

Distilled pattern: ship a **terminal simplification** claim—*this is the smallest honest container for the idea*—then **teach through the file** section by section.

## When to use

- You are demystifying a stack (compiler, model, training loop, protocol) and want the reader to *see* the whole system at once.
- You want forks and ports without maintaining a framework.

## Steps

1. **State the compression claim** — One sentence: why you cannot delete another line without lying or hiding a real dependency.
2. **Pick one vessel** — Prefer a **single file** or a **gist** as the canonical artifact; add Colab/notebook only as a runnable duplicate, not the source of truth.
3. **Walk the reader in document order** — Dataset → core math → model → train → sample (or your domain’s equivalent). Each block answers “what problem does this solve?”
4. **Name what is “just efficiency”** — Separate the invariant algorithm from speed tricks so experts know where to optimize without confusing beginners.
5. **Link the long-form explainer** — Point to a video or post for the hardest subsection only; keep the artifact self-contained for the motivated reader.

## Anti-patterns

- A “simple” repo with twenty packages where the idea is still scattered.
- Claiming minimality while hiding imports that do the real work.
- Teaching only via video with no stable text anchor.

## Companion pattern: commit-granular curriculum

When the full stack is too large for one file, pair the **minimal core** with a repo whose **git history is the syllabus** (one conceptual step per commit), plus a long-form video or post that walks commits in order. Centralize **errata and FAQ** next to the repo so the teaching artifact stays maintainable.

## Output shape

- One sentence: irreducibility claim.
- One link: canonical minimal artifact.
- Outline: section titles matching the file.
- One paragraph: efficiency vs essence.
