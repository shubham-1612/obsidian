# Knowledge Graph Integration

> _“The KG will be the semantic backbone of all agents.”_

| Dimension | Decision / Idea |
|-----------|-----------------|
| Platform  | Neo4j for prototype; optional RedisGraph for speed |
| Entity Types | Agent, Goal, SubGoal, Prompt, Output, Source |
| Edges | `produced`, `refers_to`, `contradicts`, `supports` |
| Vector Layer | HNSW index on `Output.embedding` for hybrid search |
| Risks | Ontology creep, write‑amplification at deep recursion |

### Implementation Steps
1. POC: persist agent prompts + outputs for a single recursion chain.
2. Build retrieval wrapper → agents can `query_kg()` alongside LLM.
3. Benchmark: ensure read latency ≤ 100 ms to avoid throttling loops.
