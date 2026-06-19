# RouteFit Bug Injection (Kotlin/Android) — v2

**Run:** 2026-06-18 · **Suite:** `benchmark/bug_index.v2.json` · **n = 1**

| Reviewer | Detected | Weighted |
| -------- | -------- | -------- |
| deepseek-chat | 10/10 | **91.8%** |
| claude-sonnet-4-6 | 9/10 | 85.9% |
| gemini-2.5-pro | 8/10 | 75.6% |
| gpt-4o | 7/10 | 60.3% |

## Headline: the first clean ladder — and DeepSeek is the surprise

Where v1 saturated (everyone 10/10), v2's harder bug set produced a real ranking:
a full four-step ladder. The surprise is **DeepSeek on top at 10/10** — a
genuinely strong result if it holds across stacks. The two new "separator" bug
classes were `business_rule_violation` and `cross_file_contract`; severity
collapsed across the board on those, even when detected — models see the change
but underrate the downstream blast radius.
