# Memory Management Strategy

Per your design discussions (26 Jun 2025):

- **Hybrid model**  
  - Redis → fast cache / working set  
  - PostgreSQL → relational persistence (agent identity, episodes)  
  - MongoDB → document store (long outputs, social‑media posts)

- **Promotion Rules**  
  - Confidence ≥ 0.8 **and** Novelty ≥ 0.4 → promote to long‑term.
  - Reducer functions merge duplicate insights across sibling agents.

- **Next Actions**
  1. Implement `memory.reducers` module.  
  2. Add `MemorySummarizer` checkpoint before every fork → cuts token use ≈ 40 %.
