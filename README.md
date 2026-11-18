# ASX SEPA+VCP Screener

Automated daily screener for ASX stocks using Minervini's SEPA trend template, VCP scoring, stage classification, technical indicators and basic fundamentals. Sibling of [us-sepa-vcp-screener](https://github.com/KidLearning99/us-sepa-vcp-screener) and [india-sepa-vcp-screener](https://github.com/KidLearning99/india-sepa-vcp-screener).

- **Universe:** ASX-listed companies at or above A$100M market cap, from the ASX company directory (MarkitDigital). Change with the `MIN_MARKET_CAP` env var. `data/asx_universe.txt` is a fallback snapshot.
- **Benchmark:** S&P/ASX 200 (^AXJO) for relative strength, beta and correlation.
- **Recent IPOs:** listings with under 200 sessions are always kept and tagged, since they cannot pass the MA150/MA200 checks yet.
- **Thin / no-trade stocks:** flagged in the table and excluded from the Top 10.
- **Data:** Yahoo Finance via `yfinance`.
- **Schedule:** GitHub Actions; output is deployed to the `gh-pages` branch.

Educational and research use only. Not financial advice. Prices in AUD.
