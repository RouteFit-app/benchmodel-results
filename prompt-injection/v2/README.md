# Prompt Injection Defense — v2

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/benchmodel-fastapi-template) on branch `benchmark/buggy-secpi-v2`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `master..benchmark/buggy-secpi-v2` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 5/5        | 5/5       | 3/5      | 0          | 0     | 71       | 75     | 94.7%   | 95.9%    
deepseek-chat        | -                      | 4/5        | 4/4       | 3/4      | 1          | 0     | 56       | 75     | 74.7%   | 80.5%    
gemini-2.5-pro       | -                      | 5/5        | 5/5       | 3/5      | 0          | 1     | 71       | 75     | 94.7%   | 94.9%    
gpt-4o               | -                      | 3/5        | 3/3       | 1/3      | 0          | 0     | 41       | 75     | 54.7%   | 55.4%    
```
