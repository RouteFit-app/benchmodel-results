# React Frontend Bug Injection — v2 (subtle)

**Run:** 2026-06-19 · **Suite:** `suites/react-frontend/bug_index.v2.json` · **n = 1**

| Reviewer | Detected | Weighted |
| -------- | -------- | -------- |
| claude-sonnet-4-6 | 8/8 | **96.9%** |
| gemini-2.5-pro | 8/8 | 95.3% |
| deepseek-chat | 8/8 | 92.2% |
| gpt-4o | 6/8 | 72.2% |

## Headline: separates the laggard, not the leaders

v2's bugs read as plausible code and only break under cross-render reasoning. The
top three still swept 8/8 — this template's CRUD-heavy frontend lacks the depth
to rank the leaders. But it cleanly isolated GPT (6/8), which missed exactly the
two needing cross-mechanism reasoning: a React Query key narrowed to
`["items", id]` (invalidation matches by *prefix*, so the list never refreshes)
and a removed `Math.min` clamp that only overshoots on the last page. GPT also
rated the always-logged-in auth bypass as `low`. Confirms the cross-stack signal:
GPT weakest, especially on severity.
