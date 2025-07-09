# Recursive Content Generator

Generates LinkedIn / Instagram content with images, using depth‑controlled recursion.

## Flow
1. **Seed topic** (e.g. *Akbar*).  
2. Agent expands → sub‑angles, counter‑factual hooks.  
3. `ImageAgent` calls DALL·E for carousel.  
4. Summaries stored in KG & posted via API.

### Issues Raised
- Generated posts felt *superficial* → need richer retrieval grounding.
- Scope filtering inefficient → add summarization checkpoint.

### TODO
- Plug in Wikipedia/ArXiv retriever for depth.  
- Persist per‑topic graph of what’s been posted to avoid repetition.
