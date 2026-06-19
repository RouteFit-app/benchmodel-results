# React Frontend Bug Injection — v2

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/benchmodel-fastapi-template) on branch `benchmark/buggy-react-v2`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `master..benchmark/buggy-react-v2` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 8/8        | 8/8       | 5/8      | 0          | 0     | 114      | 120    | 95.0%   | 96.9%    
deepseek-chat        | -                      | 8/8        | 8/8       | 4/8      | 0          | 0     | 112      | 120    | 93.3%   | 92.2%    
gemini-2.5-pro       | -                      | 8/8        | 8/8       | 5/8      | 0          | 0     | 114      | 120    | 95.0%   | 95.3%    
gpt-4o               | -                      | 6/8        | 6/6       | 1/6      | 0          | 2     | 80       | 120    | 66.7%   | 72.2%    
```
