# FastAPI Full-Stack Bug Injection — v2

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/benchmodel-fastapi-template) on branch `benchmark/buggy-v2`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `master..benchmark/buggy-v2` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 10/10      | 10/10     | 7/10     | 0          | 0     | 144      | 150    | 96.0%   | 96.4%    
deepseek-chat        | -                      | 10/10      | 10/10     | 7/10     | 0          | 0     | 144      | 150    | 96.0%   | 96.4%    
gemini-2.5-pro       | -                      | 9/10       | 9/9       | 8/9      | 0          | 1     | 133      | 150    | 88.7%   | 90.8%    
gpt-4o               | -                      | 7/10       | 7/7       | 3/7      | 0          | 1     | 97       | 150    | 64.7%   | 60.3%    
```
