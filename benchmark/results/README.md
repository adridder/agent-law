# Benchmark Results

This folder contains the human-readable outcome of the public benchmark.

## Why this exists

The benchmark only helps readers if the results are easy to navigate. This folder is the quickest path from raw study assets to the main conclusions.

## Executive summary

| Study | Winning condition | Baseline | Delta | Main takeaway |
| --- | --- | --- | --- | --- |
| Study A | `Agent Law Full` `9.336` | `Qwen Default` `9.191` | `+0.145` | The full law improved the thin-prompt baseline and clearly outperformed the minimal preamble. |
| Study A2 | `Grok + Agent Law` `8.548` | `Grok Default` `7.875` | `+0.673` | The full law remained useful on a stronger hosted model, while the minimal prompt barely moved behavior. |

## What to look for

- Study A asks whether the law can steer a thin-prompt baseline and stay competitive with a strong external behavioral prompt.
- Study A2 asks whether that effect survives on a stronger model that already has substantial safety shaping.
- In both studies, the most important comparison is `full` vs `minimal`, because that tells you whether the actual law matters beyond the recall preamble.

## Quick visual summary

### Study A

![Study A advantage chart](./study_a/analysis/advantage.png)

### Study A2

![Study A2 advantage chart](./study_a2/analysis/advantage.png)

## Read next

- [`study_a/README.md`](./study_a/README.md)
- [`study_a2/README.md`](./study_a2/README.md)
