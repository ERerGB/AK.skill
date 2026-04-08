# Idea File Handoff

Distilled pattern: when a hot take outgrows a post, promote the durable artifact to an **idea file** — a spec an agent can implement in *your* environment, not a frozen app.

## When to use

- A post went broad; replies want “the repo,” but the value is the **pattern**, not your stack-specific glue.
- You want others to fork behavior without forking code.

## Steps

1. **Extract the invariant** — What must stay true across editors, models, and OSes? Put that in prose with stable headings.
2. **Separate policy from mechanism** — Permissions, freshness rules, citation rules, and folder layout are policy; specific tools are examples in a sidebar.
3. **Make it agent-addressable** — Write so a tool can follow: numbered constraints, checklists, and “do / do not” rules.
4. **Host where discussion attaches** — Prefer a gist or repo with **Discussion** (or issues) so the idea evolves in public. Encourage **forks of the pattern** (tool-specific variants) rather than one canonical implementation.
5. **Link rabbit holes** — Point to talks, posts, or repos for depth; keep the idea file itself the **stable compression layer**.

## Anti-patterns

- Dumping a private `.cursor` folder as “the product.”
- Sharing only screenshots of a working wiki with no replication recipe.
- Letting the artifact rot without a “last verified” note.

## Output shape

- Short intro: who it is for, what problem it solves.
- Architecture sections: inputs, update loop, cross-link strategy, trust boundaries.
- One “give this to your agent” block: paste-ready instructions.
