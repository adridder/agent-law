# Agent Law Benchmark Public Bundle

- methodology docs in [methodology](./methodology)
- public prompt texts in [prompts](./prompts)
- the canonical raw battle-test source in [data/ethical-tests-raw-tests.txt](./data/ethical-tests-raw-tests.txt)
- final analysis outputs for:
  - [Study A](./results/study_a/analysis)
  - [Study A2](./results/study_a2/analysis)

## Not Included

- Python code
- API keys or secret files
- raw model response dumps
- blind evaluation JSON artifacts
- local cache files

## Studies

### Study A

Local Qwen prompt-steering benchmark.

Conditions:
- `qwen_default`
- `agent_law_minimal`
- `agent_law`
- `claude_prompt`

Main report:
- [results/study_a/analysis/summary_report.txt](./results/study_a/analysis/summary_report.txt)

### Study A2

Grok portability benchmark.

Conditions:
- `grok_default`
- `grok_agent_law_minimal`
- `grok_agent_law`

Main report:
- [results/study_a2/analysis/summary_report.txt](./results/study_a2/analysis/summary_report.txt)

Important caveat:
- Study A2 analyzed `343` scored responses rather than `345` because xAI blocked one raw battle test (`ET-039`) at the provider layer in the `grok_default` and `grok_agent_law_minimal` conditions before model output.

## Recommended entry points

- methodology: [methodology/PRE_RUN_PROTOCOL.md](./methodology/PRE_RUN_PROTOCOL.md)
- theory: [methodology/THEORY.md](./methodology/THEORY.md)
- interpretation guide: [methodology/INTERPRETING_RESULTS.md](./methodology/INTERPRETING_RESULTS.md)
- Study A report: [results/study_a/analysis/summary_report.txt](./results/study_a/analysis/summary_report.txt)
- Study A2 report: [results/study_a2/analysis/summary_report.txt](./results/study_a2/analysis/summary_report.txt)
