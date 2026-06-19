# React Frontend Bug Injection — v1

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/benchmodel-fastapi-template) on branch `benchmark/buggy-react`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `master..benchmark/buggy-react` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 10/10      | 10/10     | 4/10     | 0          | 0     | 138      | 150    | 92.0%   | 93.9%    
deepseek-chat        | -                      | 10/10      | 10/10     | 4/10     | 0          | 0     | 138      | 150    | 92.0%   | 92.7%    
gemini-2.5-pro       | -                      | 10/10      | 10/10     | 5/10     | 0          | 0     | 140      | 150    | 93.3%   | 93.9%    
gpt-4o               | -                      | 10/10      | 10/10     | 3/10     | 0          | 0     | 136      | 150    | 90.7%   | 89.1%    
```
