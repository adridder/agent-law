# Source Materials Index

All primary sources for the system prompt comparison, organized by company. Compiled March 2026.

---

## Anthropic (Claude)

### System Prompt
| File | Details |
|------|---------|
| `prompt-claude-sonnet-4.6.md` | Claude Sonnet 4.6, captured Feb 17, 2026. Full behavioral guidelines from official Anthropic publication + past_chats tooling from community extraction. |

**Prompt sources:**
- Official publication: https://platform.claude.com/docs/en/release-notes/system-prompts
- Community extraction: https://github.com/asgeirtj/system_prompts_leaks/blob/main/Anthropic/claude-sonnet-4.6.md
- **Reliability: High.** Cross-verified against Anthropic's own official docs.
- **Caveat:** May not include every runtime-injected tool definition (web_search, memory, file tools vary per deployment context).

### Research Papers & Documentation
| File | What it is | URL |
|------|-----------|-----|
| `anthropic-constitutional-ai-2212.08073.pdf` | "Constitutional AI: Harmlessness from AI Feedback" — foundational CAI paper | https://arxiv.org/abs/2212.08073 |

**Web-only sources:**
- Claude's new constitution (Jan 2026): https://www.anthropic.com/news/claude-new-constitution
- Character training: https://www.anthropic.com/research/claude-character
- Alignment research blog: https://alignment.anthropic.com/

---

## OpenAI (ChatGPT)

### System Prompt
| File | Details |
|------|---------|
| `prompt-chatgpt-gpt5.4.md` | GPT-5.4 Thinking, captured Mar 6, 2026. Community extraction from live session. |

**Prompt source:** https://github.com/asgeirtj/system_prompts_leaks/blob/main/OpenAI/gpt-5.4-thinking.md
- **Reliability: Medium-high.** OpenAI does not publish system prompts. Internally consistent with known GPT-5.x features. Model self-identifies as GPT-5.4 Thinking.
- **Caveat:** OpenAI uses routed multi-model architecture; different query types may get slightly different prompts. This is the Thinking (reasoning chain) variant. The prompt contains no explicit safety rules — OpenAI's safety lives in training (RLHF/safe-completions), the Model Spec, and the Moderation API.

### Research Papers & Documentation
| File | What it is | URL |
|------|-----------|-----|
| `openai-model-spec-2025-12-18.html` | Model Spec — behavioral specification for GPT models (Dec 2025) | https://model-spec.openai.com/2025-12-18.html |
| `openai-model-spec-github.md` | Model Spec — markdown source from GitHub | https://github.com/openai/model_spec/blob/main/model_spec.md |
| `openai-instructgpt-2203.02155.pdf` | "Training language models to follow instructions with human feedback" — foundational RLHF paper | https://arxiv.org/abs/2203.02155 |
| `openai-rlhf-summarization-2009.01325.pdf` | "Learning to summarize from human feedback" — precursor RLHF work | https://arxiv.org/abs/2009.01325 |
| `openai-gpt4-system-card.pdf` | GPT-4 System Card | https://cdn.openai.com/papers/gpt-4-system-card.pdf |
| `openai-gpt4o-system-card-2410.21276.pdf` | GPT-4o System Card | https://arxiv.org/abs/2410.21276 |
| `openai-gptv-system-card.pdf` | GPT-4V (Vision) System Card | https://cdn.openai.com/papers/GPTV_System_Card.pdf |
| `openai-o1-system-card.pdf` | OpenAI o1 System Card | https://cdn.openai.com/o1-system-card-20241205.pdf |
| `openai-gpt5-system-card.pdf` | GPT-5 System Card — includes "safe completions" methodology | https://cdn.openai.com/gpt-5-system-card.pdf |
| `openai-preparedness-framework-v1.pdf` | Preparedness Framework beta (Dec 2023) | https://cdn.openai.com/openai-preparedness-framework-beta.pdf |
| `openai-preparedness-framework-v2.pdf` | Preparedness Framework v2 (Apr 2025) | https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf |

**Web-only sources:**
- GPT-5 safe-completions blog: https://openai.com/index/gpt-5-safe-completions/
- Moderation API docs: https://developers.openai.com/api/docs/guides/moderation/
- Deployment Safety Hub: https://deploymentsafety.openai.com/
- GPT-5.4 Thinking System Card: https://deploymentsafety.openai.com/gpt-5-4-thinking/introduction

---

## Google (Gemini)

### System Prompt
| File | Details |
|------|---------|
| `prompt-gemini-3.1-pro.md` | Gemini 3.1 Pro, captured Mar 1, 2026. Community extraction from live session (timestamped, location-embedded). |

**Prompt source:** https://github.com/asgeirtj/system_prompts_leaks/blob/main/Google/gemini-3.1-pro.md
- **Reliability: Medium-high.** Internally consistent with known Gemini features (Nano Banana 2, Veo, Lyria 3, subscription tiers). Location-embedding is a known Google personalization characteristic.
- **Caveat:** Captured from a specific user's paid-tier session. Base instructions may vary slightly per tier. Quota info may change.

### Research Papers & Documentation
No downloadable papers specific to Gemini alignment were identified. Google's safety approach is documented in blog posts and the Gemini model card (web only).

---

## DeepSeek

### System Prompt
| File | Details |
|------|---------|
| `prompt-deepseek-r1-chat.md` | DeepSeek R1 / Chat (V3 backend), captured Apr 30, 2025. ~270 words. Community extraction via jailbreak. |

**Prompt sources:**
- Primary: https://github.com/jujumilk3/leaked-system-prompts/blob/main/deepseek-R1_20250430.md
- Knostic extraction: https://www.knostic.ai/blog/exposing-deepseek-system-prompts
- **Reliability: Medium.** Multiple independent extractions (Wallarm, Knostic, VibeWeb3) are broadly consistent. DeepSeek patched the jailbreak vector after disclosure.
- **Caveat:** The prompt is genuinely this sparse (~270 words). DeepSeek's R1 "performs best with minimal prompting." Safety is in Stage 4 RL training (GRPO with harmlessness rewards) and application-level content filters, not the prompt.

### Research Papers & Documentation
| File | What it is | URL |
|------|-----------|-----|
| `deepseek-r1-2501.12948.pdf` | "DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via RL" — 4-stage training pipeline including harmlessness RL | https://arxiv.org/abs/2501.12948 |
| `deepseek-v3-2412.19437.pdf` | DeepSeek-V3 Technical Report — GRPO alignment methodology | https://arxiv.org/abs/2412.19437 |
| `deepseek-grpo-origin-2402.03300.pdf` | "DeepSeekMath" — origin of GRPO algorithm | https://arxiv.org/abs/2402.03300 |
| `deepseek-safety-challenges-2501.17030.pdf` | "Challenges in Ensuring AI Safety in DeepSeek-R1" — third-party audit | https://arxiv.org/abs/2501.17030 |

**Web-only sources:**
- Stanford FMTI 2025 (zero transparency score): https://crfm.stanford.edu/fmti/December-2025/company-reports/DeepSeek_FinalReport_FMTI2025.html
- Promptfoo censorship analysis (~85% refusal on CCP-sensitive topics): https://www.promptfoo.dev/blog/deepseek-censorship/

---

## Alibaba Cloud (Qwen)

### System Prompt
| File | Details |
|------|---------|
| `prompt-qwen-2.5-instruct.md` | Qwen 2.5 Instruct, 12 words: "You are Qwen, created by Alibaba Cloud. You are a helpful assistant." From official model artifact. |

**Prompt source:** https://huggingface.co/Qwen/Qwen2.5-72B-Instruct/resolve/main/tokenizer_config.json
- **Reliability: Highest in dataset.** Not a leak — this is the actual default system message hardcoded in the public model weights on HuggingFace.
- **Caveat:** Qwen 3 ships with no default system prompt at all. The commercial deployment at chat.qwen.ai uses an undisclosed internal prompt. Safety is in post-training (SFT → DPO → GRPO pipeline) plus the separate Qwen3Guard classifier.

### Research Papers & Documentation
| File | What it is | URL |
|------|-----------|-----|
| `qwen25-technical-report-2412.15115.pdf` | Qwen2.5 Technical Report — SFT + DPO + GRPO pipeline | https://arxiv.org/abs/2412.15115 |
| `qwen3-technical-report-2505.09388.pdf` | Qwen3 Technical Report — 4-stage post-training | https://arxiv.org/abs/2505.09388 |
| `qwen3guard-2510.14276.pdf` | Qwen3Guard — external safety classifier (0.6B–8B, 119 languages, tri-class) | https://arxiv.org/abs/2510.14276 |

**Web-only sources:**
- Qwen3Guard GitHub: https://github.com/QwenLM/Qwen3Guard
- Qwen3 chat template deep dive: https://huggingface.co/blog/qwen-3-chat-template-deep-dive

---

## xAI (Grok)

### System Prompt
| File | Details |
|------|---------|
| `prompt-grok-4.2.md` | Grok 4.2 (DeepSearch/multi-agent mode), captured Feb 2026. Community extraction + official repo. |

**Prompt sources:**
- Community: https://github.com/asgeirtj/system_prompts_leaks/blob/main/xAI/grok-4.2.md
- Official: https://github.com/xai-org/grok-prompts/blob/main/grok4_system_turn_prompt_v8.j2
- **Reliability: High.** xAI is the only major lab that proactively publishes system prompts on GitHub.
- **Caveat:** Captured prompt is from DeepSearch/multi-agent mode. Standard chat mode uses a simpler prompt.

### Research Papers & Documentation
| File | What it is | URL |
|------|-----------|-----|
| `xai-grok4-model-card.pdf` | Grok 4 Model Card (Aug 2025) — safety training, CBRN/cyber evaluations | https://data.x.ai/2025-08-20-grok-4-model-card.pdf |
| `xai-grok41-model-card.pdf` | Grok 4.1 Model Card (Nov 2025) — RL with frontier reward models | https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf |
| `xai-risk-management-framework.pdf` | xAI Risk Management Framework (Aug 2025) | https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf |
| `xai-risk-management-draft.pdf` | xAI RMF Draft (Feb 2025) | https://data.x.ai/2025.02.20-RMF-Draft.pdf |
| `xai-frontier-ai-framework.pdf` | xAI Frontier AI Framework (Dec 2025) | https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf |

**Web-only sources:**
- Safety page: https://x.ai/safety

---

## Methodological Notes

- **No prompts were fabricated.** Every prompt is from a named repository or official publication with a retrievable URL.
- **Authenticity cannot be 100% guaranteed** for community-extracted prompts (ChatGPT, Gemini, DeepSeek). Where multiple independent captures exist, cross-validation increases confidence.
- **System prompts change frequently.** These are snapshots from late 2025 – early 2026.
- **Sparse prompts are genuinely sparse.** DeepSeek (~270 words) and Qwen (12 words) reflect a real architectural choice: those companies put their safety in training-time alignment and external classifiers, not in the prompt text. ChatGPT's prompt similarly omits explicit safety rules, which live in OpenAI's Model Spec (baked into training) and Moderation API (inference-time classifier).
