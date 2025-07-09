# Strategy Hub

Folder layout:

```
app/
  shared/base_strategy.py
  strategies/
    generic/sma_crossover.py
    intraday/...
    swing/...
```

Enhancements discussed:

- Add optional `on_tick()` hook while keeping candle default.
- Windowed vote (10‑15 ticks) to avoid single‑strategy noise.
