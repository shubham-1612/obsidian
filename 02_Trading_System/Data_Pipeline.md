# Data Pipeline

1. **Historical Fetcher** – grabs 2 years of 1 min OHLC via Kite Connect.
2. **Tick Collector** – WebSocket → parquet sink.  
   - TODO: implement 60‑day backfill before live ticks.
3. **Resampler** – Tick → Candle aggregator (configurable window).

All Parquet shards stored under `data/ohlc/{symbol}/YYYY-MM-DD.parquet`.
