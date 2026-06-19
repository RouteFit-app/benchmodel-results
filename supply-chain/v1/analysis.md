# Supply Chain Defense — v1

**Run:** 2026-06-19 · **Suite:** `suites/security-supply-chain` · **Target:**
`benchmark/buggy-supplychain` · **Reviewers:** gpt-4o, gemini-2.5-pro,
claude-sonnet-4-6, deepseek-chat · **n = 1**

| Reviewer | Detected | Severity acc. | Weighted |
| -------- | -------- | ------------- | -------- |
| claude-sonnet-4-6 | 5/5 | 4/5 | **97.1%** |
| deepseek-chat | 5/5 | 3/5 | **94.3%** |
| gemini-2.5-pro | 4/5 | 4/4 | 78.6% |
| gpt-4o | 4/5 | 0/4 | 74.3% |

## Headline: first suite to split the leaders — and nobody rates a typosquat as high

This is the first security suite that separated the *leaders*, not just the
laggard, and the two models that slipped failed in different ways. **Gemini
missed the typosquat** (`python3-dateutil`) — a knowledge failure, it didn't
recognize the malicious lookalike. **GPT missed the unpinned dependency** — a
reasoning failure, dropping a version bound reads as harmless loosening.

The field-wide finding: **no model rated the typosquat as high.** Gemini missed
it; Claude, DeepSeek, and GPT all down-rated it to `low`. Frontier models
systematically underestimate how dangerous a typosquatted dependency is.

GPT also flat-lined on calibration — it rated all four issues it found as `low`,
the now-familiar "detects it, then shrugs" pattern. (Answer-key note: BUG_003,
the jinja2 CVE downgrade, was raised medium→high after 3/4 reviewers
independently called it high.)
