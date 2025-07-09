# Agentic Product‑Development Team

A “virtual company” of agents covering PO, PM, BA, Dev, QA.

## Hardest Agent
> **Developer Agent** — must *understand* and *run* code across arbitrary stacks.

### Proposed Solution
- Use containerized *tool execution* sandbox (Docker‑in‑Docker).  
- Developer Agent asks Orchestrator for **`run(code)`** tool, receives result JSON.  
- Static code analysis with `tree‑sitter` to build context map beyond the LLM window.

### Outstanding Problems
1. Scaling comprehension for monorepos.  
2. Safe execution & resource limits (seccomp).
