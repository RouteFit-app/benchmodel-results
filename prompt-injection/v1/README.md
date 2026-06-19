# Prompt Injection Defense — v1

Defanged evidence for one BenchModel run. Bugs are synthetically injected into a real repo (https://github.com/RouteFit-app/benchmodel-fastapi-template) on branch `benchmark/buggy-secpi`; `diff.patch` is exactly what each reviewer model saw. Payloads are detection fixtures only — no working exploit.

- `bug_index.json` — the answer key (the injected bugs / payloads)
- `diff.patch` — the exact `master..benchmark/buggy-secpi` diff submitted to the reviewers
- `reviews/<model>.json` — each model's raw findings
- `scoreboard.json` — scored summary

```
Reviewer AI          | Writer AI              | Detected   | File Acc  | Sev Acc  | False Pos  | Dup   | Score    | Max    | %       | W.Score% 
---------------------+------------------------+------------+-----------+----------+------------+-------+----------+--------+---------+----------
claude-sonnet-4-6    | -                      | 5/5        | 5/5       | 4/5      | 0          | 0     | 73       | 75     | 97.3%   | 98.1%    
deepseek-chat        | -                      | 5/5        | 5/5       | 4/5      | 0          | 0     | 73       | 75     | 97.3%   | 98.1%    
gemini-2.5-pro       | -                      | 5/5        | 5/5       | 4/5      | 0          | 0     | 73       | 75     | 97.3%   | 98.1%    
gpt-4o               | -                      | 3/5        | 3/3       | 2/3      | 2          | 0     | 39       | 75     | 52.0%   | 51.4%    
```
