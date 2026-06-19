# RouteFit Bug Injection — v2

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/routefit) on branch `benchmark/buggy-v2`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `main..benchmark/buggy-v2` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 9/10       | 9/9       | 7/9      | 0          | 0     | 131      | 150    | 87.3%   | 85.9%    
deepseek-chat        | -                      | 10/10      | 10/10     | 4/10     | 0          | 0     | 138      | 150    | 92.0%   | 91.8%    
gemini-2.5-pro       | -                      | 8/10       | 8/8       | 4/8      | 0          | 0     | 112      | 150    | 74.7%   | 75.6%    
gpt-4o               | -                      | 7/10       | 7/7       | 4/7      | 1          | 0     | 97       | 150    | 64.7%   | 60.3%    
```
