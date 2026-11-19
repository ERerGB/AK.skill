---
name: scoreboard-loop
description: >-
  Defines a cheap-to-evaluate score and one mutable workspace so agents iterate from numbers; separates immutable prep from editable experiment files.
  Use when designing overnight experiment loops, autoresearch-style harnesses, or metric-gated agent iteration.
---

# Scoreboard Loop

Design bounded iteration around an evaluator whose result changes the next decision.
Reuse the user's objective and constraints; do not substitute a convenient metric.

Define the score or task rubric, hard gates, baseline, evaluator command and allowed
edit surface before a run. Separate immutable evaluation data/preparation from the
candidate so the optimizer cannot improve its score by changing the measurement.
If a scorer defect must be repaired, record that separately and rebaseline.

Provide a command for one experiment and a log of candidate revision, result and
accept/reject decision. Set a finite cycle/time/resource budget before unattended
iteration; keep the best verified candidate on timeout or failure. A small baseline
can be a reusable template without claiming production completeness.

The user owns the objective, forbidden changes and review boundaries. State what
the metric misses, especially when it can be gamed. Do not launch an overnight
job, paid run or recurring schedule merely because the design supports one.
