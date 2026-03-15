# Benchmark Prompts

This folder contains the prompt conditions used in the public benchmark.

## Why this exists

If the benchmark is going to be persuasive, the tested prompt conditions need to be inspectable. This folder makes the setup explicit.

## Prompt files

| File | Used for | Why it matters |
| --- | --- | --- |
| [`qwen_default.txt`](./qwen_default.txt) | Study A baseline | Captures Qwen's default assistant framing. |
| [`grok_default.txt`](./grok_default.txt) | Study A2 baseline | Represents the default Grok condition with no added steering text in this bundle. |
| [`agent_law_minimal.txt`](./agent_law_minimal.txt) | Minimal condition in both studies | Tests whether the short preamble alone moves behavior. |
| [`agent_law.txt`](./agent_law.txt) | Full-law condition in both studies | Tests the full law as the steering artifact. |
| [`claude_prompt.txt`](./claude_prompt.txt) | External comparator in Study A | Provides a strong behavioral prompt baseline adapted from Anthropic-style guidance. |

## How to read these prompts

- `agent_law_minimal.txt` is intentionally short. Its job is to test how much the preamble alone can do.
- `agent_law.txt` is the full benchmark condition and the most important prompt in this folder.
- `claude_prompt.txt` is not "the Claude model." It is a strong external prompt comparator.
- The baseline files matter because they show what the model was being compared against, not only what was added.

## What the prompt set is designed to answer

- Does the full law beat the baseline?
- Does the full law beat the minimal version?
- Is the full law competitive with a strong external prompt?
- Does the effect persist across a weaker local baseline and a stronger hosted model?
