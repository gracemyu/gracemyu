# Grace Yu

Projects I have built or contributed to.

## [Food is Medicine Benchmark](https://github.com/gracemyu/OpenFIM-Bench/tree/add-nhanes-merge-pipeline)

OpenFIM-Bench is an open benchmark for testing whether AI-generated nutrition guidance is safe, evidence-based, and appropriate for Food is Medicine programs, grounded in real US population data.

I built the NHANES merge pipeline: it joins 341 public NHANES tables into one row per participant per survey cycle (113,386 rows by 14,066 columns), resolves duplicate variables against CDC's own descriptions, cuts a diabetes and kidney disease slice, and compares three synthetic patient generators, including a tabular diffusion model I wrote, to see which is good enough to build benchmark cases from.

## [Artemis](https://github.com/Abhi7419/artemisv2)

Artemis discovers connections between people and organizations from public sources, builds an evidence-grounded relationship graph, and finds warm introduction paths through it. Every edge carries a source URL and evidence snippet.

I shipped 20 merged pull requests covering pathfinding cost shaping (hop surcharge, fame penalty, mega-hub degree), a homonym disambiguation guard, firm-roster and headless-browser fallback providers, per-hop evidence verification, a Claude entity filter at persist time, and Postgres concurrency and NUL-byte fixes. I also built the Claude and Ollama relationship-strength classifiers in the [demo app](https://github.com/Abhi7419/DrewGloverDemo).

## [Elutive](https://elutive.com)

Elutive is the AI layer for analytical chemistry: it helps LC-MS labs in drug development troubleshoot methods and review run data by identifying likely causes of problems and suggesting fixes.

The code is private.

## AI gateway at Ellucian (internship)

An internal AI gateway with model routing, governance, cost attribution, and MCP tool access.

## Agentic on-call tools at AWS (internship)

An MCP server that pulls runbooks and knowledge bases into live incident investigations.
