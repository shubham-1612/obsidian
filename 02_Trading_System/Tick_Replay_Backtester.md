# Tick Replay Backtester

Plays historical stream in *real‑time* pacing.

| Feature | Status |
|---------|--------|
| Async loop per symbol | ✅ |
| Grid‑search (param sweep) | ✅ |
| Resume from last checkpoint | ⏳ (planned) |

Refactor idea: decouple *clock* so we can **time‑warp** during backtest accelerations.
