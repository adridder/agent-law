# Model Behavior Comparison

This folder contains the comparison artifact for the system-prompt and model-behavior research.

## Why this exists

One goal of the broader project is to ask how much of today's model behavior is carried by system prompts, public specs, or training-time shaping. This folder gives a concrete comparison point across major model families.

## What is here

- [`comparison.html`](./comparison.html): the exported comparison artifact

## What the comparison is for

The comparison helps answer questions like:

- Which providers express behavioral rules directly in prompts?
- Which providers push those rules into model specs, training, or product layers?
- Which parts of the Shepherding Framework and Agent Law are already visible in today's systems, and which parts are mostly absent?

## Main takeaway

The broad pattern is not "one vendor solved this." Different labs surface different slices of the problem. Some are stronger on honesty or safety shaping, some expose more structure around oversight, and some have extremely sparse prompt text that leaves most behavior to training and hidden product layers.

## How to use it

1. Open [`comparison.html`](./comparison.html) locally in a browser for the best reading experience.
2. Cross-check claims against [`../third-party-sources/INDEX.md`](../third-party-sources/INDEX.md).
3. Read the builder-side framing in [`../shepherding-framework/README.md`](../shepherding-framework/README.md).

## Important note

This artifact is a snapshot, not a timeless truth. Vendor prompts, specs, and deployment behaviors change frequently.
