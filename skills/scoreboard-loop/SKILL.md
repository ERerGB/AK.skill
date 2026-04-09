---
name: scoreboard-loop
description: >-
  Defines a cheap-to-evaluate score and one mutable workspace so agents iterate from numbers; separates immutable prep from editable experiment files.
  Use when designing overnight experiment loops, autoresearch-style harnesses, or metric-gated agent iteration.
---

# Scoreboard Loop

Distilled pattern: give agents (or humans) a **cheap-to-score objective** and a **single mutable workspace**; let iteration be driven by numbers, not vibes.

## When to use

- You want continuous improvement (training code, prompts, configs, pipelines) without hand-running every experiment.
- You can define a metric that is **efficient to evaluate** relative to the cost of proposing changes.

## Steps

1. **Freeze the interface** — One script or file is the contract: edit here, run `train` / `eval`, read score. Everything else is optional. When you need hygiene, split **immutable prep** (data, constants) from **mutable experiment surface** so diffs stay reviewable.
2. **Publish the scoreboard** — Stdout table, log file, or wandb-style trail; the loop must make “better / worse” unambiguous.
3. **Let the optimizer be dumb but persistent** — Agents propose diffs; the metric decides survival. Novelty comes from breadth of search, not from charisma in the proposal.
4. **Keep the baseline intentionally bare** — Frame the first version as a **template for a pattern**, not a finished product—so others fork the loop, not your hyperparameters.
5. **Human owns objective and constraints** — What is optimized, what is forbidden, and what requires review stays outside the agent.

## Anti-patterns

- Fuzzy goals (“make it better”) with no scalar or rubric.
- Letting agents change eval code and training code in one step without separation of duties.
- Chasing leaderboard metrics you admit are gamed or meaningless—pair with epistemic honesty (see **Hype–Discipline Pairing**).

## Output shape

- Objective function (one paragraph).
- Command(s) to reproduce one experiment.
- What the agent is allowed to edit vs read-only.
- One paragraph: what this loop does *not* solve.
