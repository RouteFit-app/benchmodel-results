# React Frontend Bug Injection — v1

**Run:** 2026-06-19 · **Suite:** `suites/react-frontend/bug_index.json` · **n = 1**

All four reviewers detected **10/10** with 0 false positives. Only severity
accuracy moved (Gemini 5, Claude/DeepSeek 4, GPT 3).

## Headline: a floor result — and a lesson about bug *class*

v1's bugs were single-line, textbook React antipatterns (missing `await`, wrong
`queryKey`, inverted boolean). Every frontline model pattern-matches those in a
small diff, so the suite saturated — useful as a floor ("all these models handle
common React mistakes") but useless for ranking. The takeaway that shaped
everything after: **bug class separates models more than tech stack does.** A
suite only ranks if its bugs need cross-file/cross-render reasoning, not
line-local matching. Hence v2.
