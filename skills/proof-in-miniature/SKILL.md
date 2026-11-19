---
name: proof-in-miniature
description: >-
  Pairs strong claims with the smallest falsifiable proof (script, gist, notebook, or runbook) and labels bare-bones baselines clearly.
  Use when arguing that a capability crossed a threshold or when credibility must fit in one link.
---

# Proof in Miniature

Pair a capability claim with the smallest artifact that lets another person test it.

State the bounded claim first. A threshold or before/after claim needs a real
comparison; do not invent a previous-quarter baseline. Choose a primary artifact
(script, gist, small repository, notebook or runbook) and give the exact inputs,
command, relevant environment/cost and observable result.

For an agentic capability, show one actual initialize→act→observe→revise cycle
when it is part of the claim. Report what ran, what was only proposed and what
failed. Keep the reproduction small enough to expose the mechanism, without
hiding meaningful dependencies behind a line-count claim.

Close with what the artifact establishes and what remains brittle or untested.
Label a teaching/bare-bones baseline accordingly. Screenshots or an architectural
diagram can supplement execution evidence but cannot replace it. Publication is
separate from preparing a local proof.
