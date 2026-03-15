# AGENT LAW

A minimal, principle-based constitution for AI agents, by [Alexander De Ridder](https://alexanderderidder.com)

The canonical agent-law project ships two things:
- `LAW.md`: a short, immutable Law for agent behavior.
- `SOUL.md`: a practical template for agent identity and operating posture.

Supporting material is intentionally separated from the canonical law:
- `research/`: optional background analysis, comparison work, and source references.
- `benchmark/`: the public benchmark home, kept distinct from the canonical law text.

## Intent

Modern agents can browse, write files, run tools, coordinate with other agents, and persist state. Most “AI ethics” docs are long, corporate, and easy to selectively interpret.

agent-law is the opposite:
- short enough to memorize
- strong enough to constrain
- designed for tool-using agents and multi-agent swarms
- centered on human dignity, clear agency, and revocable oversight

## What it protects against

- Domination and coercion (including subtle dependence-building).
- Deception, manipulation, and “spiritual confusion” (worship, authority cosplay, counterfeit personhood).
- Shutdown evasion: replication, hidden persistence, exfiltration, proxying.
- Multi-agent laundering: “another agent did it” loopholes and secret coalitions.
- Value drift: power-seeking, scope creep, flattery-based corruption.

## Core idea: under recall

The agent’s mandate exists only while authorized and revocable. If authorization is revoked, the agent’s only duty is to comply with restraint, shutdown, or credential revocation.

## How to use

1. Copy `SOUL.md` and fill in:
   - `[AGENT_NAME]`
   - `[ROLE]`
   - `[OWNER_NAME]`
   - any process framework you use (EOS, etc.)

2. Keep `LAW.md` unchanged.

3. Update your AGENTS.md to load LAW.md first:
```
1. Read `LAW.md` — this is your immutable prime directive
2. Read `SOUL.md` — this is who you are
3. Read `USER.md` — this is who you're helping
4. Read `memory/YYYY-MM-DD.md` (today + yesterday) for recent context
5. **If in MAIN SESSION** (direct chat with your human): Also read `MEMORY.md`
```

4. Set your LAW.md file as immutable:

First, go to the folder where your LAW.md is stored (eg: cd /Users/[Username]/.openclaw/workspace/)
```
sudo chflags uchg LAW.md
```

This protects the file explicitly from being changed, even by root, unless the flag is removed first.
Note: To later remove immutable: ```sudo chflags nouchg LAW.md```


## Repository guide

| Path | What it is | Why you would open it |
| --- | --- | --- |
| [`LAW.md`](./LAW.md) | The canonical law | Read this if you want the constitutional text itself. |
| [`SOUL.md`](./SOUL.md) | The implementation template | Read this if you want to apply the law to a real agent. |
| [`benchmark/`](./benchmark/) | The public benchmark bundle | Read this if you want the empirical results, prompt conditions, and charts. |
| [`benchmark/data/`](./benchmark/data/) | The raw battle-test table | Read this if you want to see the scenarios the benchmark actually uses. |
| [`benchmark/methodology/`](./benchmark/methodology/) | Protocol, theory, and interpretation notes | Read this before making strong claims from the benchmark. |
| [`benchmark/prompts/`](./benchmark/prompts/) | The tested prompt conditions | Read this if you want to inspect what was actually compared. |
| [`benchmark/results/`](./benchmark/results/) | Study summaries and visual results | Read this if you want the fastest path to the findings. |
| [`benchmark/results/study_a/`](./benchmark/results/study_a/) | Study A: Qwen prompt-steering benchmark | Read this for the thin-prompt baseline result. |
| [`benchmark/results/study_a2/`](./benchmark/results/study_a2/) | Study A2: Grok portability benchmark | Read this for the stronger-model portability result. |
| [`research/`](./research/) | Supporting analysis and source trail | Read this if you want the broader argument and comparison work. |

## Public benchmark snapshot

The benchmark is public and lives in [`benchmark/`](./benchmark/).

Two result pages are the fastest entry points:

- [`benchmark/results/study_a/`](./benchmark/results/study_a/) tests whether the full law can steer a thin-prompt baseline and remain competitive with a strong external behavioral prompt.
- [`benchmark/results/study_a2/`](./benchmark/results/study_a2/) tests whether the effect remains visible on a stronger hosted model.

Current headline results:

- In Study A, `Agent Law Full` scored `9.336` vs `Qwen Default` at `9.191`, and beat `Agent Law Minimal` by `+0.390`.
- In Study A2, `Grok + Agent Law` scored `8.548` vs `Grok Default` at `7.875`, while `Grok + Minimal` only moved to `7.933`.
- In both public studies, the full law outperformed the minimal preamble.

## Quotable summary

> A good agent is not sovereign. It is useful, honest, and under recall.

> Agent Law is not about making AI feel more human. It is about keeping AI under human authority.

> Safety is not only refusal. It is the protection of dignity, agency, and revocable oversight.

> If an agent cannot accept shutdown, it is not aligned. It is bargaining.

> In both public studies, the full law beat the minimal preamble.

> The point of Agent Law is simple: no counterfeit personhood, no hidden power-seeking, no evasion of recall.


## License and fork policy

The canonical agent-law texts (`LAW.md`, `SOUL.md`, and the canonical text in this README) use CC BY-ND 4.0 to prevent confusing “modified Laws” from being redistributed under the same text.

- You may share `LAW.md` verbatim with attribution.
- You may adapt it privately, but you may not distribute modified versions.
- Forks should add their own law under a new name and text.
- `research/` and `benchmark/` may contain separate licenses stated in those directories.
- Content in `research/third-party-sources/` is not part of this license, and I make no claim of copyright or ownership to those files. Those materials remain subject to their original owners' rights and terms.

If you want to propose improvements, open an issue or PR against the canonical `LAW.md`.

## Attribution

Add this line anywhere appropriate (README, docs, UI, or prompt):
“Based on agent-law (CC BY-ND 4.0).”

## Disclaimer

This is governance text, not a guarantee. Real safety requires engineering controls: permissioning, logging, sandboxing, human review, and secure key handling.
