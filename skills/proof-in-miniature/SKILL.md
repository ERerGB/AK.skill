---
name: proof-in-miniature
description: >-
  Pairs strong claims with the smallest falsifiable proof (script, gist, notebook, or runbook) and labels bare-bones baselines clearly.
  Use when arguing that a capability crossed a threshold or when credibility must fit in one link.
---

# Proof in Miniature

Distilled pattern: pair a **strong claim** with the **smallest artifact** that makes the claim falsifiable (code, experiment log, or reproducible runbook).

## When to use

- You are arguing that a capability crossed a threshold (“suddenly usable,” “good enough to loop”).
- You want credibility without a startup demo or a paper.

## Steps

1. **State the threshold in one sentence** — What became true that was not true last quarter?
2. **Shrink the proof** — Prefer lines-of-code count, wall-clock duration, hardware budget, and a public entrypoint. **Vessel options** (pick one primary): single file or gist, minimal repo tag, notebook/Colab duplicate of the same source.
3. **Show one loop** — If the idea is “agentic,” show initialize → act → observe → revise once. One lap beats a architecture diagram.
4. **Say what is still brittle** — One paragraph on failure modes preserves trust.
5. **Label the baseline** — If the artifact is meant to be forked into serious systems, say **“intentionally bare bones”** (or similar) so nobody mistakes minimal for production-complete.

## Anti-patterns

- Screenshots of vibes.
- Huge repos where the insight is buried.
- “Trust me” without a command someone else can run.

## Output shape

- Claim.
- Minimal reproduction (command block or file pointer).
- One paragraph: what it proves / what it does not prove.
