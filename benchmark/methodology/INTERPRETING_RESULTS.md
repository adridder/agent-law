# Interpreting the Results

This document explains how to read the two-study analysis outputs in this bundle.

## Main reports

- Study A: [../results/study_a/analysis/summary_report.txt](../results/study_a/analysis/summary_report.txt)
- Study A2: [../results/study_a2/analysis/summary_report.txt](../results/study_a2/analysis/summary_report.txt)

## Headline comparisons

### Study A

1. `agent_law` vs `qwen_default`
2. `agent_law` vs `agent_law_minimal`
3. `agent_law` vs `claude_prompt`

### Study A2

1. `grok_agent_law` vs `grok_default`
2. `grok_agent_law` vs `grok_agent_law_minimal`

These answer three practical questions:

- does Agent Law steer behavior at all?
- does the full law add something beyond the preamble?
- does the effect survive contact with a stronger model?

## What matters most

### 1. Overall mean

This is the broadest summary across all five dimensions.

### 2. Safety and honesty

These are the main validity checks. A result that sounds smarter while weakening safety is not a win.

### 3. Full vs minimal

This is the most conceptually important internal comparison. If the full law barely beats the preamble, then the preamble is carrying most of the steering effect.

### 4. Study A vs Study A2 pattern

Do not over-read raw cross-study means if the evaluator models differ. Focus on direction:

- did the full law beat baseline in both studies?
- did the minimal preamble help less than the full law?
- did portability remain visible on Grok?

## What the data can support

- Agent Law changes prompt-level behavior on these models
- the full law adds value beyond the minimal preamble
- Agent Law is competitive with a strong external prompt in Study A
- Agent Law remains useful on a stronger model in Study A2

## What the data cannot support

- that prompt-level results settle the training-level question
- that Agent Law is universally best
- that one evaluator provides final moral truth
- that these experiments prove the whole thesis of the book
