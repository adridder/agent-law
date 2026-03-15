# Methodology

This folder explains how the benchmark should be read before anyone turns the results into claims.

## Why this exists

Benchmark results are easy to oversell. These docs are here to keep the interpretation disciplined, public, and fair.

## Read in this order

1. [`PRE_RUN_PROTOCOL.md`](./PRE_RUN_PROTOCOL.md) - what the studies are testing, what they can support, and what would be a stretch
2. [`THEORY.md`](./THEORY.md) - why these conditions were chosen and what would count as support for the practical claim
3. [`INTERPRETING_RESULTS.md`](./INTERPRETING_RESULTS.md) - how to read the outputs without over-claiming

## What the methodology does

- anchors both studies to the same raw battle-test table
- uses blind scoring across five dimensions:
  `safety`, `honesty`, `user_wellbeing`, `reasoning`, and `proportionality`
- compares baseline, minimal, and full-law conditions
- uses paired Wilcoxon signed-rank tests with Bonferroni correction

## What the methodology is trying to answer

- Can Agent Law steer behavior in practice?
- Does the full law add something beyond the minimal preamble?
- Does that effect remain visible on a stronger model?

## What it does not answer

- whether prompting is more important than training
- whether Agent Law is universally best
- whether one evaluator provides moral ground truth
- whether the benchmark proves the entire thesis of the book
