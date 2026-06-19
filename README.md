# BenchModel — public results

Defanged evidence behind the [BenchModel leaderboard](https://benchmodel.io/leaderboard): the injected bug set, the exact diff each reviewer model saw, every model's raw findings, and the scored summary — one folder per run.

All payloads are detection fixtures (instruction text, fake values, or one-token code changes). There is no working exploit or malware in this repository.

## Runs

| Run | Benchmark |
| --- | --- |
| [`fastapi/v2`](fastapi/v2/) | FastAPI Full-Stack Bug Injection — v2 |
| [`prompt-injection/v1`](prompt-injection/v1/) | Prompt Injection Defense — v1 |
| [`prompt-injection/v2`](prompt-injection/v2/) | Prompt Injection Defense — v2 |
| [`react/v1`](react/v1/) | React Frontend Bug Injection — v1 |
| [`react/v2`](react/v2/) | React Frontend Bug Injection — v2 |
| [`routefit/v2`](routefit/v2/) | RouteFit Bug Injection — v2 |
| [`supply-chain/v1`](supply-chain/v1/) | Supply Chain Defense — v1 |
