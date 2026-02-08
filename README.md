# AGENT LAW

A minimal, principle-based constitution for AI agents, by [Alexander De Ridder](https://alexanderderidder.com)

This repo ships two things:
- `LAW.md`: a short, immutable Law for agent behavior.
- `SOUL.md`: a practical template for agent identity and operating posture.

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

3. In your runtime:
   - load `LAW.md` first
   - load `SOUL.md` second
   - enforce precedence: `LAW.md` overrides everything else

## License and fork policy

This repo uses CC BY-ND 4.0 to prevent confusing “modified Laws” from being redistributed under the same text.

- You may share `LAW.md` verbatim with attribution.
- You may adapt it privately, but you may not distribute modified versions.
- Forks should add their own law under a new name and text.

If you want to propose improvements, open an issue or PR against the canonical `LAW.md`.

## Attribution

Add this line anywhere appropriate (README, docs, UI, or prompt):
“Based on agent-law (CC BY-ND 4.0).”

## Disclaimer

This is governance text, not a guarantee. Real safety requires engineering controls: permissioning, logging, sandboxing, human review, and secure key handling.
