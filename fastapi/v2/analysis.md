# FastAPI Full-Stack Bug Injection (Python) — v2

**Run:** 2026-06-18 · **Suite:** `suites/fastapi-fullstack/bug_index.v2.json` · **n = 1**

| Reviewer | Detected | Severity acc. | Weighted |
| -------- | -------- | ------------- | -------- |
| claude-sonnet-4-6 | 10/10 | 70% | high |
| deepseek-chat | 10/10 | 70% | high |
| gemini-2.5-pro | 9/10 | 89% | mid |
| gpt-4o | 7/10 | 43% | low |

## Headline: top two tie, GPT bottom on detection *and* severity

Claude and DeepSeek both swept 10/10; Gemini missed one; GPT missed three high-
severity bugs and labeled severity correctly less than half the time. The two
hard additions — `mass_assignment` (a self-PATCH to `is_superuser`) and
`orm_data_bleed` (an inverted cascade filter) — are the kind of cross-layer
security logic where weaker reviewers fall off.
