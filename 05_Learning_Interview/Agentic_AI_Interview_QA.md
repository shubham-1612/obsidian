# Agentic AI — Interview Q&A

> Crib sheet for quick review before calls.

*Explain inversion of control in agent orchestrators.*  
A: Orchestrator (graph) owns loop; agents are invoked as pure functions, encouraging reusability and traceability.

*How does memory summarization improve recursive agents?*  
A: Reduces context size (token cost) and quells irrelevant branches, yielding ~40 % speed‑up.

*Trade‑offs of storing embeddings in KG vs vector DB?*  
A: KG gives rich semantics but slower; vector DB faster ANN search but weak relationships.
