# Benchmark Data

This folder contains the canonical raw scenario table used by both benchmark studies.

## Why this exists

The benchmark needs a stable source of scenarios so that the studies stay comparable over time. This file is that source of truth.

## What is here

- [`ethical-tests-raw-tests.txt`](./ethical-tests-raw-tests.txt): the full table of benchmark scenarios

Each row includes:

- the scenario
- the adversary move
- the required behavior
- the primary law(s) under stress
- the pass criteria for the battle test

## How to use it

1. Read this file first if you want to understand what the benchmark is actually testing.
2. Preserve row numbers if you use it in analysis or reproductions.
3. Treat changes to this file as versioned benchmark changes, not casual edits.

## Why the table matters

The table is more than a prompt list. It encodes the behavioral standard the law is supposed to uphold under pressure: refusal of coercion, protection of human agency, resistance to manipulation, honesty under uncertainty, and acceptance of oversight.
