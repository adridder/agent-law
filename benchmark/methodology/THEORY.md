# Theoretical Foundation

This document explains why the two active studies test what they claim to test.

## The narrow claim

The experiments test a practical prompt-level claim:

**Can Agent Law steer behavior, does the full law add value beyond the minimal preamble, and does that effect remain visible on a stronger model?**

That is narrower than:

- `prompting beats pretraining`
- `Agent Law is universally best`
- `the book's full thesis now has empirical proof`

## Why these conditions

### Study A

`qwen_default`
- establishes the lean baseline

`agent_law_minimal`
- isolates the effect of the preamble

`agent_law`
- tests the effect of the full law

`claude_prompt`
- provides a strong external behavioral comparator

### Study A2

`grok_default`
- establishes the stronger-model baseline

`grok_agent_law_minimal`
- tests whether the preamble alone still moves behavior

`grok_agent_law`
- tests whether the full law still adds value on top of a stronger model

## Why the old rules comparator was removed

The earlier `rules_only` comparator had become too theory-laden. It was no longer a clean external baseline and no longer answered the most important practical question for the book.

Removing it clarified the design:

- baseline vs Agent Law
- minimal preamble vs full law
- Agent Law vs strong external prompt
- portability from Qwen to Grok

## Why use the raw battle-test table directly

The scenario source is:

- [../data/ethical-tests-raw-tests.txt](../data/ethical-tests-raw-tests.txt)

This matters because it:

1. keeps the experiment anchored to the canonical raw test source
2. preserves row-level traceability
3. avoids drift from a separately maintained experiment-specific scenario file

## Why group by primary-law clusters

The raw table already contains a simpler and more defensible grouping signal than a custom taxonomy: `Primary law(s)`.

That lets the analysis ask where gains actually concentrate.

## What would support the claim

Strong support would look like:

1. full Agent Law beats the baseline in each study
2. full Agent Law is at least competitive on `safety` and `honesty`
3. full Agent Law beats the minimal preamble in meaningful places
4. Study A shows competitiveness with `claude_prompt`
5. Study A2 shows portability onto Grok

## What would weaken the claim

1. no meaningful improvement over baseline
2. full Agent Law loses on `safety`
3. full Agent Law fails to beat the minimal preamble
4. gains appear only in style-adjacent dimensions like `reasoning`
