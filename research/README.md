# Research

This folder holds the supporting research around `agent-law`. It is intentionally separate from the canonical law so readers can adopt the law without needing to adopt every supporting argument, source archive, or comparison artifact.

## Why this exists

The law is short on purpose. The research folder is where the longer context lives: how the framework compares with current model behavior, what builder-side principles sit behind it, and which third-party materials support the analysis.

## What is in this folder

| Folder | What it contains | Why it matters |
| --- | --- | --- |
| [`model-behavior-comparison/`](./model-behavior-comparison/) | Exported comparison artifact | Situates Agent Law against current vendor prompts and specs. |
| [`shepherding-framework/`](./shepherding-framework/) | Builder-facing principles and coverage analysis | Explains the builder-side obligations that sit behind the law. |
| [`third-party-sources/`](./third-party-sources/) | Source index and archived references | Makes the research traceable. |

## How to use this folder

1. Start with [`shepherding-framework/README.md`](./shepherding-framework/README.md) if you want the conceptual argument.
2. Open [`model-behavior-comparison/README.md`](./model-behavior-comparison/README.md) if you want the market comparison.
3. Use [`third-party-sources/README.md`](./third-party-sources/README.md) when you need provenance and source material.

## Main takeaway

The research points to a gap the law is trying to fill: current systems often express some safety and honesty norms, but they are much less consistent on anti-dependence, anti-counterfeit personhood, revocable authority, and builder responsibility.

## License scope

- Unless otherwise noted, original prose in `research/` is licensed under [`LICENSE.md`](./LICENSE.md).
- Files in [`third-party-sources/`](./third-party-sources/) are not covered by that license.
