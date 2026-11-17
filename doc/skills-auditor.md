# Skills Auditor registration (AK.skill)

Use [Skills Auditor](https://github.com/ERerGB/skills-auditor) to inspect this pack together with the intended host install roots. Follow its current `SKILL.md` for the inspect → plan → authorized apply → verify lifecycle; the former embedded Bash pipeline is no longer the interface.

## Optional agent configuration

`config/skills-auditor.ak.env` supplies this pack's `skills/` directory to the Auditor agent entry. Adjust the checkout path:

```bash
export AK_SKILL_ROOT="/path/to/AK.skill"
set -a
source "$AK_SKILL_ROOT/config/skills-auditor.ak.env"
set +a
```

These variables describe the agent's maintenance scope. The CLI does not automatically translate them into arguments. They do not authorize applying changes. `SKILLS_AUDITOR_WITH_DRIFT=1` requests remote drift inspection, which fetches Git remotes; the example defaults to 0.

## Direct inspection

Use the actual host roots for this environment. For example:

```bash
AK_SKILLS="/path/to/AK.skill/skills"
skills-audit audit --help
skills-audit audit --skills-dir "$HOME/.codex/skills" --skills-dir "$AK_SKILLS"
```

Add `--with-drift` only when remote fetch is intended. Audit output and source hashes do not establish that the host actually discovered or used every skill.

## Installation and maintenance

Auditing does not itself register the pack. For adoption, inspect `skills-audit integrate --help` and prepare a plan for `skills/` and the chosen host (for example `--target codex@global`). Review its target paths and archive behavior before applying within the user's authorized scope, then verify the receipt and fresh host discovery. Already managed installations must use their existing lifecycle, not an ad hoc relink.

For metadata, duplicates or variants, use only the relevant current maintenance command. Do not assume a broad audit automatically applies deduplication/routing, and do not treat archive or deletion as an implicit default authorization. Preserve existing local edits and differing variants for review.
