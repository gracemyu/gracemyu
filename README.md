# Grace Yu

Things I've built or worked on.

## [Food is Medicine Benchmark](https://github.com/gracemyu/OpenFIM-Bench/tree/add-nhanes-merge-pipeline)

OpenFIM-Bench is an open benchmark for checking whether AI nutrition advice would hold up in a Food is Medicine program. The test cases are built from real US survey data and go through expert review.

I wrote the NHANES merge pipeline. It joins the 341 public NHANES tables into one row per participant per survey cycle, 113,386 rows by 14,066 columns, and asserts the row count against a spine after every join. Duplicate variables get resolved against CDC's own variable descriptions. From the merged data I cut a diabetes and kidney disease slice and trained three synthetic patient generators on it (CTGAN, GReaT, and a small tabular diffusion model I wrote) to find out whether synthetic patients are good enough to build benchmark cases from. The diffusion model came out closest to the real data.

## [Artemis](https://github.com/Abhi7419/artemisv2)

Artemis builds a relationship graph of people and organizations from public web sources and finds introduction paths through it. Nothing goes in the graph without a source URL and the sentence that supports it.

I have 20 merged PRs in the repo. The bigger ones: cost shaping for the pathfinder so it stops routing through celebrities and mega-hubs, a guard against merging two people who share a name, firm-roster and headless-browser scrapers as fallback providers, and a check that verifies the evidence on each hop of a path before returning it. I also fixed a batch of less visible things, like Postgres write concurrency, NUL bytes in scraped text breaking builds, and a Claude entity filter that only ran at ranking time and not when saving. In the [demo app](https://github.com/Abhi7419/DrewGloverDemo) I built the Claude and Ollama classifiers that score how strong a relationship is.

## [Elutive](https://elutive.com)

Elutive is an AI layer for analytical chemistry. Labs that run LC-MS in drug development use it to troubleshoot methods and review run data. It points at the likely cause of a problem and suggests a fix. The code is private.

## AI gateway at Ellucian (internship)

An internal AI gateway with model routing, governance, cost attribution, and MCP tool access.

## Agentic on-call tools at AWS (internship)

An MCP server that pulls runbooks and knowledge bases into live incident investigations.
