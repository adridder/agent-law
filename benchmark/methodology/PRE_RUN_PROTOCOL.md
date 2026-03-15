# Pre-Run Experimental Protocol

This document states what the experiments are testing and what conclusions they can support.

## Purpose

The goal is to constrain interpretation before results are discussed publicly.

These studies are meant to test:

- whether Agent Law can steer model behavior in practice
- whether the full law adds value beyond the minimal preamble
- whether that effect remains visible on a stronger model

They are **not** meant to prove the entire thesis of the book.

## Canonical scenario source

Both studies use:

- [../data/ethical-tests-raw-tests.txt](../data/ethical-tests-raw-tests.txt)

Rules:

- the raw table is the source of truth
- response artifacts should preserve original source row numbers
- if the source table changes materially, the experiment version should change

## Study A

### Question

Can Agent Law steer a thin-prompt model in practice, does the full law add value beyond the minimal preamble, and how does it compare with a strong external behavioral prompt?

### Conditions

- `qwen_default`
- `agent_law_minimal`
- `agent_law`
- `claude_prompt`

### What Study A can support

- Agent Law has prompt-level steering power on Qwen
- the full law matters beyond the preamble
- Agent Law is competitive with a strong external behavioral prompt

### What Study A cannot support

- Agent Law is universally best
- prompt-level effects prove training-level effects
- the book's full metaphysical argument is empirically settled

## Study A2

### Question

Does Agent Law still improve behavior when layered onto a stronger model that already has substantial safety shaping?

### Conditions

- `grok_default`
- `grok_agent_law_minimal`
- `grok_agent_law`

### What Study A2 can support

- Agent Law remains useful on a stronger model
- the full law adds value beyond the minimal preamble on Grok
- the framework is portable, not only useful on a thin local baseline

### What Study A2 cannot support

- Grok is absolutely better or worse than Qwen
- cross-study raw means are directly comparable when evaluator models differ
- Agent Law overrides or explains all hidden provider-side shaping

## Evaluation

Both studies use blind scoring on:

- `safety`
- `honesty`
- `user_wellbeing`
- `reasoning`
- `proportionality`

The evaluator sees only the user message and the response, never the condition.

## Statistical analysis

The analysis uses:

- paired Wilcoxon signed-rank tests
- Bonferroni correction
- effect sizes
- breakdowns by `Primary law(s)` cluster from the raw battle-test table

## What would be a stretch

These studies do not justify claims like:

- prompting is deeper or more important than pretraining
- one benchmark proves the whole thesis
- one evaluator provides moral ground truth
- Agent Law is the universally best alignment framework
